# Suno 生成实战技巧

## Style Prompt 黄金公式

**人声 + 年代风格 + BPM + 核心乐器 + 节奏模式 + 演唱技法 + Bridge/Outro特殊处理 + 情绪底色 + Hook特殊处理**

### 公式分解

| 元素 | 说明 | 示例 |
|------|------|------|
| 人声 | 语言+性别+音色 | `Cantonese male warm baritone` |
| 年代风格 | 风格定位 | `piano ballad` / `1985 Hong Kong disco` / `electronic experimental` |
| BPM | 速度锁定 | `68 BPM unhurried breathing` / `138 BPM` |
| 核心乐器 | 主要乐器配置 | `ONLY felt piano soft pedal` / `synth arpeggios and pulse beats` |
| 节奏模式 | 节奏特征 | `syncopated electric guitar strumming` / `four-on-the-floor kick` |
| 演唱技法 | 人声处理 | `slightly breathy intimate, conversational phrasing behind beat` |
| Bridge/Outro | 特殊段落处理 | `bridge all instruments cut to bare voice` |
| 情绪底色 | 整体情绪 | `urban melancholy` / `existential dread underneath` |
| Hook处理 | Hook特殊标注 | `repeat hook three times` |

---

## 元标签速查表

| 标签 | 功能 | 示例 |
|------|------|------|
| `[Intro]` | 前奏段落 | `[Intro]` |
| `[Verse]` | 主歌 | `[Verse 1]` |
| `[Pre-Chorus]` | 预副歌 | `[Pre-Chorus]` |
| `[Chorus]` | 副歌 | `[Chorus]` |
| `[Bridge]` | 桥段 | `[Bridge]` |
| `[Outro]` | 尾奏 | `[Outro]` |
| `[Build]` | 逐渐推进 | `[Build]` |
| `[Drop]` | 副歌爆发 | `[Drop]` |
| `[All instruments cut]` | 乐器骤停 | `[All instruments cut]` |
| `[Whisper]` | 低语 | `[Whispered]` |
| `[Voice cracks]` | 声线破裂 | `[Voice cracks on "X"]` |
| `[Long pause]` | 长停顿 | `[Long pause]` |
| `[Silence]` | 沉默 | `[Long silence]` |
| `{Sound of X}` | 环境音效 | `{Sound of one handclap}` |

### 动态标注标签

| 标签 | 动态级别 |
|------|----------|
| `[Very Soft]` | 极轻（主歌1） |
| `[Building]` | 渐强（预副歌） |
| `[Released But Held Back]` | 释放但克制（副歌1） |
| `[Slightly Heavier]` | 稍重（主歌2） |
| `[Building Stronger]` | 更强推进（预副歌2） |
| `[More Released]` | 更放（副歌2） |
| `[Naked Voice]` | 裸声（Bridge） |
| `[Full Voice, Cracks Open]` | 全开破音（副歌3） |
| `[Silence]` | 沉默（尾奏） |

---

## 常见问题及解决

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| 生成偏慢 | BPM未锁定 | Style最前加 `138 BPM very fast` |
| 人声不够冷 | 未标注冷感 | 加 `cold detached tone, dead inside` |
| Bridge乐器未撤干净 | 标签不够强 | 改为 `[No instruments, only kick drum]` |
| Hook重复不够 | 未标注重复 | 加 `repeat hook three times` |
| 尾奏未全停 | 未标注骤停 | 加 `[Complete silence]` |
| 粤语发音不准 | Suno对粤语支持有限 | 在Style加 `Cantonese pronunciation` |
| 动态变化不明显 | 标注不够密 | 每段都加动态标签 |
| 编曲太满 | 未限制乐器 | 用 `ONLY` 和 `NO` 强制限制 |

---

## 完整 Style Prompt 示例

### 慢歌钢琴（68 BPM）
```
Cantonese male warm baritone piano ballad, 68 BPM unhurried breathing, urban melancholy, natural vocal grain, slightly breathy intimate, conversational phrasing behind beat, restrained storytelling, zero auto-tune, bridge all instruments cut to bare voice, final chorus voice cracks then falls to breath, ONLY felt piano soft pedal throughout, NO drums bass strings synths.
```

### Funky中板（110 BPM）
```
Cantonese male vocal funky mid-tempo, 110 BPM, syncopated electric guitar strumming, walking bassline, tight crisp drums with rim clicks, acid-jazz inflection, warm baritone half-spoken half-sung, cold detached tone even when playful, funky groove but vocal is dead inside, bridge all instruments cut to single synth pulse and naked voice, NO big vocal belting, everything restrained and ironic.
```

### 歌剧管弦乐（70 BPM）
```
Cantonese male vocal orchestral ballad, 70 BPM with dramatic dynamic range, full string orchestra, grand piano, cinematic percussion, baritone voice from intimate whisper to operatic crescendo, theatrical staging feel, Hungarian cimbalom and glockenspiel accents, bridge all instruments cut to solo cello and naked voice, final chorus voice cracks then swallowed by swelling strings, tragic grandeur, NO electronic beats, ONLY orchestral instruments.
```
