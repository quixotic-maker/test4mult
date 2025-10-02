**操作系统**: 推荐使用 Ubuntu 22.04。

**ROS 2 Humble**: 请严格按照ROS官方文档进行桌面版安装：[ROS 2 Humble Installation Guide](https://www.google.com/search?q=https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html)

**Python 依赖 (针对项目1, 2, 3)**:

Bash

```
pip install ultralytics opencv-python numpy py_trees
```

**C++ 编译工具 (针对项目4)**:

Bash

```
sudo apt update && sudo apt install build-essential cmake git
```

**Git 配置**:

- 请确保你的Git已配置好用户名和邮箱。
- [Git首次配置官方教程](https://git-scm.com/book/zh/v2/起步-初次运行-Git-前的配置)