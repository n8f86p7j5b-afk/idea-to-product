# 想法成型 (Idea to Product)

把"我想试试"变成"明天就能动手验证"的产品包。

Turn "I want to try" into a product package you can verify tomorrow.

---

## 这是什么 / What is this

这是一个 **跨 agent 通用** 的 skill，通过 6-8 轮渐进对话，帮你把一个模糊的想法变成一份清晰、可验证的产品设计文档 + MVP 验证方案。

This is a **cross-agent** skill that turns a fuzzy idea into a clear product design document + MVP verification plan through 6-8 rounds of progressive conversation.

**它不是审核工具，是 helper。** 你不需要证明这个想法"值得做"。哪怕只服务自己、哪怕只是好奇，都足够充分。

**It's not a gatekeeper, it's a helper.** You don't need to prove your idea is "worth doing." Even if it's just for yourself or pure curiosity, that's enough.

---

## 谁适合用 / Who is this for

- 有想法但不会写 PRD 的**普通人**（HR、老师、医生、销售…任何领域专家）
- 想快速验证想法的**创业者/产品经理**
- 好奇 "AI 能不能帮我做产品" 的**AI 爱好者**

- Regular people with ideas but no PRD-writing experience
- Entrepreneurs and PMs who want to validate ideas quickly
- AI enthusiasts curious about "can AI help me build a product"

---

## 核心特点 / Key Features

### 1. 三档专业度自适应 / 3-Tier Adaptivity

| 档位 / Tier | 适合谁 / For | 产出物 / Output |
|------------|-------------|----------------|
| **小白档 / Beginner** | 第一次想产品的人 | 思路整理卡（故事化、无术语） |
| **中档 / Intermediate** | 有一定了解的人 | 轻量产品包（结构化 PRD + 验证方案） |
| **熟练档 / Advanced** | 产品经理、创业者 | 专业级 PRD/MRD（含竞品分析、技术选型、成本估算） |

Skill 会从你第一句话自动判断档位，并**明牌告诉你**。随时可调。

The skill auto-detects your level from your first sentence and **tells you openly**. Adjust anytime.

### 2. 真正的人性化引导 / Truly Human-Centered

不是把产品经理面试题换成轻松的词，而是**从人性角度出发**：

- 不问"你要帮谁解决问题"，问"这个想法跟你自己的生活有什么联系"
- 不问"砍掉功能"，问"你最想先试试哪部分"
- 允许"我就是好奇想试试"

Not rephrasing PM interview questions in casual tone, but **starting from human nature**:
- Not "who are you helping" but "how does this connect to your life"
- Not "cut features" but "what do you want to try first"
- "I'm just curious" is totally valid

### 3. 技术选型具体到个人 / Concrete Tech Choices for Individuals

中档和熟练档会给出**具体、现实**的技术建议：

- 个人PC跑不了24小时？→ 推荐 Vercel/腾讯云（含免费额度说明）
- 不懂后端？→ 推荐无代码/低代码方案
- 预算有限？→ 给出最低成本起步方案

Intermediate and advanced tiers provide **concrete, realistic** tech recommendations:
- Personal PC can't run 24/7? → Vercel/Cloud (with free tier details)
- No backend skills? → No-code/low-code alternatives
- Limited budget? → Minimum-cost starting plans

### 4. 验证 Prompt 包 / Verification Prompt Pack

产出的产品包里包含 5 个可直接使用的 AI 验证 prompt：

1. **用户访谈模拟** / User Interview Simulation
2. **价值主张压力测试** / Value Proposition Stress Test
3. **原型描述生成**（用于 AI 画图）/ Prototype Description (for AI image generation)
4. **竞品速查** / Competitor Quick Scan
5. **低保真原型草图** / Lo-fi Prototype Sketch
   - 多模态 LLM → 直接画给你看 / Multimodal LLM → draws it for you
   - 纯文本 LLM → 文字描述布局 / Text-only LLM → describes layout in text

### 5. 明确 AI 边界 / Clear AI Boundaries

从第一句话就告诉你 AI 能做什么、不能做什么：

- ✅ AI 可以：理清思路、写文案、出主意、模拟对话
- ❌ AI 不能：判断真实市场需求、替代真实用户反馈、做最终决策

AI boundaries are set from the first sentence:
- ✅ AI can: organize thoughts, write copy, brainstorm, simulate conversations
- ❌ AI cannot: judge real market demand, replace real user feedback, make final decisions

### 6. 跨 Agent 通用 / Cross-Agent Universal

一个 `SKILL.md` 文件，不依赖任何平台特性：

- Claude Code ✅
- Cursor ✅
- Kimi / 豆包 / 通义千问 ✅
- Trae / Windsurf / 任何 LLM agent ✅

One `SKILL.md` file, no platform lock-in.

---

## 怎么用 / How to Use

### 显式调用 / Explicit
```
/想法成型
idea-to-product
run idea-to-product
```

### 隐式触发 / Implicit
说出你的想法即可：
- "我想做一个..."
- "我有个想法..."
- "帮我设计..."

Just describe your idea:
- "I want to build a..."
- "I have an idea..."
- "Help me design..."

---

## 引导链 / Conversation Flow

| 轮次 / Round | 主题 / Topic |
|-------------|-------------|
| 1 | 破冰 + 专业度嗅探 / Icebreaker + Level Detection |
| 2 | 想法缘起 / Idea Origin |
| 3 | 你和想法的关系 / Your Relationship with the Idea |
| 4 | 最期待的画面 / The Vision |
| 5 | 真实的驱动力 / True Motivation |
| 6 | 从哪里开始试 / Where to Start |
| 7 | 验证方案设计 / Verification Plan |
| 8 | 打包输出 / Package Output |

**专家快速通道 / Express Mode**：如果你已经想得很清楚，可以直接说"给我专业版"或"跳过引导"，skill 会直接进入产出。

**Express Mode**: If you've already thought it through, say "give me the pro version" or "skip the guide" to jump straight to output.

---

## 文件结构 / File Structure

```
idea-to-product/
├── SKILL.md          # 核心 skill 文件 / Core skill file
└── README.md         # 本文件 / This file
```

---

## 设计哲学 / Design Philosophy

1. **鼓励表达，绝不审核** / Encourage expression, never gatekeep
2. **加法思维，不浇冷水** / Additive thinking, no cold water
3. **三档各有真实深度** / Every tier has real depth
4. **工具国内优先** / China-accessible tools by default
5. **用户主权** / User agency
6. **明确 AI 边界** / Clear AI boundaries

---

## 适用场景 / Use Cases

- 有个模糊念头，想理清楚到底是什么
- 想验证想法是否可行，不想直接投入开发
- 需要一份轻量 PRD 给合作者看
- 好奇 "AI 能不能帮我做产品"

- You have a fuzzy idea and want to clarify it
- You want to validate before building
- You need a lightweight PRD for collaborators
- You're curious "can AI help me with products"

---

## 标签 / Tags

`skill` `prompt-engineering` `product-design` `ai-agent` `mvp` `prd` `no-code` `low-code` `idea-validation` `ai-tools`

---

## 反馈 / Feedback

用过之后觉得哪里不顺、哪个引导语别扭、哪个产出物缺东西，欢迎反馈。

After using it, if something feels off, a prompt feels awkward, or an output is missing something, feedback is welcome.

---

> **AI 是副驾驶，不是飞行员。用它加速思考，但不要让它代替你思考。**
>
> **AI is a co-pilot, not the pilot. Use it to accelerate thinking, but don't let it replace your thinking.**
