# Robot's Morning Routine BT

- **项目简介**:

  使用Python的行为树库py_trees，构建一个模拟机器人早晨起床流程的行为树。你不需要控制任何真实或仿真的机器人，只需让行为节点打印信息即可。

  - **基础行为 (Action Nodes)**: `IsAlarmRinging` (检查闹钟，随机返回成功或失败), `HitSnoozeButton` (打印"Snoozing..."), `GetOutOfBed` (打印"Getting up!"), `BrewCoffee` (打印"Brewing coffee...")。
  - **任务逻辑**: 使用行为树的**控制流节点 (Control Flow Nodes)**，如`Sequence`（顺序执行）, `Selector`（选择其一）, `Parallel`（并行），来组合上述基础行为，实现一个有意义的流程。例如：“如果闹钟响了，机器人会选择‘起床’或‘按掉闹钟’；起床后，必须先‘冲咖啡’才能开始一天的工作”。

- **技术要求**:

  - 语言: Python
  - 框架: `py_trees` (ROS 2官方推荐的行为树库)

- **交付物**:

  1. 一个包含你的`py_trees`脚本的GitHub仓库链接。
  2. **效果录屏**: 用于展示你的代码运行及测试效果。
  3. 仓库中必须包含一份`README.md`，内容包括：
     - 如何运行你的行为树。
     - 用文字或截图画出你的行为树结构。
     - **思考题**: 解释你在哪里使用了`Sequence`，在哪里使用了`Selector`，为什么？如果现在要增加一个条件“仅在工作日冲咖啡”，你会在行为树的哪个部分进行修改？**（请在代码中实现此修改，并在README中指出相关代码部分，解释你的实现方式。）**