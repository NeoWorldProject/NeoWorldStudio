<h1 align="center">NeoWorld Studio</h1>

<p align="center"><strong>White-Box, Agentic Reconstruction of Interactive 3D Worlds</strong></p>

<p align="center">
  <a href="https://neoworldproject.github.io/Studio/"><img src="assets/project-page.svg" alt="Project page and demos"></a>
  <img src="assets/arxiv-soon.svg" alt="arXiv: coming soon">
  <img src="assets/models-soon.svg" alt="Hugging Face: coming soon">
  <img src="assets/app-store-soon.svg" alt="App Store: coming soon">
</p>

<p align="center"><strong>English</strong> · <a href="README_zh-CN.md">简体中文</a></p>

> **Research preview.** This repository currently contains the project introduction. Code and **MATRIX-Preview** weights are planned for progressive release from **late September 2026**.

<p align="center">
  <a href="https://neoworldproject.github.io/Studio/#demos">
    <img src="assets/scene-preview.jpg" width="800" alt="Scene reconstruction preview: original capture on the left, Blender reconstruction on the right.">
  </a>
</p>
<p align="center"><sub>Original capture (left) · Reconstruction rendered in Blender (right)</sub><br><a href="https://neoworldproject.github.io/Studio/#demos"><strong>Watch the scene demo →</strong></a></p>

## Overview

NeoWorld Studio takes a **white-box** approach to building editable, interactive 3D objects and scenes. VLM agents author explicit geometry and refine it through NeoSDK tools, **without relying on pretrained 3D generation models**.

Geometry programs, part structure, and refinement steps remain explicit, interpretable, and editable. Reconstruction is not tied to a pretrained 3D generator's learned shape space: new objects can be addressed through explicit modeling and tool-based refinement.

### Objects: initialize, observe, refine

For each object, we first create an initial reconstruction, or **t0**. An agent then compares rendered views with the observations and calls [NeoSDK](https://github.com/NeoWorldProject/NeoSDK)'s geometry optimization tools to refine the object's shape and structure.

### Scenes: initialize, assemble, refine

At scene scale, we begin with an initial reconstruction of the environment and its object layout. Once the objects have been reconstructed, we assemble them into the scene and use scene-level visual feedback to further refine geometry, placement, and their fit within the surrounding environment.

## Toward Interactive, Simulation-Ready Scenes

- **Articulated motion:** configure movable joints, their axes, and motion ranges to create objects with controllable articulation.
- **Physics, part by part:** assign physical parameters at the part level, including density, with mass and inertia derived from geometry.
- **Watertight geometry:** use NeoSDK's solid construction and adaptation tools to build and inspect watertight physical geometry for suitable parts.

**Research direction: physics-in-the-loop.** We are extending this foundation so simulation feedback can inform subsequent modeling and optimization toward interactive, simulation-ready scenes.

## Release Roadmap

- [x] Project homepage and scene demo
- [x] NeoWorld Studio and NeoSDK repository introductions
- [ ] Project code, progressively from late September 2026
- [ ] MATRIX-Preview pretrained weights, progressively from late September 2026
- [ ] Paper and arXiv link
- [ ] App Store app, coming soon (release date to be announced)

**MATRIX-Preview** is our pretrained vision-language model for scene reconstruction. The Hugging Face and arXiv links will be added when available.

## Related Project

[**NeoSDK**](https://github.com/NeoWorldProject/NeoSDK) provides the geometry construction and optimization tools used in the reconstruction workflow.

---

<p align="center"><a href="https://neoworldproject.github.io/Studio/">Project page</a> · <a href="https://github.com/NeoWorldProject/NeoSDK">NeoSDK</a> · <a href="README_zh-CN.md">简体中文</a></p>
