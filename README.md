# NeoWorld Studio

Agentic Reconstruction of Editable 3D Objects and Scenes

[Project page & demos](https://neoworldproject.github.io/Studio/) · [English](#english) · [中文](#中文)

<p>
  <a href="https://github.com/NeoWorldProject/NeoWorldStudio">GitHub</a> &nbsp;·&nbsp;
  <span>arXiv · Coming soon</span> &nbsp;·&nbsp;
  <span>Hugging Face · Coming soon</span>
</p>

## English

NeoWorld Studio combines initial reconstruction with agentic refinement to build editable 3D objects and scenes from visual observations.

For each object, we first create an initial reconstruction, or t0. An agent then compares rendered views with the observations and calls NeoSDK’s geometry optimization tools to refine the object’s shape and structure.

At scene scale, we begin with an initial reconstruction of the environment and its object layout. Once the objects have been reconstructed, we assemble them into the scene and use scene-level visual feedback to further refine geometry, placement, and their fit within the surrounding environment.

### Availability

Our repositories are open now with README previews. We plan to progressively release project code and pretrained weights for MATRIX-Preview, our vision-language model for scene reconstruction, starting in late September 2026.

[NeoSDK](https://github.com/NeoWorldProject/NeoSDK) is our geometry toolkit. The paper and model download links will be added when available.

## 中文

NeoWorld Studio 将初始重建与智能体驱动的迭代优化相结合，从视觉观测中构建可编辑的三维物体与场景。

对于每个物体，我们先生成初始重建结果 t0，再由智能体对照渲染视图与原始观测，调用 NeoSDK 的几何优化工具，逐步优化物体的形状与结构。

在场景层面，我们首先建立环境与物体布局的初始重建。物体重建完成后，将它们装配回场景，再结合场景级视觉反馈，进一步调整几何、摆放及其与周围环境的匹配。

### 开放计划

项目仓库现已公开，目前提供 README 介绍。我们计划从 2026 年 9 月底开始，陆续开放项目代码，以及用于场景重建的预训练视觉语言模型 MATRIX-Preview 的权重。

几何工具集详见 [NeoSDK](https://github.com/NeoWorldProject/NeoSDK)。论文与模型下载链接将在可用后补充。
