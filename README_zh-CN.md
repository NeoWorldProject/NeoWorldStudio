<h1 align="center">NeoWorld Studio</h1>

<p align="center"><strong>白盒、智能体驱动的可交互三维世界重建</strong></p>

<p align="center">
  <a href="https://neoworldproject.github.io/Studio/"><img src="assets/project-page.svg" alt="项目主页与演示"></a>
  <img src="assets/arxiv-soon.svg" alt="arXiv：即将发布">
  <img src="assets/models-soon.svg" alt="Hugging Face：即将发布">
  <img src="assets/app-store-soon.svg" alt="App Store：即将发布">
</p>

<p align="center"><a href="README.md">English</a> · <strong>简体中文</strong></p>

> **研究预览。** 本仓库目前提供项目介绍。项目代码与 **MATRIX-Preview** 预训练权重计划从 **2026 年 9 月底**起陆续开放。

<p align="center">
  <a href="https://neoworldproject.github.io/Studio/#demos">
    <img src="assets/scene-preview.jpg" width="800" alt="场景重建预览：左侧为原始拍摄，右侧为 Blender 渲染的重建结果。">
  </a>
</p>
<p align="center"><sub>左侧：原始拍摄 · 右侧：Blender 渲染的重建结果</sub><br><a href="https://neoworldproject.github.io/Studio/#demos"><strong>观看场景演示 →</strong></a></p>

## 核心思路

NeoWorld Studio 以**白盒**方式构建可编辑、可交互的三维物体与场景。VLM 智能体生成显式几何，并调用 NeoSDK 工具逐步优化，**不依赖预训练的 3D 生成模型**。

几何程序、零件结构和每步优化操作均显式可见，建模与优化过程可检查、可解释、可编辑。重建不受某个预训练 3D 生成模型所学习的形状空间约束，可通过显式建模与工具调用应对新的物体。

### 物体：初始化、观察、优化

对于每个物体，我们先生成初始重建结果 **t0**，再由智能体对照渲染视图与原始观测，调用 [NeoSDK](https://github.com/NeoWorldProject/NeoSDK) 的几何优化工具，逐步优化物体的形状与结构。

### 场景：初始化、装配、优化

在场景层面，我们首先建立环境与物体布局的初始重建。物体重建完成后，将它们装配回场景，再结合场景级视觉反馈，进一步调整几何、摆放及其与周围环境的匹配。

## 面向可交互、Simulation-Ready 的场景

- **可动关节：** 支持配置可动关节、运动轴及运动范围，构建能够控制关节运动的物体。
- **逐零件物理属性：** 支持按零件设置物理参数，例如密度，并结合几何推导质量与惯性。
- **Watertight 几何：** 通过 NeoSDK 的实体构建与适配工具，为适用零件构建和检查水密的物理几何。

**研究方向：physics-in-the-loop。** 将仿真反馈引入后续建模与优化，逐步构建可交互、simulation-ready 的场景。

## 开放计划

- [x] 项目主页与场景演示
- [x] NeoWorld Studio 与 NeoSDK 仓库介绍
- [ ] 项目代码，计划从 2026 年 9 月底起陆续开放
- [ ] MATRIX-Preview 预训练权重，计划从 2026 年 9 月底起陆续开放
- [ ] 论文与 arXiv 链接
- [ ] App Store 应用，即将发布（上架时间待定）

**MATRIX-Preview** 是我们面向场景重建的预训练视觉语言模型。Hugging Face 与 arXiv 链接将在可用后补充。

## 相关项目

[**NeoSDK**](https://github.com/NeoWorldProject/NeoSDK) 为重建流程提供几何构建与优化工具。

---

<p align="center"><a href="https://neoworldproject.github.io/Studio/">项目主页</a> · <a href="https://github.com/NeoWorldProject/NeoSDK">NeoSDK</a> · <a href="README.md">English</a></p>
