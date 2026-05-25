# Mentor Guidance Writer

这个 skill 的出发点很简单：以前老师会把论文改得满页红笔，很多问题会被一遍遍指出；现在这类高密度、一针见血的写作反馈越来越稀缺（导师也越来越忙，只在纸上留下稀疏的几个问号）。与其每次重新回忆那些零散的写作规范，不如把可复用的部分沉淀成一个可以调用、维护、迭代的 skill。

我把它理解为一种“导师经验的可移植封装”。它并不试图替代人的判断，也不承诺生成一份放之四海而皆准的神奇 prompt。它做的事情更朴素：把无线通信论文写作中那些重复出现、却又很容易漏掉的结构要求、术语约束、句法偏好和常见错误单独存起来，让 AI 在写作时先读这些，再动笔。

用袁老师的话说：“学术写作，80%都是八股文。” 相信大家写了1~2篇期刊论文后，也会深有同感。论文写作里确实有一部分是重复劳动。结构怎么搭，Introduction 怎样铺垫，系统模型该写到什么程度，首次出现的缩写怎么处理，图正文和 caption 怎样分工，哪些词一看就有 AI 腔。这些内容并不需要每次都从零开始发明。把它们做成 skill 的价值，不是为了偷懒，而是为了把注意力从重复召回转移到真正重要的判断上：问题是否成立，贡献是否清楚，证据是否充分，表达是否真的更好了。

## Package Tree

```text
.github/skills/mentor-guidance-writer/
├── SKILL.md
├── README.md
└── knowledge_base/
    ├── style_profile.md
    ├── outline_template.md
    ├── hard_memory.json
    ├── soft_memory.json
    └── error_log.md
```

## Knowledge Base Roles

### `style_profile.md`

这是高层写作风格文件。它回答的是“整体应该写成什么样”。这里面会规定段落逻辑、句式节奏、衔接方式、常用修辞动作，以及要主动回避的 AI 腔表达。它不是句子库，而是宏观风格的护栏。

例如：
`句首先承接上一句句尾已经引出的对象，再在句尾引出下一个对象，尽量形成 sentence-by-sentence handoff`

下面给出一个错误示例：
`Pilot-based CSI acquisition struggles to keep pace with the rapid variation of wireless channels. Channel knowledge maps (CKMs) have been proposed to address this problem. Propagation parameters such as path delays and angles are environment-specific and stable. Physical-layer processing can use these parameters to reduce reliance on pilots.`

以下是对错误示例的修改：
`Pilot-based CSI acquisition struggles to keep pace with the rapid variation of wireless channels. This rapid variation has, in recent years, motivated the introduction of channel knowledge maps (CKMs). A CKM stores environment-specific propagation parameters that remain stable over much longer timescales than the channel itself. These parameters can be queried in real time to bootstrap physical-layer processing, reducing its reliance on dense pilot transmission.`

### `outline_template.md`

这是结构模板文件。它回答的是“这类短文应该怎么搭”。对无线通信短文来说，这个文件很重要，因为如果没有明确的章节预算、段落范围和 word budget，模型很容易偷懒，本来该写成五页的内容最后只写出两页。这个模板默认贴近 IEEE Wireless Communications Letters 风格，但也可以继续扩展。

### `hard_memory.json`

这是硬记忆文件。它保存研究方向里的术语、单位、固定规则和硬约束，例如 CKM、RIS、MIMO、常见 performance metric、缩写首次出现规则、图表与篇幅限制等。它的任务是防止术语漂移、定义不稳和格式失控。

```text
示例
"term": "Channel knowledge map (CKM)",
"definition": "A location-indexed representation of channel-related knowledge that supports environment-aware wireless communication and sensing."
```

### `soft_memory.json`

这是软记忆文件。它和 `style_profile.md` 有交集，但分工不同。`style_profile.md` 更偏宏观，`soft_memory.json` 的信息会更加密集，关注的是“怎么把可读提升到易读，再提升到让人进入心流，停不下来”。比如句首承接旧概念、句尾引出新概念、怎样避免味同嚼蜡的平铺直叙。

```text
示例
"preferences": [
"Keep LaTeX output clean and minimal; avoid adding decorative formatting.",
"Use precise, common academic vocabulary and short, clear sentences.",
"Expand non-universal abbreviations at first mention using the full term followed by the abbreviation in parentheses.",
"Explain concepts close to where they appear to reduce confusion time.",
"Start each sentence by resolving the concept handed off by the previous sentence, then use the sentence ending to introduce the next local idea.",
"Prioritize logical coherence over ornate connectives.",
"Prefer plainer, mechanism-explicit wording when a compound phrase would otherwise sound opaque.",
"State core novelty early and align experiments with contribution claims.",
"Keep captions self-explanatory and place key explanations near figures/tables.",
"Replace ambiguous pronouns with explicit technical referents when several nouns compete as antecedents.",
"Use high-level taxonomy in subsection titles before introducing method-level detail.",
"When sibling subsections compare representative methods, title them on a shared axis such as prerequisite information, modeled object, or estimation target.",
"Check article choice deliberately for each countable noun phrase during revision.",
"After a motivating example or numerical result, begin the next paragraph by stating what the example established and why the next distinction or comparison is needed."
]
```

