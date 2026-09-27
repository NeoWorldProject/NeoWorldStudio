# NeoWorld-3: Agentic World Authoring with Tunable Geometry Programs

[简体中文](README_zh-CN.md) · [Project page and demonstrations](https://neoworldproject.github.io/Studio/) · [NeoSDK](https://github.com/NeoWorldProject/NeoSDK)

**NeoWorld Studio** is the application implementing the NeoWorld-3 framework. It
reconstructs objects and scenes from visual observations as tunable geometry
programs, retaining editable construction logic, named parameters, and part
structure alongside rendered previews and 3D assets.

> **Project introduction.** This edition contains documentation only. It does
> not include implementation source code or an installable application.

## From observations to editable worlds

NeoWorld-3 combines agentic construction with numerical refinement. Agents
inspect the observations, author a geometry program, render it, and revise its
structure. Geometry tools fit the program's exposed parameters and object
placements against the observed views. Shared parameters express relationships
between parts, preserving the dimensions and attachments encoded in the program.

The workflow connects three components:

| Component | Role |
| --- | --- |
| **NeoWorld Studio** | Coordinates object and scene reconstruction, task state, and user feedback. |
| **NeoMCP** | Exposes observation, source editing, rendering, measurement, and refinement as agent tools. |
| **[NeoSDK](https://github.com/NeoWorldProject/NeoSDK)** | Supplies geometry authoring, native execution, inspection, and parameter refinement. |

## Framework capabilities

- **Objects and compositional scenes.** Construct individual assets from visual
  references and assemble them into a shared scene. Local edits can update a
  part, an object, or its placement while retaining the surrounding construction.
- **Tunable geometry programs.** Keep construction, parameters, and placement
  explicit so structural editing and numerical fitting operate on the same
  editable representation.
- **Differentiable refinement.** Evaluate supported programs in a tensor geometry
  twin with batched rasterization. Native/twin consistency checks precede search;
  Blender materializes the baseline and selected candidates and provides native
  renders.
- **Geometry and articulation checks.** Inspect native geometry and proposed
  joint relationships. Configured physics feedback can propose bounded rigid
  corrections for subsequent geometry and visual checks.
- **Optional recursive self-improvement.** A research extension develops reusable
  tool candidates from completed-task traces. Candidates undergo development
  checks before entering a provisional library; ongoing tasks retain their fixed
  tool snapshot.

Scene delegation and metric-scale calibration remain experimental. Recursive
self-improvement is optional and disabled for ordinary tasks by default.
Articulation hypotheses depend on the available evidence; task completion and
geometric admission alone do not establish reconstruction quality or physical
validity.

## Explore the project

The [project page](https://neoworldproject.github.io/Studio/) presents the
framework, a scene reconstruction demonstration, and interactive articulated
assets. The object viewer demonstrates kinematics; it is not a physics
simulation.

[NeoSDK](https://github.com/NeoWorldProject/NeoSDK) describes the geometry toolkit
underlying the framework. This introduction does not announce a code-release
date.

## License

See [LICENSE](LICENSE) for the license accompanying this repository edition.
