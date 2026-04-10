---
name: cantopop-lyrics
description: >
  Eason Chan (陈奕迅) style Cantonese lyrics creation, evaluation, and iteration system.
  Use when the user wants to write Cantopop lyrics, evaluate existing Cantonese lyrics,
  generate Suno AI style prompts for Cantonese songs, or iterate on lyrics quality.
  Trigger phrases: "写粤语歌词", "陈奕迅风格", "Cantopop lyrics", "粤语填词",
  "评分歌词", "score lyrics", "Suno粤语", "写歌", "填词", "Hook设计",
  "声调协音", "物化意象", "Cantonese songwriting", "广东歌", "粤语歌",
  "evaluate my lyrics", "improve my lyrics", "Suno style prompt Cantonese".
---

# 陈奕迅风格粤语歌词创作 Skill

基于十三轮「评估-迭代-修正」实战闭环提炼的工程化创作系统。
将「只可意会」的创作密码拆解为可计算、可评估、可迭代的参数系统。

**满分 470 · 十四维度 · 四变量数学模型 · 九大风格 · Suno 可执行**

---

## 能力范围

| 模式 | 说明 |
|------|------|
| **创作模式** | 从种子画面出发，六阶流程完成一首 450+ 歌词 |
| **评估模式** | 十四维度 + 四变量模型精确打分，定位扣分点 |
| **迭代模式** | 针对诊断结果逐项修正，每轮提升 5-15 分 |
| **Suno 输出** | 生成可直接复制到 Suno 的 Style Prompt + 带元标签歌词 |

---

## 核心工作流

### 模式一：从零创作

按六阶流程执行，每阶完成后向用户确认：

#### 第一阶：种子（用户输入）
向用户确认三个要素：
1. **画面**：一个让你心里一紧的日常瞬间
2. **物象**：画面中的具体物件（情感锚点）
3. **情感落点**：一个动作，不给答案

如果用户只给了模糊方向，帮助提炼出具体的物象。参考案例库中的种子设计（见 `references/case-studies.md`）。

#### 第二阶：结构搭建
根据情感属性选择风格分支（见 `references/style-branches.md`），搭建三段式骨架：

```
主歌1（场景）→ 副歌1（点题）→ 主歌2（加深）→ 副歌2（强化）
→ Bridge（骤停转折）→ 副歌3（升华/认命）→ 尾奏（留白）
```

标注每段功能 and 目标动态。

#### 第三阶：歌词填充
核心法则：
- **只写动作不写情绪**：写「手指悬在半空收回」，不写「我很犹豫」
- **动词暴力精准**：每首至少一个让人心头一紧的动词（搣、攥、渗、㩒）
- **物象动作链**：核心物象必须有完整动作链（出现→接触→转折→落点）
- **被动发现**：主歌中至少一个「被动发现」瞬间（非「我谂起」式主动反思）
- **粤语口语**：句式短促有切分感，使用纯正粤语词（㩒、闩、咗、啲、嚟、佢、冇、喺、畀）

Hook 设计（见 `references/scoring-system.md` 维度六）：
- 字数 ≤ 4 字
- 重复 ≥ 4 次，每次有情绪递进
- 尾字声调与风格匹配（慢歌用阴上/阴平，快歌用入声/阴去）

#### 第四阶：声调协音检查
逐句检查尾字声调，确保 Hook 与风格匹配。
参照 `references/scoring-system.md` 维度十三和 `references/appendix.md` 声调速查表。

#### 第五阶：动态弧线标注
逐段标注：`[Very Soft]` → `[Building]` → `[Released But Held Back]` → `[More Released]` → `[Naked Voice]` → `[Full Voice, Cracks Open]` → `[Silence]`