### `error_log.md`

这是给人复盘用的错题本，而不是强制喂给模型的主上下文。它记录的是那些在写作中反复踩坑的问题，例如词语搭配、指代歧义、句间衔接断裂、survey 分类轴不统一等。它的价值在于温故而知新，也方便后续把常见问题进一步抽象进风格或记忆文件。

## Two Main Usage Modes

### 1. 从零到一

适用于刚开始写短文、还没有成稿的情况。一个比较稳妥的做法是先选 5 篇左右参考论文，但不要只看引用量。高引用不等于写作一定最适合作为模板。有的论文措辞好，有的论文结构更强，有的论文图文呼应做得更干净。你可以自己先读，也可以让 AI 帮你打分，判断哪些文章更适合用来学习写法。第一次上手的朋友，建议先结合根目录的 [写作指引.md](../../../写作指引.md) 一起看，这样更容易先把短文的章节分工和写作顺序建立起来。

在这个模式下，建议优先使用 plan 模式。不同平台的命名可能不完全一样，有的叫 `plan`，有的叫 `grill me`，有的会表现成先给出执行方案再等待确认，但核心思想是一致的：先让 AI 给出它准备如何抽取这些论文中的写作规律、如何映射到当前 topic、哪些旧规则会保留、哪些新规则值得纳入 knowledge base，需要我们同意后，才能执行任务，我们也能和他迭代修改。这样可以防止模型为了追求局部顺滑，把已有知识库里真正重要的写作经验误删掉。

``` 使用示例
- `/mentor-guidance-writer 请仔细阅读我提供的论文，然后去完善knowledge base，关于knowledge base中的通用或共性写作方法，请保留。如果出现和我想要投递的IEEE Transactions on Wireless Communications期刊写作风格有冲突的地方（最有可能是outline_template.md），请将其删除，但是要提前告知我预计删除与修改哪些内容，待我同意后再执行。
```

### 2. 局部修改或润色

适用于你已经写了一部分，只想让 AI 结合 knowledge base 做定向改进，例如重写 Introduction 第二段、压缩 system model、补强 results 的解释句，或者检查某一节是否有明显 AI 腔。这个模式下不需要每次动知识库，但如果发现了反复出现的稳定问题，应该及时回写到 package 里。如果只是改部分措辞，并且你还没完全想清楚怎么改，也建议转移到网页版 AI 对话里多来回几轮，这样往往更有助于澄清需求，也更节约 token。

``` 使用示例
若处于论文前期的撰写（自身思路还不是太清晰、论文也相对粗糙的情况），可以用相对简洁的提示词：
- `/mentor-guidance-writer Draft a WCL-style introduction for wireless channel estimation from these five reference papers and show me a Writing_Plan first.`
- `/mentor-guidance-writer Revise my System Model and Results sections using the packaged knowledge base, but do not update the package itself.`
- `/mentor-guidance-writer 根据这个段落和两篇参考文献，帮我重写 Introduction 的第二段与第三段，并检查是否符合短文结构。`
- `/mentor-guidance-writer Update the packaged soft_memory.json and style_profile.md based on the writing preferences we confirmed today.`

