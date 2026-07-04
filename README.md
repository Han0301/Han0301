<h1 align="center">👋 你好，我是 Han0301</h1>

<p align="center">
  <b>机器人竞赛视觉感知工程师</b><br>
  多传感器融合 · YOLOv11 自定义模型 · ROS 机器人开发 · C++/Python
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ROS-Noetic-22314E?style=flat-square&logo=ros" />
  <img src="https://img.shields.io/badge/C++-17-00599C?style=flat-square&logo=cplusplus" />
  <img src="https://img.shields.io/badge/Python-3.8-3776AB?style=flat-square&logo=python" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv" />
  <img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake" />
  <img src="https://img.shields.io/badge/YOLOv11-00FFFF?style=flat-square" />
  <img src="https://img.shields.io/badge/OpenVINO-0078D4?style=flat-square" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git" />
</p>

---

## 🙋 关于我

- 🔭 专注于 **RC26 机器人竞赛** 的视觉感知系统开发
- 🌱 当前工作的核心是 **多传感器融合**（相机 + 激光雷达 + Z-buffer）与 **YOLOv11 自定义模型训练**
- 🎯 目标：从仿真验证 → 模型训练 → 上车部署，打造完整的竞赛机器人视觉系统
- ⚡ 版本迭代哲学：每个版本解决一个真实问题，用 Release 记录演进

---

## 📂 项目总览

所有仓库均采用 **版本迭代 + Release** 的方式管理，每个版本提交都记录了真实的问题背景与改进动机。

<table>
<tr>
<th>项目</th>
<th>技术栈</th>
<th>版本数</th>
<th>最新 Release</th>
<th>核心功能</th>
</tr>
<tr>
<td><a href="https://github.com/Han0301/RC26_Vision_Simulation"><b>🧪 Simu</b></a></td>
<td>C++ / ROS / PCL / OpenCV</td>
<td>10</td>
<td><a href="https://github.com/Han0301/RC26_Vision_Simulation/releases/tag/world_ws/v13.5">v13.5</a></td>
<td>Z-buffer 遮挡处理 · HSV 检测 · PID 控制 · 数据集录制</td>
</tr>
<tr>
<td><a href="https://github.com/Han0301/RC26_Vision_camera"><b>📷 Camera</b></a></td>
<td>C++ / ROS / RealSense / OpenVINO</td>
<td>8</td>
<td><a href="https://github.com/Han0301/RC26_Vision_camera/releases/tag/camera/v2.51">v2.51</a></td>
<td>PnP 位姿估计 · KFS 方块定位 · Apriltag · 多线程管线</td>
</tr>
<tr>
<td><a href="https://github.com/Han0301/RC26_Vision_Yolo"><b>🧠 YOLO</b></a></td>
<td>Python / PyTorch / Ultralytics</td>
<td>6</td>
<td><a href="https://github.com/Han0301/RC26_Vision_Yolo/releases/tag/yolo/v2.1">v2.1</a></td>
<td>12-ROI 分类 · 注意力机制 · Point-size 加权 · 模型导出</td>
</tr>
<tr>
<td><a href="https://github.com/Han0301/RC26_Vision_src"><b>🔗 Merge</b></a></td>
<td>C++ / ROS / LiDAR / YOLO</td>
<td>12</td>
<td><a href="https://github.com/Han0301/RC26_Vision_src/releases/tag/rc/v2">v2</a></td>
<td>多传感器融合 · 上层决策 · 竞赛系统集成</td>
</tr>
</table>

---

## 🗺️ 技术演进路线

```
2025 ───────────────────────────────────────────────────────────────▶ 2026

仿真验证 ──▶ world_ws5  →  world_ws6  →  ...  →  world_ws13.5
                Z-buffer 遮挡    重构          旗舰版     地图数据更新

相机感知 ──▶ camera_ws3 →  camera_ws4  →  ...  →  camera_ws2.51
                PnP 初始      OpenVINO     KFS 方块    Apriltag R1

模型训练 ──▶ 12roi(v1.0) →  12roi_c2   →  ...  →  atten2(v2.1)
                3 分类     2 分类+数量约束   注意力机制   联合训练

上车融合 ──▶ merge_ws20 →  merge_ws21  →  ...  →  rc_ws2
                初始版       标定+线程池     竞赛候选版    竞赛最终版
```

---

## 🛠️ 核心技术能力

