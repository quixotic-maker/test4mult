# Smart Cafe Order System)

- **项目简介**:

  用Python编写两个ROS 2节点来模拟咖啡厅的后台：

  1. **`OrderManager`节点**: 提供一个Action服务`/submit_order`，接收订单（例如`['latte', 'cappuccino']`）。它负责维护所有订单的状态（`QUEUED`, `IN_PROGRESS`, `COMPLETED`）。
  2. **`BaristaBot`节点**: 作为一个客户端，不断地从`OrderManager`获取状态为`QUEUED`的订单。接收到订单后，它将订单状态更新为`IN_PROGRESS`，然后“制作”每一杯咖啡（通过`time.sleep()`模拟耗时），制作完成后将最终状态更新为`COMPLETED`。

- **技术要求**:

  - 语言: Python
  - 框架: ROS 2 Humble (重点考察Action的使用)

- **交付物**:

  1. 一个包含两个节点的ROS 2功能包的GitHub仓库链接。
  2. **效果录屏**: 用于展示你的代码运行及测试效果。
  3. 仓库中必须包含一份`README.md`，内容包括：
     - 如何启动和测试整个系统。
     - 画出两个节点间的通信流程图。
     - **思考题**: 如果`BaristaBot`节点在制作一杯`latte`时崩溃了，当前的订单状态会是什么？你认为系统应该如何处理这种情况才能保证订单不会丢失？**（请在你的代码中实现一个基础的恢复或保障机制，并在README中详细阐述你的方案。）**