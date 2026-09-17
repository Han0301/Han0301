<div align="center">

# Hi, I'm Han Zhang 👋

### Robotics Engineering Student · Machine Vision · Multi-Sensor Fusion

机器人工程专业本科生，专注于机器人视觉感知、深度相机、三维几何与多传感器融合。

[![GitHub](https://img.shields.io/badge/GitHub-Han0301-181717?style=flat-square&logo=github)](https://github.com/Han0301)
[![University](https://img.shields.io/badge/GDUT-Robotics_Engineering-005BAC?style=flat-square)](https://www.gdut.edu.cn/)
[![Email](https://img.shields.io/badge/Email-hanzhang060301%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:hanzhang060301@gmail.com)

</div>

## About Me

我目前就读于广东工业大学机器人工程专业，主要围绕机器人竞赛中的视觉感知问题开展工程实践。从仿真验证、数据采集和模型训练，到真实机器人上的相机、激光雷达与运动信息融合，我希望把算法做成能够稳定运行的完整系统。

- 🔭 正在完善 **RC26 机器人视觉感知系统**
- 🧠 研究方向：**Machine Vision / Deep Learning / 3D Geometry / Sensor Fusion**
- 🤖 工程方向：**ROS、RealSense、LiDAR、YOLO、PnP、OpenVINO**
- 🌱 持续学习模型部署、视觉算法优化与机器人系统工程
- 📫 联系方式：**hanzhang060301@gmail.com**

## Featured Projects

| Project | Description | Tech |
| --- | --- | --- |
| [RC26 Vision YOLO](https://github.com/Han0301/RC26_Vision_Yolo) | 面向固定 12 个 ROI 的二分类模型：12 ROI 合并后单次批量通过共享 Backbone，再使用多头自注意力融合跨位置特征；支持训练、推理、注意力可视化及 ONNX/OpenVINO 导出。 | Python · PyTorch · YOLO11 · ONNX · OpenVINO |
| [RC26 Vision Camera](https://github.com/Han0301/RC26_Vision_camera) | 基于 RealSense D435 的相机感知工作区，覆盖深度点云平面拟合、PnP 位姿解算、KFS 方块定位、AprilTag 识别与数据集录制。 | C++ · ROS Noetic · OpenCV · PCL · RealSense |
| [RC26 Vision Simulation](https://github.com/Han0301/GDUT_RC26_Vision_Simulation) | RC26 视觉仿真环境，使用 Z-buffer 完成 3D→2D 映射与遮挡处理，并结合 HSV 检测、相机标定、PID 控制及地图数据生成。 | C++ · ROS · Gazebo · OpenCV · Python |
| [RC26 Vision Fusion](https://github.com/Han0301/GDUT_RC26_Vision_src) | 真实机器人上的融合代码工作区，整合双相机、双激光雷达、里程计、IMU、YOLO、PnP 与 Z-buffer 感知模块。 | C++ · ROS · LiDAR · Multi-threading · Sensor Fusion |

## System Perspective

```text
Simulation & Data Generation
            │
            ▼
Camera / LiDAR / Odometry / IMU
            │
            ▼
Detection · Depth · PnP · Z-buffer
            │
            ▼
Multi-Sensor Fusion & Coordinate Transform
            │
            ▼
Robot Decision / Control / Visualization
```

我的仓库分别对应这条链路中的模型、相机、仿真和上车融合环节，目标是持续提升系统的准确性、实时性与可维护性。

## Tech Stack

<p>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/ROS-22314E?style=flat-square&logo=ros&logoColor=white" alt="ROS" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV" />
  <img src="https://img.shields.io/badge/YOLO11-111F68?style=flat-square&logo=yolo&logoColor=white" alt="YOLO11" />
  <img src="https://img.shields.io/badge/OpenVINO-00A3E0?style=flat-square&logo=intel&logoColor=white" alt="OpenVINO" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
</p>

### Areas I Work With

- **Robot Vision:** object detection, ROI classification, depth imaging, AprilTag
- **3D Geometry:** PnP, point clouds, plane fitting, coordinate transforms
- **Deep Learning:** PyTorch, YOLO11, multi-head self-attention, focal loss
- **Deployment:** ONNX, OpenVINO, real-time inference
- **Robotics:** ROS Noetic, Gazebo, RealSense, LiDAR, sensor fusion
- **Engineering:** C++/Python, multithreading, data pipelines, debugging and visualization

## Current Focus

```python
current_focus = {
    "perception": ["12-ROI classification", "cross-ROI attention"],
    "geometry": ["PnP", "point-cloud processing", "Z-buffer occlusion"],
    "robotics": ["camera-LiDAR fusion", "real-time ROS pipelines"],
    "deployment": ["ONNX", "OpenVINO"],
}
```

## GitHub Activity

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Han0301&show_icons=true&hide_border=true&theme=transparent&rank_icon=github" alt="Han0301 GitHub statistics" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Han0301&layout=compact&hide_border=true&theme=transparent&langs_count=6" alt="Han0301 most used languages" />
</div>

---

<div align="center">

**Build, test, deploy — turn perception algorithms into reliable robot systems.**

[Projects](https://github.com/Han0301?tab=repositories) · [RC26 YOLO](https://github.com/Han0301/RC26_Vision_Yolo) · [RC26 Camera](https://github.com/Han0301/RC26_Vision_camera) · [Email](mailto:hanzhang060301@gmail.com)

</div>
