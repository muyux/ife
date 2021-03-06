作业提交截止时间：01-01

# 第六十三天到第六十六天：足球小将（三）

## 课程目标

通过趣味练习，来强化对于 JavaScript 的熟悉

持续练习如何对于问题进行抽象，应用面向对象或者各种设计模式进行问题的解决

这也是本次2018百度前端技术学院零基础班最后一个任务，祝大家学习开心

## 课程描述

我们在前两个子任务中完成了运动员的运动，足球的运动，接下来我们来实现具体的足球运动的行为。

### 踢球行为

#### 停球

停球，就是将运动向自己的足球控制在自己的一定范围内。

将上一任务中的踢球封装为父类，停球继承踢球。

我们定义停球的行为，是将足球踢向一个距离自己很近的位置，甚至距离为0。比如：

  * 球员在原地停球时，需要将球停到自己脚下
  * 球员在前插奔跑中停球，需要将球停到自己奔跑方向 2 米远的地方，便于下一步射门
  * 球员在摆脱防守队员中停球，有时候需要将球停到自己当前方向反方向 1 米远的地方，便于摆脱

为了简化需求，我们将停球动作抽象为以下规则：

  * 当球员静止时，球停在原地
  * 当球员运动时，球停到 1 秒后球员在的位置

#### 传球

传球就是将球传给另外一个运动员，依然是继承踢球的父类

最简单的传球，就是看目标运动员在哪里，然后传给他，但在实际比赛中，我们往往会把球传给目标运动员的运动方向，或者躲开防守队员，将球传到空档区域。

为了简化需求，我们将传球抽象为以下规则：

  * 对于传球目标静止的，我们将球直接传给他
  * 对于传球目标在运动中，我们需要通过计算，算好提前量，把球传到目标球员运动方向的前方，正好是目标球员跑到那个位置的时候，球也传到那个位置

#### 带球

带球是不断地踢球的过程，每次踢一小步，让球向前滚动一小段距离，然后奔跑跟上。

我们简化需求，假设带球过程中，触球的频率是固定的，假设每秒触球一次，所以带球过程中，每次触球踢球的距离为，运动员按照当前速度 1 秒后到达的距离。

#### 射门

射门在这其中是最好处理的，朝向球门射去即可。

为了简化射门中的参数传递，我们把射门抽象为以下几种：

  * 射向球门左上角
  * 射向球门左下角
  * 射向球门右上角
  * 射向球门右上角
  * 射向球门正上方
  * 射向球门正下方

#### 验证

如前面的任务，创建一系列的参数可视化配置，及方法执行按钮，验证如上行为的实现和效果验证。

### 提交

把你的代码放在Github后进行提交

### 总结

依然把今天的学习用时，收获，问题进行记录

### 最后

零基础班 66 天任务发布结束，希望对您有所帮助，祝您学习顺利！