### 感知算法
| 技术 | 项目 | 说明 |
|------|------|------|
| 🔲 **Z-buffer 遮挡处理** | Simulation | 利用深度缓冲判断目标遮挡，过滤假阳性，提升遮挡场景检测可靠性 |
| 📐 **PnP 位姿估计** | Camera | 2D-3D 对应点解算目标 6D 位姿（位置 + 朝向），用于机械臂抓取 |
| 🏷️ **Apriltag 检测** | Camera | 在 R1 机器人上固定 Apriltag 标签进行识别与定位 |
| 🎯 **KFS 方块定位** | Camera | 基于点云处理的 35cm 方块 6D 位姿识别 |
| 🧩 **ORB 特征匹配** | Merge | 在纹理贫乏场景下维持视觉定位 |
| 🔄 **点云配准 (GICP)** | Merge | nano_gicp 轻量级配准，5 倍速度提升 |

### 模型训练
| 技术 | 项目 | 说明 |
|------|------|------|
| 🧬 **YOLOv11 自定义分类头** | YOLO | 在预训练 backbone 上设计 ROI 分类头，直接对 12 个区域分类 |
| ⚖️ **数量约束损失** | YOLO | 统计预测正样本数量与实际数量的 MSE 损失，约束输出分布 |
| ⚡ **Point-size 加权** | YOLO | 根据点云密度对损失加权，让模型关注信息丰富区域 |
| 👁️ **LocalGrid Attention** | YOLO | 局部网格注意力，让 ROI 之间交互上下文信息 |
| 🎯 **Focal Loss** | YOLO | 缓解类别不平衡，提升少数类（有方块）的召回率 |

### 系统集成
| 技术 | 项目 | 说明 |
|------|------|------|
| 🔗 **多传感器融合** | Merge | 视觉 + 激光雷达 + Z-buffer 三通道决策层仲裁 |
| 🏛️ **上层决策层** | Merge | 三级仲裁：一致/投票/最高置信度 |
| 📍 **视觉里程计 + EKF** | Merge | 特征点跟踪 + 轮式里程计融合定位 |
| ⚙️ **参数配置系统** | Merge | YAML 外部化 + 运行时动态调整，无需重新编译 |
| 🔍 **设备自检** | Merge | 启动时自动检测全部传感器状态 |
| 🖥️ **上位机监控** | Merge | 工控机-上位机双向通信，远程控制与状态监控 |

---

## 🏅 推荐稳定版本

| 标签 | 对应版本 | 推荐理由 |
|------|---------|---------|
| `world_ws/v9.0` | world_ws9 | 旗舰稳定版，完整的 Z-buffer 感知管线 + 相机标定 |
| `world_ws/v13.5` | world_ws13.5 | 最终版，大规模地图数据更新 |
| `camera/v2.4` | camera_ws2.4 | 稳定的 KFS 35cm 方块识别版 |
| `camera/v2.51` | camera_ws2.51 | Apriltag R1 识别版 |
| `yolo/v2.0` | Custom_atten | 注意力机制版，模块化架构 |
| `yolo/v2.1` | Custom_atten2 | 12ROI + 单 ROI 联合训练版 |
| `merge/v39.8` | merge_ws39.8 | 上位机集成稳定版 |
| `rc/v2` | rc_ws2 | 竞赛最终版，含设备自检、双雷达热备 |

---

## 📊 GitHub 统计

<p align="center">
  <a href="https://github.com/Han0301/RC26_Vision_Simulation"><img src="https://img.shields.io/github/stars/Han0301/RC26_Vision_Simulation?style=social&label=Simu" /></a>
  <a href="https://github.com/Han0301/RC26_Vision_camera"><img src="https://img.shields.io/github/stars/Han0301/RC26_Vision_camera?style=social&label=Camera" /></a>
  <a href="https://github.com/Han0301/RC26_Vision_Yolo"><img src="https://img.shields.io/github/stars/Han0301/RC26_Vision_Yolo?style=social&label=YOLO" /></a>
  <a href="https://github.com/Han0301/RC26_Vision_src"><img src="https://img.shields.io/github/stars/Han0301/RC26_Vision_src?style=social&label=Merge" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/github/last-commit/Han0301/RC26_Vision_src?style=flat-square&label=最近更新" />
  <img src="https://img.shields.io/github/repo-size/Han0301/RC26_Vision_src?style=flat-square&label=代码规模" />
  <img src="https://img.shields.io/badge/总计提交-36+%20versions-2ea44f?style=flat-square" />
</p>

---

<p align="center">
  <sub>✨ 从仿真验证 → 模型训练 → 上车部署，完整的机器人竞赛视觉系统全栈开发 ✨</sub>
</p>

<p align="center">
  <a href="https://github.com/Han0301/RC26_Vision_Simulation">Simulation</a> ·
  <a href="https://github.com/Han0301/RC26_Vision_camera">Camera</a> ·
  <a href="https://github.com/Han0301/RC26_Vision_Yolo">YOLO</a> ·
  <a href="https://github.com/Han0301/RC26_Vision_src">Merge</a> ·
  <a href="https://github.com/Han0301?tab=repositories">All Repos</a>
</p>