若论文已达到及格线，即便你有了SKILL.md，还是要注意每次对话prompt的设计。根据我目前的试错，prompt写得比较好的情况下，可以相信AI修改的80%的地方。提示词写得不好的话，它会让你血压飙升。建议采用角色-任务-要求-参考资料的结构撰写：
- `/mentor-guidance-writer` 
角色：xx资深专家，擅长xx，精通xx（例如，你让AI帮你改算法中的公式推导，提升公式间的严谨性，你就让他精通XX方向的数学表达和逻辑推理）
任务：需要你帮助我xx，达到xx效果
具体要求：按以下顺序执行任务 1. xxx 2. xxx 3. xxx （例如1. 充分理解上下文 2. 分析结构，约束某些不能修改的地方（如某某公式、某些措辞、或传达的某些含义） 3. 定向优化xx ）
参考资料：草稿、可借鉴的其它论文段落、或者单独强调knowledge base里哪些规则需要特别遵守（如果你维护的knowledge base特别庞大，范围指定是有必要的）
输出：对应tex xx-xx行的修改
```

## How To Judge Whether The Revision Is Better

至少从两个层面判断。

第一层是结构。段落是否各司其职，Introduction 有没有把 motivation、gap、contribution 区分开，system model 有没有过长，method 和 results 有没有互相重复 framing。

第二层是语义与表达。句间衔接是否顺，指代是否清楚，术语是否稳定，句子是不是一上来就抛出新概念，是否混入了 AI 很喜欢但并不真正服务论证的词。结构问题可以更多依赖模板，语义问题则要靠 `error_log.md` 和持续复盘。

如果模型偷懒，最有效的方法通常不是加更多prompt，而是拆分任务。把“写完整篇论文”拆成“抽结构”“写四段式引言”“压缩 system model”“解释图 1 的主要趋势”这类粒度更小的子任务，通常更容易得到可控结果。

## Maintenance Guidance

- `style_profile.md` 适合收录稳定、可迁移的高层写作偏好。
- `outline_template.md` 适合维护某类 venue 的结构约束与 done criteria。
- `hard_memory.json` 适合放术语、单位、缩写、硬规则。
- `soft_memory.json` 适合放句级偏好、语气、衔接和 avoid list。
- `error_log.md` 适合收录反复出现、值得人回头看的错误。

这几个文件的目标不是越多越好，而是越稳定越好。只有当一条规则会反复影响后续写作时，才值得写进去。

## Scope

这个示例包当前聚焦于无线通信短文写作，尤其是 WCL 风格的结构化表达。它不是一个通用学术写作总框架，也不打算把所有场景都折叠进一个技能里。真正可持续的方式，是先把一个任务做好，再逐步派生出适合自己团队的版本。

## 推荐平台

VS Code、Cursor、Anti Gravity 和 Trae，基本都已经支持 skill 或类似工作流的调用。用这些平台的一个直接好处是，它们原生就支持修改前后版本的高亮对比，例如 diff、timeline、Git 历史等，这对写作任务尤其重要，因为很多时候你不是要看 AI 改没改，而是要判断它到底改好了没有。

另一个很实用的点是，这类 AI agent 通常已经可以直接读取 PDF、图片等材料，不需要我们再手动去装额外的 PDF 阅读插件，工作流会顺很多。对论文写作来说，这意味着你可以把参考论文、批注截图、公式图片、仿真图直接交给 agent，让它围绕同一套 knowledge base 工作。

如果你的 agent token 暂时不太够，或者你只是想先快速试一轮思路，也完全可以直接用网页版聊天。最简单的做法就是把这里的几个 markdown 或 json 文件直接丢给 AI，让它先读 knowledge base，再针对你的局部问题给出建议。skill 不是唯一入口，它只是把这些经验组织得更稳定、更便于复用。

## 写在最后

Karpathy 分享过一个值得我们警醒的判断：“You can outsource your thinking, but you can't outsource your understanding.” 换句话说，如果 AI 帮你改完一段话，你已经无法判断它是更好了还是更差了，这是一个危险信号，说明我们自己的审美和理解没有跟上。在 AI 时代，我们可以不再亲自做每一道繁琐工序，但仍然要做最后那个能分辨好坏的人。

从这个角度看，README 的重要性并不低于 SKILL.md。SKILL.md 更像一个可发布、可复用、可继续修改的示例；README 和写作指引真正想传达的，是如何逐渐形成你自己的判断标准。如果发现 AI 的某些修改你无法判断好坏，最好的办法往往不是继续堆 prompt，而是专门开一个新的session，围绕这一处问题反复追问，把它真正吃透理解透。

也向以下作者与项目致谢，它们分别从不同角度影响了这个SKILL的设计。
- ARIS 作者（GitHub 开源项目 Auto-claude-code-research-in-sleep）：<https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep>。推崇利用博弈论思想让科研工作自动化，可用于弥补该SKILL的不足。更具体而言，由于AI有掩盖自身的写作缺陷、迎合作者的倾向，易让作者陷入“当局者迷”的状态，导致一些问题（甚至是十分明显的问题）无法被发现。最简单的做法，就是另开一个网页对话，让另一个模型充当更苛刻的审稿人，对当前文章做压力测试，再把结果反馈给 writing agent。更自动化的做法，则是以 MCP 或类似方式接入另一类模型做外部评审。
- `AI-Vibe-Writing-Skills`：<https://github.com/donghuixin/AI-Vibe-Writing-Skills>。这个包及其 knowledge base 的提炼，受到了该项目的直接启发。

希望这个SKILL最终服务的，不仅是“更快地产出一篇像样的稿子”，更是“把重复劳动交给工具之后，把更多时间留给真正需要判断、审美和创造力的部分”。

欢迎大家共创，在Github上提issue。如果有直接针对skill的修改方案，能直接合并的话，也特别欢迎直接提PR。这个writing skill更新地越快，我们写作提效就会越快。
