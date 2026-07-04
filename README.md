<h1 align="center">👋 你好，我是 Han0301</h1>

<p align="center">
  <b>RC26 机器人竞赛视觉系统开发者</b><br>
  多传感器融合 · 自定义 YOLOv11 模型 · ROS 机器人感知
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ROS-Noetic-22314E?style=flat-square&logo=ros" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv" />
  <img src="https://img.shields.io/badge/C++17-00599C?style=flat-square&logo=cplusplus" />
  <img src="https://img.shields.io/badge/Python_3.8-3776AB?style=flat-square&logo=python" />
  <img src="https://img.shields.io/badge/YOLOv11-00FFFF?style=flat-square" />
  <img src="https://img.shields.io/badge/RealSense-FF0000?style=flat-square" />
  <img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake" />
</p>

---

## 📂 项目一览

| 项目 | 描述 | 版本演进 | 最新 Release |
|------|------|---------|-------------|
| [🧪 **RC26_Vision_Simulation**](https://github.com/Han0301/RC26_Vision_Simulation) | Z-buffer 仿真感知工作区，从仿真验证到算法定型 | `world_ws5` → `world_ws13.5`（10 个版本） | [v13.5](https://github.com/Han0301/RC26_Vision_Simulation/releases/tag/world_ws/v13.5) |
| [📷 **RC26_Vision_camera**](https://github.com/Han0301/RC26_Vision_camera) | 相机视觉感知工作区，RealSense 驱动 + PnP + Apriltag | `camera_ws3` → `camera_ws2.51`（8 个版本） | [v2.51](https://github.com/Han0301/RC26_Vision_camera/releases/tag/camera/v2.51) |
| [🧠 **RC26_Vision_Yolo**](https://github.com/Han0301/RC26_Vision_Yolo) | YOLOv11 自定义模型训练，3 分类到注意力机制 | `Custom_12roi` → `Custom_atten2`（6 个版本） | [v2.1](https://github.com/Han0301/RC26_Vision_Yolo/releases/tag/yolo/v2.1) |
| [🔗 **RC26_Vision_src**](https://github.com/Han0301/RC26_Vision_src) | 上车融合代码，多传感器融合竞赛系统 | `merge_ws20` → `rc_ws2`（12 个版本） | [v2](https://github.com/Han0301/RC26_Vision_src/releases/tag/rc/v2) |

---

## 🗺️ 项目演进路线

```
2025                        2026
├───world_ws5────────world_ws13.5───┐
│   Z-buffer 遮挡处理算法迭代        │
├───camera_ws3────camera_ws2.51─────┤
│   RealSense → PnP → Apriltag       │
├───Custom_12roi───Custom_atten2────┤
│   3分类 → 2分类 → 注意力机制        │
├───merge_ws20───────────rc_ws2─────┘
    上车初始版 → 竞赛最终版
```

---

## 🏅 版本里程碑

### 稳定版（推荐使用）

| 版本标签 | 对应版本 | 说明 |
|---------|---------|------|
| `world_ws/v9.0` | world_ws9 | Z-buffer 感知管线旗舰版，适合仿真测试 |
| `world_ws/v13.5` | world_ws13.5 | 大规模地图数据更新最终版 |
| `camera/v2.4` | camera_ws2.4 | KFS 35cm 方块位姿识别稳定版 |
| `camera/v2.51` | camera_ws2.51 | Apriltag R1 识别版 |
| `yolo/v2.0` | Custom_atten | 注意力机制引入版，模块化架构 |
| `yolo/v2.1` | Custom_atten2 | 12ROI + 单 ROI 联合训练版 |
| `merge/v39.8` | merge_ws39.8 | 上位机集成稳定版 |
| `rc/v2` | rc_ws2 | 竞赛最终版，含设备自检 |

---

## 🛠️ 核心技术

<table>
<tr>
<th>领域</th>
<th>技术</th>
<th>用途</th>
</tr>
<tr>
<td><b>感知</b></td>
<td>Z-buffer 遮挡处理</td>
<td>利用深度缓冲判断目标遮挡状态，过滤假阳性检测</td>
</tr>
<tr>
<td><b>感知</b></td>
<td>PnP 位姿估计</td>
<td>2D-3D 对应点解算目标 6D 位姿，用于机械臂抓取</td>
</tr>
<tr>
<td><b>感知</b></td>
<td>Apriltag 检测</td>
<td>在 R1 机器人上固定 Apriltag 标签进行识别定位</td>
</tr>
<tr>
<td><b>模型</b></td>
<td>YOLOv11 12-ROI 分类</td>
<td>对 12 个固定 ROI 进行方块有无的二分类/三分类</td>
</tr>
<tr>
<td><b>模型</b></td>
<td>LocalGrid Attention</td>
<td>局部网格注意力机制，让 ROI 之间交互上下文信息</td>
</tr>
<tr>
<td><b>模型</b></td>
<td>Point-size 加权损失</td>
<td>根据点云密度对损失函数加权，关注信息丰富区域</td>
</tr>
<tr>
<td><b>融合</b></td>
<td>多传感器融合框架</td>
<td>视觉 + 激光雷达 + Z-buffer 三通道决策层仲裁</td>
</tr>
<tr>
<td><b>融合</b></td>
<td>上层决策层</td>
<td>三级仲裁机制（三通道一致/两通道一致/全冲突）</td>
</tr>
<tr>
<td><b>定位</b></td>
<td>视觉里程计 + GICP</td>
<td>视觉特征点跟踪与 nano_gicp 点云配准融合定位</td>
</tr>
<tr>
<td><b>运维</b></td>
<td>参数配置系统</td>
<td>YAML 参数外部化，运行时动态调整无需重新编译</td>
</tr>
<tr>
<td><b>运维</b></td>
<td>设备自检</td>
<td>启动时自动检测相机/激光雷达/IMU 传感器状态</td>
</tr>
</table>

---

## 📦 各项目 Release 导航

<p align="center">
  <a href="https://github.com/Han0301/RC26_Vision_Simulation/releases">🔗 RC26_Vision_Simulation Releases</a> ·
  <a href="https://github.com/Han0301/RC26_Vision_camera/releases">🔗 RC26_Vision_camera Releases</a> ·
  <a href="https://github.com/Han0301/RC26_Vision_Yolo/releases">🔗 RC26_Vision_Yolo Releases</a> ·
  <a href="https://github.com/Han0301/RC26_Vision_src/releases">🔗 RC26_Vision_src Releases</a>
</p>

---

<p align="center">
  <sub>从仿真到实车，从感知到融合，从训练到部署 — 完整的机器人竞赛视觉系统</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/Han0301/RC26_Vision_Simulation?style=social" />
  <img src="https://img.shields.io/github/stars/Han0301/RC26_Vision_camera?style=social" />
  <img src="https://img.shields.io/github/stars/Han0301/RC26_Vision_Yolo?style=social" />
  <img src="https://img.shields.io/github/stars/Han0301/RC26_Vision_src?style=social" />
</p>
