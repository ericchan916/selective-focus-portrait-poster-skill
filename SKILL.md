---
name: selective-focus-portrait-poster
description: 选择性对焦编辑人像海报：画面大部分人像柔焦/轻微运动模糊/降饱和，只有一个焦点区域（横向清晰切片 / 浮动对焦窗 / 竖向清晰切片 / 偏移对焦框）回到锐利真实，配中性色场 + 唯一强调色与杂志级编辑字体，生成一张 9:16 写实人像海报。当用户提到"对焦人像海报 / 选择性对焦 / 焦点人像 / FOCAL IDENTITY / selective focus poster"时使用。Use when the user asks for a selective-focus editorial portrait poster or a FOCAL IDENTITY-style poster — produces one realistic magazine-grade portrait where blur and sharpness direct the eye, with a neutral field plus one accent color.
license: MIT
---

# 选择性对焦编辑人像海报 · Selective Focus Portrait Poster

模糊让人退后，清晰让人看见：焦点就是叙事。
Blur pushes back, sharpness pulls in — focus is the story.

## 输入 · Inputs

```
Series Name:   e.g. FOCAL IDENTITY
Main Title:    e.g. MOTION / OBSERVE / SIGNAL / FRAME
Subject:       age, gender, identity, profession
Name:
Role:
Key Line:      short, concept-driven sentence
Accent Color:  yellow / red / cobalt blue / rust orange
Focus Method:  horizontal sharp slice / floating focus window /
               vertical sharp slice / offset focus frame
Aspect Ratio:  9:16 (default)
```

## 使用规则 · Agent rules
- **不要追问，不输出分析 / Never ask, never show analysis.**
- 缺失字段协调补全：Subject、Role、Key Line 与 Main Title 指向同一概念；Focus Method 与 Accent Color 选最契合概念的一种；Series Name 缺省 FOCAL IDENTITY；画幅缺省 9:16。
- **人物身份**：未提供 Name 时虚构一个自然的名字；除非用户本人明确提供，**不描绘、不命名任何真实可识别的人物**。Use a fictional name if none is given; never depict or name a real identifiable person unless the user supplies it.
- 只输出一张海报；环境不能生图时，输出已填好的 [prompt.md](prompt.md) 提示词。

示例见 [examples/subjects.md](examples/subjects.md)。

## 核心规则 · Core rules

### 写实人像 · Realistic portrait
自然皮肤纹理、毛孔、细微瑕疵、可信的头发、真实面部结构。避免塑料皮肤、CGI 光滑感、重度美颜、千篇一律的商业模特造型。

### 选择性对焦 · Selective focus
- 人像大部分柔和模糊、轻微运动柔化、降饱和或减少细节。
- 只有 Focus Method 指定区域回到锐利细节、自然肤色、清晰纹理。
- 清晰与模糊区域必须完美对齐，是同一个人、同一瞬间；不出现重复眼睛、第二张脸或贴图感。

### 对焦结构 · Focus methods
| Method | 描述 |
|---|---|
| horizontal sharp slice | 横穿双眼的清晰横带 |
| floating focus window | 小型浮动窗口，隔离面部局部 |
| vertical sharp slice | 穿过运动模糊的窄竖向清晰切片 |
| offset focus frame | 较大的偏移框，把注意力从面部中心移开 |

### 色彩 · Color — Neutral Field + One Accent Color
- 克制中性色：炭灰、灰、暖米、灰白、自然肤色。
- Accent Color 是唯一的强调色，只用于对焦线框、主标题和少量关键细节。

### 字体 · Typography
- Main Title：高对比编辑衬线体。
- Name、Role：窄体粗无衬线。
- 次要信息：小号中性无衬线。
- Key Line：与人物和概念相关、有意义的文案。

### 构图与质感 · Composition & finish
- 不对称构图，大量负空间；人像、字体与对焦几何相互作用。
- 细微胶片颗粒、轻扫描质感、克制的印刷肌理；一件完整的编辑作品。
- 气质：精致的独立时尚 / 摄影 / 音乐 / 文化杂志海报；由模糊与清晰控制视线。

### 避免 · Avoid
赛博朋克 HUD、过多 UI 图形、霓虹渐变、乱码、logo、水印、编号、闪光符号、生硬高斯模糊、五官融化、重复五官、塑料皮肤、过度修图。
