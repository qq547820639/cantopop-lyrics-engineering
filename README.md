# 陈奕迅风格创作评价体系与实战手册

> 基于十三轮「评估-迭代-修正」实战闭环提炼\
> **版本 2.1** · 覆盖九大风格分支 · 十三首完整词作 · 462分天花板《天桥》\
> **NEW: 已封装为可交互 AI Skill，支持 ChatGPT / Claude / Cursor / Accio Work 等任意 AI 平台**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Made with Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)](https://www.markdownguide.org/)
[![Suno AI Ready](https://img.shields.io/badge/Suno-AI%20Ready-orange)](https://suno.ai)
[![AI Skill Ready](https://img.shields.io/badge/AI%20Skill-Ready-blueviolet)](#-快速开始作为-ai-skill-使用)

**维护者**：Peter.Pan\
**协作**：人类 × AI（十三轮评估-迭代-修正）\
**最后更新**：2026-04-11

---

## 📖 关于本项目

本项目将陈奕迅歌词中「只可意会」的创作密码，拆解为一套**可计算、可评估、可迭代**的工程化系统。

它有两种使用方式：

| 方式 | 说明 |
|------|------|
| **📚 作为手册阅读** | 直接阅读本 README，学习评分体系、风格分支、创作流程 |
| **🤖 作为 AI Skill 使用** | 将 `skill/` 目录喂给任意 AI，通过对话完成创作、评估、迭代（推荐） |

---

## 🚀 快速开始：作为 AI Skill 使用

### 适用平台

本 Skill 基于 pure Markdown 编写，**不依赖任何特定平台 API**，可用于所有支持自定义 Prompt / Knowledge Base 的 AI 工具：

| 平台 | 使用方式 |
|------|----------|
| **ChatGPT** | 创建 GPT → 将 `skill/` 下所有 `.md` 文件上传到 Knowledge |
| **Claude Projects** | 创建 Project → 将 `.md` 文件添加为 Project Knowledge |
| **Cursor / Windsurf** | 将 `skill/` 目录放入项目，作为 `.cursorrules` 或上下文引用 |
| **Accio Work** | Agent → Skills → 安装 `skill/` 目录 |
| **其他 AI** | 将 `skill/SKILL.md` 内容粘贴为 System Prompt，按需附加 `references/` 文件 |

### 安装步骤

```bash
# 1. 克隆仓库
git clone https://github.com/qq547820639/cantopop-lyrics-engineering.git

# 2. Skill 文件在 skill/ 目录下
ls skill/
# SKILL.md                    ← 主文件（工作流 + 核心法则）
# references/scoring-system.md ← 十四维度 + 数学模型
# references/style-branches.md ← 九大风格 + Style Prompt
# references/advanced-rules.md ← 高阶法则
# references/suno-guide.md     ← Suno 生成技巧
# references/case-studies.md   ← 十三首案例
# references/appendix.md       ← 诊断卡 + 声调表 + 词库

# 3. 按你使用的 AI 平台，将这些文件上传/导入即可
```

> **Tip**：如果你的 AI 平台有上下文长度限制，优先上传 `SKILL.md`（核心），再按需添加 `references/` 下的文件。

### 四大交互模式

#### 模式一：从零创作

给 AI 一个画面或感觉，它会按六阶流程帮你完成一首 450+ 的完整词作。

```
你说：帮我写一首关于深夜便利店的粤语歌
你说：写一首陈奕迅风格的歌，关于地铁最后一班车
你说：我想写一首关于旧手机的歌
```

**AI 输出**：完整歌词 + Suno Style Prompt + 十四维度评分卡 + 四变量数学参数

#### 模式二：评估打分

把你写好的歌词发给 AI，获得精确的量化评估。

```
你说：帮我评分这首歌词：[贴上你的歌词]
你说：这首词像不像陈奕迅风格？
```

**AI 输出**：十四维度逐项打分 + PAC/TSMI/NSRQ/C3AC 四变量分析 + Top 3 改进建议

#### 模式三：迭代改进

在评估基础上逐项修正，每轮展示分数变化。

```
你说：帮我把这首歌从 430 分提到 450+
你说：Bridge 太弱了，帮我改
你说：Hook 声调不对，帮我换一个
```

**AI 输出**：定位扣分点 → 逐项修正 → 前后对比 → 重新评分

#### 模式四：Suno 输出

生成可以直接复制到 [Suno](https://suno.ai) 使用的完整内容。

```
你说：帮这首歌生成 Suno prompt
你说：我想在 Suno 上生成一首 Funky 中板的粤语歌
```

**AI 输出**：Style Prompt（黄金公式）+ 带元标签的歌词 + 动态标注

### 创作流程示意

```
种子（画面+物象+情感落点）
  ↓
风格选择（九大风格分支决策树）
  ↓
结构搭建（三段式骨架）
  ↓
歌词填充（写动作不写情绪）
  ↓
声调协音检查
  ↓
动态弧线标注
  ↓
数学模型自检（PAC/TSMI/NSRQ/C3AC）
  ↓
修正 → 重新计算 → 输出
```

---

## 📂 项目结构

```
cantopop-lyrics-engineering/
├── README.md                              ← 你正在读的文件（完整手册）
└── skill/
    ├── SKILL.md                           ← 主文件：四大模式工作流
    └── references/
        ├── scoring-system.md              ← 十四维度评分标准 + 四变量数学模型
        ├── style-branches.md              ← 九大风格分支 + Style Prompt 模板
        ├── advanced-rules.md              ← 高阶法则：寄生三形态、呼吸量、识穿→认领弧线
        ├── suno-guide.md                  ← Suno 元标签速查、黄金公式、常见问题
        ├── case-studies.md                ← 十三首案例（种子→迭代→总分）
        └── appendix.md                    ← 快速诊断卡 + 评分卡模板 + 声调表 + 词库
```

---

## 🎯 核心内容速览

| 模块 | 内容 |
| :------- | :--------------------------------------------------------------------------- |
| 十四维度评价体系 | 主题选择、物化意象、叙事细节、动词精准、粤语口语、Hook设计、结构建筑、Bridge设计、尾奏处理、演唱质感、编曲配置、留白负空间、声调协音、动态弧线 |
| 四变量数学模型 | PAC（寄生系数）、TSMI（声调匹配）、NSRQ（呼吸量）、C3AC（副歌3弧线完成度） |
| 九大风格分支 | 慢歌钢琴 / Funky冷感 / 摇滚撕裂 / Synth-pop / 电子实验 / 民谣叙事 / 暗黑电子 / 歌剧管弦乐 / R&B Soul |
| 十三首完整词作 | 每首含 Style Prompt、动态标注、迭代记录，最高分462《天桥》 |
| Suno生成指南 | 元标签速查、常见问题、黄金Style公式 |

### 十三首词作总览

| 词作 | 风格 | BPM | Hook | TSMI | C3AC | 总分 | 迭代 |
| :--- | :-------- | :-- | :--- | :--- | :---- | :------ | :- |
| 波子跌落 | 慢歌钢琴 | 68 | 波子敢敢 | 8 | 1.3 | 450 | 2 |
| 双蓝剔 | Funky中板 | 110 | 双蓝剔 | 12 | 0(特例) | 450 | 1 |
| 暖柜 | 慢歌钢琴 | 68 | 暖柜门 | 19 | 1.5 | 461 | 3 |
| 裂镜 | 摇滚撕裂 | 70 | 裂镜 | 14 | 1.3 | 445 | 2 |
| 收唔到掣 | Synth-pop | 138 | 收唔到掣 | 21 | 1.5 | 461 | 2 |
| 嘟声 | Funky中板 | 110 | 嘟一声 | 18 | 1.5 | 452 | 3 |
| 31 | Funky中板 | 110 | 31 | 12 | 1.2 | 458 | 3 |
| 房卡 | 电子实验 | 105 | 房卡 | 7.2 | 1.2 | 458 | 4 |
| 琴键 | 民谣叙事 | 70 | 琴键 | 12 | 1.2 | 459 | 3 |
| 体温正常 | 电子实验 | 105 | 体温正常 | 14.4 | 1.5 | 460 | 3 |
| 超载 | 暗黑电子 | 70 | 超载 | 16.8 | 1.5 | 460 | 3 |
| 画面 | 电子实验 | 105 | 画面 | 13.2 | 1.0 | 458 | 3 |
| 天桥 | 歌剧管弦乐 | 70 | 天桥 | 17.6 | 1.2 | **462** | 3 |

---

## 目录

1. [十四维度评价体系](#一十四维度评价体系)
2. [四变量数学模型](#二四变量数学模型)
3. [九大风格分支体系](#三九大风格分支体系)
4. [高阶法则深挖](#四高阶法则深挖)
5. [Suno生成实战技巧](#五suno生成实战技巧)
6. [实战六阶流程](#六实战六阶流程)
7. [十三首案例全记录](#七十三首案例全记录)
8. [附录：快速诊断卡与评分表](#附录)

---
## 一、十四维度评价体系

