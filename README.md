<div align="center">

# 👋 你好，我是 Han0301

**RC26 机器人竞赛视觉系统开发者** · 多传感器融合 · YOLOv11 自定义模型 · ROS Noetic

[![GitHub](https://img.shields.io/badge/GitHub-Han0301-181717?logo=github&style=flat-square)](https://github.com/Han0301)
[![ROS](https://img.shields.io/badge/ROS-Noetic-22314E?logo=ros&style=flat-square)]()
[![Python](https://img.shields.io/badge/Python-3.8-3776AB?logo=python&style=flat-square)]()
[![C++](https://img.shields.io/badge/C++-17-00599C?logo=cplusplus&style=flat-square)]()

---

### 🏆 项目总览

</div>

<table align="center">
<tr>
<td width="33%" align="center">
<a href="https://github.com/Han0301/RC26_Vision_Simulation">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=Han0301&repo=RC26_Vision_Simulation&theme=dark&hide_border=true" />
</a>
<br/><b>🧪 Z-buffer 仿真感知</b>
<br/>10 个版本的仿真→实车算法迭代
</td>
<td width="33%" align="center">
<a href="https://github.com/Han0301/RC26_Vision_camera">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=Han0301&repo=RC26_Vision_camera&theme=dark&hide_border=true" />
</a>
<br/><b>📷 相机视觉感知</b>
<br/>8 个版本的 RealSense 相机管线
</td>
<td width="33%" align="center">
<a href="https://github.com/Han0301/RC26_Vision_Yolo">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=Han0301&repo=RC26_Vision_Yolo&theme=dark&hide_border=true" />
</a>
<br/><b>🧠 YOLOv11 自定义模型</b>
<br/>6 个版本的注意力机制演进
</td>
</tr>
<tr>
<td width="33%" align="center">
<a href="https://github.com/Han0301/RC26_Vision_src">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=Han0301&repo=RC26_Vision_src&theme=dark&hide_border=true" />
</a>
<br/><b>🔗 上车融合代码</b>
<br/>12 个版本的多传感器融合系统
</td>
<td width="33%" align="center">
<a href="https://github.com/Han0301/RC26_Vision_camera/releases">
<img src="https://img.shields.io/github/v/release/Han0301/RC26_Vision_camera?label=camera&style=flat-square&color=blue" />
</a>
<br/><b>📦 已发布版本</b>
<br/>camera/v2.51 · merge/v39.8 · yolo/v2.1
</td>
<td width="33%" align="center">
<a href="https://github.com/Han0301?tab=repositories">
<img src="https://img.shields.io/badge/View%20All-4%20Repos-2ea44f?style=flat-square" />
</a>
<br/><b>📂 全部仓库</b>
<br/>点击查看所有项目
</td>
</tr>
</table>

---

<br/>

<div align="center">

### 📊 项目演进历程

</div>

```mermaid
timeline
    title RC26 视觉系统迭代路线
    section 仿真验证
      world_ws5-13.5 : Z-buffer 遮挡处理算法
                      : HSV 目标检测
                      : PID 运动控制
    section 相机感知
      camera_ws3-2.51 : RealSense 驱动
                       : PnP 位姿估计
                       : OpenVINO 推理
                       : Apriltag 识别
    section 模型训练
      yolo11_Custom   : 3分类 → 2分类
      _12roi→atten2   : 数量约束损失
                       : Z-buffer 集成
                       : Point-size 加权
                       : 注意力机制
    section 上车融合
      merge_ws20→rc_ws2 : 多传感器融合
                         : LiDAR 识别
                         : 上层决策层
                         : 竞赛最终版
```

<br/>

<div align="center">

### 🛠️ 技术栈

</div>

<p align="center">
<img src="https://img.shields.io/badge/ROS-Noetic-22314E?style=for-the-badge&logo=ros" />
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch" />
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv" />
<img src="https://img.shields.io/badge/OpenVINO-0078D4?style=for-the-badge" />
<img src="https://img.shields.io/badge/RealSense-FF0000?style=for-the-badge" />
<img src="https://img.shields.io/badge/Livox_MID_360-00C853?style=for-the-badge" />
<img src="https://img.shields.io/badge/C++17-00599C?style=for-the-badge&logo=cplusplus" />
<img src="https://img.shields.io/badge/Python_3.8-3776AB?style=for-the-badge&logo=python" />
<img src="https://img.shields.io/badge/YOLOv11-00FFFF?style=for-the-badge" />
<img src="https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake" />
</p>

<br/>

<div align="center">

### 📈 GitHub 统计

</div>

<p align="center">
<img src="https://github-readme-stats.vercel.app/api?username=Han0301&show_icons=true&theme=dark&hide_border=true&count_private=true&bg_color=0d1117" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Han0301&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&langs_count=6" height="165"/>
</p>

<br/>

<div align="center">

### 🏅 版本里程碑

</div>

| 领域 | 稳定版本 | 最新版本 | 亮点 |
|------|---------|---------|------|
| 🧪 **Z-buffer 仿真** | `world_ws/v9.0` | `world_ws/v13.5` | 遮挡处理 + PID 控制 |
| 📷 **相机感知** | `camera/v2.4` | `camera/v2.51` | Apriltag R1 识别 |
| 🧠 **YOLO 模型** | `yolo/v2.0` | `yolo/v2.1` | LocalGrid 注意力 |
| 🔗 **上车融合** | `merge/v39.8` | `rc/v2` | 竞赛最终版系统 |

<p align="center">
<a href="https://github.com/Han0301/RC26_Vision_Simulation/releases">
<img src="https://img.shields.io/github/v/release/Han0301/RC26_Vision_Simulation?label=world_ws&style=flat-square" />
</a>
<a href="https://github.com/Han0301/RC26_Vision_camera/releases">
<img src="https://img.shields.io/github/v/release/Han0301/RC26_Vision_camera?label=camera&style=flat-square" />
</a>
<a href="https://github.com/Han0301/RC26_Vision_Yolo/releases">
<img src="https://img.shields.io/github/v/release/Han0301/RC26_Vision_Yolo?label=yolo&style=flat-square" />
</a>
<a href="https://github.com/Han0301/RC26_Vision_src/releases">
<img src="https://img.shields.io/github/v/release/Han0301/RC26_Vision_src?label=merge&style=flat-square" />
</a>
</p>

<br/>

<div align="center">

---

⭐ **从仿真到实车，从感知到融合，从训练到部署 — 完整的机器人竞赛视觉系统。**

</div>
