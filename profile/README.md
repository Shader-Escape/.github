# TheExit

[中文](#中文)

**Visual helper mods** and **Iris shader packs** don't get along. Schematic overlays, selection boxes and similar rendering break or disappear once a shader pack is on, so players end up choosing between a **good looking world** and **usable tools**.

**TheExit** is a community effort to remove that choice. It is built on **EXIT (Emergency Exit)**, a rendering library that lets a mod's world rendering skip the shader pack. EXIT draws that content into its own target with vanilla shaders and, once the shader pack has finished the frame, merges it back by depth. 

How one frame works, with real captures from BSL, Kappa and Super Resolution: 
https://shader-escape.github.io/emergency-exit/render-scale/

## Repositories

| Repository | What it is |
|---|---|
| [emergency-exit](https://github.com/shader-escape/emergency-exit) | The EXIT library. Minecraft 1.16.5 to 26.3, one branch per version. Fabric on every version, NeoForge on newer ones. CC0 |
| [litematicapass](https://github.com/shader-escape/litematicapass) | Shader compatibility for Litematica, where EXIT's approach was first worked out. It has its own copy of the rendering and doesn't depend on EXIT yet. Latest release [1.1.2](https://github.com/shader-escape/litematicapass/releases/tag/1.1.2) covers 1.21.1 to 26.3; 1.16.5 to 1.20.6 are in [1.1.0-1.20.6-1.16.5](https://github.com/shader-escape/litematicapass/releases/tag/1.1.0-1.20.6-1.16.5) |

Each addon gives one existing mod an exit by wrapping its rendering in EXIT. The list grows as people pick up mods.

## How to help

- Test. Try the shader packs and mods you already use, and report what works and what doesn't. You don't need to write code.
- Write an addon for a mod you use. Open an issue first so two people don't take the same mod. AI assistance is allowed.
- Request a mod you'd like covered.

<!-- Discord link -->

AI helped with parts of EXIT's development, mostly porting to older Minecraft versions under rules the author wrote. The design and the decisions are human, and every version is tested. Contributors may use AI too, as long as they can explain their changes and say in the pull request what the AI did.

## 中文

可视化/辅助模组一直难以和 Iris光影 一起使用。投影、选区框这类渲染一开光影就显示错乱，玩家只能在**美好的画面**和**实用的工具**之间二选一。

**TheExit** 是一个社区项目，旨在让大家不用再选。它基于 EXIT（应急出口）：一个让模组的世界渲染绕开光影包的库。EXIT 用原版着色器把这些内容画进自己的目标，等光影画完这一帧，再按深度合回画面。

一帧里具体发生了什么（BSL、Kappa、Super Resolution 的实际截图）：https://shader-escape.github.io/emergency-exit/render-scale/

### 仓库

| 仓库 | 内容 |
|---|---|
| [emergency-exit](https://github.com/shader-escape/emergency-exit) | EXIT 库本体。Minecraft 1.16.5 到 26.3，每个版本一个分支。所有版本支持 Fabric，较新的版本还支持 NeoForge。CC0 |
| [litematicapass](https://github.com/shader-escape/litematicapass) | Litematica 的光影兼容模组，EXIT 的做法最早就是在这里摸索出来的。它自带一份渲染实现，目前还不依赖 EXIT。最新版 [1.1.2](https://github.com/shader-escape/litematicapass/releases/tag/1.1.2) 支持 1.21.1 到 26.3；1.16.5 到 1.20.6 见 [1.1.0-1.20.6-1.16.5](https://github.com/shader-escape/litematicapass/releases/tag/1.1.0-1.20.6-1.16.5) |

每个附属模组负责一个现有模组，把它的渲染交给 EXIT。每有人认领一个模组，这里就多一行。

### 怎么参与

- 测试：用你平时的光影和模组试一下，协助我们发现问题。你不需要会写代码。
- 写附属模组：给你常用的模组写一个。动手前先开 issue 认领，避免撞车。允许AI辅助编写。
- 提需求：告诉我们你想让哪个模组接上。

EXIT 的开发中用到了 AI，主要是按作者制定的规则把它移植到旧版本。设计和决定都由人来做，每个版本都经过测试。贡献者也可以用 AI，只要能解释自己的改动，并在 PR 里写明 AI 做了哪些部分。
