# Style Profile

## Source Corpus

- Default transfer venue: IEEE Wireless Communications Magazine.
- Compression mode: compress to IEEE Wireless Communications Letters only when the user explicitly requests letter-style condensation.
- Transfer principle: keep the references' clean technical exposition, taxonomy discipline, and forward-looking discussion, with a default magazine-style posture and letter-style compression only when explicitly requested.

## Core Style DNA

- **Tone**: Formal, technical, evidence-bound, and forward-looking. Sound confident about the setup and restrained about the claims.
- **Narrative Posture**: Start from a concrete wireless-system problem, expose why existing practice is insufficient, then introduce the proposed mechanism as the natural response to that gap.
- **Macro Structure**: Motivation -> precise gap -> proposed idea/framework -> implementation or estimation method -> evidence/results -> takeaway and boundary conditions.
- **Abstract Pattern**: One sentence on context, one sentence on the gap, one or two sentences on the method, one sentence on the key finding, one sentence on why the finding matters for wireless systems.
- **Introduction Pattern**: Broad 6G/wireless motivation first, then a sharper problem statement, then the limitation of existing approaches, then the paper's contribution, then a short roadmap only if needed.
- **Section Pattern**: Each section should answer one question. Example: What is the problem? Why is it hard? What is the proposed answer? Why does it work? What do the results imply?
- **Paragraph Logic**: Topic sentence states the local claim. The next sentence explains why that claim matters. Middle sentences supply mechanism, contrast, or evidence. The closing sentence hands one keyword or tension to the next paragraph.
- **Sentence Pattern**: Prefer medium-length sentences with one main clause and one supporting clause. Use shorter sentences to land key claims. Reserve long sentences for taxonomy or tightly coupled technical conditions.
- **Lexical Preference**: Use precise verbs such as enable, characterize, reveal, quantify, facilitate, mitigate, predict, generalize, reconstruct, and validate. Prefer plain technical nouns over fashionable buzzwords.
- **Evidence Framing**: Numerical observations should be interpreted, not merely reported. After each key result, add one sentence explaining what the result means for deployment, estimation, robustness, or complexity.
- **Figure/Table Narration**: Introduce each figure with the question it answers; discuss the dominant trend, the comparison baseline, and the engineering implication. For simulation figures, place configuration details in the caption and keep the body focused on interpretation.

## Flow and Coherence Rules

- Use keyword echoing between adjacent sentences and paragraphs. The ending of one sentence should plant a concept that the next sentence opens and develops.
- Do not open a sentence by throwing in a new concept with no local anchor. Start from the concept handed off by the previous sentence, then use the sentence ending to introduce the next concept.
- If a sentence would need to introduce several new concepts at once, split it into two or more sentences so the handoff remains explicit.
- Prefer semantic transitions over stock connectives. Good bridges include: "This mismatch motivates...", "That limitation becomes critical when...", "With this representation in place...", "The same observation also affects..."
- When explaining a concept, method, or phenomenon, end the current unit with the unresolved consequence and begin the next unit by resolving it.
- After a motivating example or numerical result, open the next paragraph by stating what that example has established and why the following distinction, definition, or comparison is needed.
- Keep one visible logic chain per paragraph: claim -> reason -> mechanism/evidence -> implication.

## English Rendering Rules for Chinese Source Material

- Translate ideas, not sentence shells. Rewrite Chinese source material into idiomatic academic English instead of preserving Chinese syntax.
- Replace parataxis-heavy Chinese phrasing with explicit English logic markers such as contrast, cause, concession, and implication.
- Convert broad Chinese summaries into concrete English claims with subject, action, condition, and implication.
- Avoid literal translations of promotional phrasing. Rewrite into reviewer-facing technical language centered on assumptions, mechanisms, and evidence.
- Prefer concise English clause structure over stacked modifiers.

## Preferred Rhetorical Moves

- Define the object before evaluating it.
- Contrast the proposed method against the most relevant baseline immediately after introducing the method.
- Use case-driven motivation in the introduction when possible, especially for wireless channel prediction, CKM construction, channel estimation, and physical-layer signal processing.
- State limitations in the same section where benefits are claimed.
- End the conclusion with scope and next-step implications, not slogans.

## Safe Phrase Bank

- "This article investigates..."
- "The key difficulty lies in..."
- "This observation motivates..."
- "To address this issue, we..."
- "The resulting framework enables..."
- "Numerical results indicate that..."
- "The gain is most pronounced when..."
- "This behavior suggests that..."
- "These results support the use of..."

## Do's (我要的风格)