#### 第六阶：数学模型自检与修正
计算四个变量（见 `references/scoring-system.md` 数学模型部分）：
1. **PAC**（寄生动作链系数）：< 3.0 标红修正
2. **TSMI**（声调-风格匹配度）：< 0 标红修正
3. **NSRQ**（负空间呼吸量）：< 2.5 标红修正
4. **C3AC**（副歌3双阶弧线完成度）：< 0.5 标红修正

修正后重新计算 TEE（总情感能量函数）。

### 最终输出格式

```
## 《歌名》

**风格**：[风格分支]
**BPM**：[数值]
**Hook**：[Hook词] （[声调分析]）
**物象**：[核心物象]
**动作链**：[动作1] → [动作2] → [动作3] → [落点]

### Style Prompt（直接复制到 Suno）
[完整 Style Prompt]

### 歌词（带元标签和动态标注）
[Intro]
...
[Verse 1]
[Very Soft]
...

### 评分卡
| 维度 | 满分 | 得分 | 备注 |
|------|------|------|------|
| ... | ... | ... | ... |
| **总分** | **470** | **[X]** | |

### 数学模型参数
- PAC = [X]
- TSMI = [X]
- NSRQ = [X]
- C3AC = [X]
- TEE = [X]
```

---

### 模式二：评估现有歌词

当用户提供歌词要求评分时：

1. 读取 `references/scoring-system.md` 获取完整评分标准
2. 逐维度打分，标注具体扣分原因
3. 计算四变量数学模型
4. 使用快速诊断卡（见 `references/appendix.md`）做最终检查
5. 给出分级：450-470 封神级 / 400-449 优秀级 / 350-399 合格级 / <350 需大幅改进
6. 列出 Top 3 改进优先级

---

### 模式三：迭代修正

当用户要求改进现有歌词时：

1. 先用模式二评估，定位扣分点
2. 按优先级排序修正：C3AC > PAC > TSMI > NSRQ
3. 每次修正后重新评分，展示分数变化
4. 迭代直到目标分数

---

### 模式四：Suno 输出

当用户只需要 Suno 相关内容时：

1. 读取 `references/suno-guide.md` 获取完整 Suno 技巧
2. 组装 Style Prompt（黄金公式：人声 + 年代风格 + BPM + 核心乐器 + 节奏模式 + 演唱技法 + Bridge/Outro处理 + 情绪底色 + Hook处理）
3. 添加元标签到歌词
4. 检查常见问题（BPM锁定、冷感标注、Bridge乐器撤干净等）

---

## 参考文件索引

| 文件 | 内容 |
|------|------|
| `references/scoring-system.md` | 十四维度评分标准 + 四变量数学模型（PAC/TSMI/NSRQ/C3AC/TEE） |
| `references/style-branches.md` | 九大风格分支 + Style Prompt 模板 + 风格-声调咬合矩阵 |
| `references/advanced-rules.md` | 高阶法则：寄生动作链三形态、负空间呼吸量模板、识穿→认领双阶弧线 |
| `references/suno-guide.md` | Suno 元标签速查、Style Prompt 黄金公式、常见问题解决 |
| `references/case-studies.md` | 十三首完整案例（种子、物象、Hook、Bridge、迭代记录、总分） |
| `references/appendix.md` | 一页纸快速诊断卡、十四维度评分卡模板、粤语声调速查表、十三首参数总览 |

**使用时按需读取参考文件，不要一次性全部加载。**

---

## 关键法则速记

1. **写动作不写情绪**
2. **物象必须有动作链**（出现→接触→转折→落点），且至少一个节点「寄生」到人
3. **Hook ≤ 4字，重复 ≥ 4次**，尾字声调与风格匹配
4. **Bridge = 全曲最脆弱处**：乐器骤停、裸声、一个画面、不解释
5. **副歌3必须完成「识穿→认领」弧线**
6. **尾奏 = 一个动作 + 沉默**，不给答案
7. **粤语口语底色**：读出来像一个人在说话
8. **动词暴力精准**：㩒、搣、攥、渗、抰、揿