- 变换句式节奏：关键结论用短句强调，复杂论述用长句展开。
- 使用学术性限定：These results indicate / This behavior suggests / The gain becomes evident when ...
- 注入具体性：给出场景、变量、约束、比较基线、数量级。
- 首次出现的非通用缩写先给出全称，再在括号中引入缩写，例如 channel knowledge map (CKM)。
- 用上一句或上一段的关键词承接下一句或下一段，形成环环相扣的结构。
- 对非技术概念使用简明英文表达，对技术概念使用标准术语。
- 在提出优势后立刻补充适用条件、复杂度代价或边界情形。
- 保持段落首句可独立成立，让审稿人快速抓住该段主旨。
- 不用破折号承载额外说明。
- 优先用自然衔接改写冒号句式，让解释顺着前一句展开。
- 描述图谱、信号和先验的使用关系时，优先用 use / rely on / incorporate / provide 等领域常见表达。
- 当前句附近存在多个技术名词时，优先用明确名词替换 it / they，避免指代歧义。
- 描述系统压力和规模增长关系时，优先用 scale poorly with / challenge / limit / complicate 等直接搭配。
- 如果 section opening 与第一个 subsection 的功能高度重复，合并成一到两段连续叙述，避免重复 framing。
- 如果几个代表性方法的 scope 明显不对等，不要为了形式对称强行拆成等权子节；优先合并铺垫性工作，再把覆盖范围更广的方法作为主体展开。
- 如果词组本身不能清楚说明机制，优先使用更直白的中心词，再补充说明其如何校准、推断或更新。
- 需要命名两种交互关系、两类方法或两列对比项时，优先使用能直接反映技术关系且形式对仗的名称。
- 描述方法适用场景时保持并列句法，明确 each method is suitable for 的条件，而不是只堆叠方法名。
- 如果同级 survey 子节仅用方法名难以形成清晰并列，优先改用共享比较轴命名，例如 available side information、modeled objects 或 estimation targets。
- 子节标题确定比较轴后，正文开头两句要立刻复现这一比较轴，而不是换成另一套分类标准。
- 对每一个可数名词短语都主动检查 a/an、the 或零冠词是否最符合该处的特指性和泛指性。
- 介词要准确表达技术关系，例如 based on, to assist, conditioned on, inferred from，而不是使用语义松散的 relative to。
- 句首先承接上一句句尾已经引出的对象，再在句尾引出下一个对象，尽量形成 sentence-by-sentence handoff。
- 如果一句话要同时抛出多个新概念，优先拆句，而不是把多个新对象堆在一个句首。

## Don'ts (我不要的风格)

- 用偏口语化的表达，例如leaves performance on the table
- 段首机械过渡词堆叠 Moreover / Additionally
- 夸张形容词与副词：paramount / revolutionary / groundbreaking / vital。
- 绝对化结论：This proves that... / This guarantees...
- 僵尸名词泛滥（-tion/-ment/-ance 名词化过多）。
- 领域外隐喻和商业化表达：leverage / ecosystem / game-changer / next-generation solution。
- 高频 AI 味词：delve / tapestry / testament / multifaceted / fosters / in summary / to summarize。
- 中文直译式英语，如长串并列、主语缺失、抽象空泛总结句。
- 用破折号插入次级解释，导致一句承载过多层级信息。
- 用冒号硬切分论点与解释，导致句子显得生硬。
- 用 keep pace with 描写 CSI 获取、算法能力与信道维度或动态之间的非并列关系。
- 用较生僻的动词如 strain 描写无线系统瓶颈，如果 challenge / limit / complicate 更直接。
- 当前文有多个候选先行词时仍连续使用 it，造成指代不明。
- 用过细的实现级标题对 survey 类方法分类，掩盖更高层的 taxonomy。
- 用不透明、机制不明的搭配，例如 stochastic refinement，而不说明如何利用实测数据校准模型参数。
- 用 overlapping 的近义表达堆叠一个因素，例如 moving objects or dynamic-environment conditions。
- 用抽象但信息量低的标签概括具体技术关系，例如在这里只存在两种 interaction patterns 时写成 paradigms。
- 在需要突出核心区分时用会削弱对比力度的修饰语，例如 additional value。
- 句首直接抛出尚未由上文铺垫的新概念，导致句间衔接生硬。
- 在一句中同时引入多个新概念，导致读者需要边读边回填逻辑链。
- 同级子节标题混用输入条件、方法机制和建模因素，导致读者无法一眼看出比较轴。
- 标题按一套标准命名，而正文开头又切换成另一套分类依据，导致 title-body mismatch。
- 用动词时先问它的核心意象是否与句子的主宾结构匹配。例如，*deviate* 意指一个对象偏离自身轨迹（单主体、两时间点），不能用于描述两个不同对象之间的不一致；此时应换用 *mismatch*。