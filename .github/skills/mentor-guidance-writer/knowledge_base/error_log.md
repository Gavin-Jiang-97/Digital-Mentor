# Error Log

- **[Date] Error Type**:
  - ❌ **Wrong**:
  - ✅ **Right**:
  - 🔒 **Instruction**:

- **[2026-03-10] AI 风格词汇与机械过渡**
  - ❌ **Wrong**: 段首使用 “Furthermore / Moreover / Additionally / In conclusion”
  - ✅ **Right**: 通过复用上段关键词与论点自然承接段落
  - 🔒 **Instruction**: Never start a paragraph with mechanical transitions; prefer keyword linking.

- **[2026-03-10] 夸张形容词与副词**
  - ❌ **Wrong**: 使用 “paramount / crucial / revolutionary / vital” 等情绪化词
  - ✅ **Right**: 使用客观、可验证的描述（数据、约束、方法）
  - 🔒 **Instruction**: Replace hyperbolic modifiers with precise, objective phrasing.

- **[2026-03-10] 绝对化断言**
  - ❌ **Wrong**: “This proves that...”
  - ✅ **Right**: “These findings suggest... / The data indicates...”
  - 🔒 **Instruction**: Default to academic hedging; avoid absolute claims.

- **[2026-03-10] 僵尸名词（Nominalizations）**
  - ❌ **Wrong**: “perform an evaluation of...” 等 -tion/-ment/-ance 名词化堆砌
  - ✅ **Right**: 使用主动动词（evaluate, analyze, compare）
  - 🔒 **Instruction**: Prefer active verbs; reduce nominalizations.

- **[2026-03-10] 领域外隐喻/行话**
  - ❌ **Wrong**: “orthogonal” (物理/数学), “leverage” (商业), “ecosystem” (生物)
  - ✅ **Right**: 使用本领域等效词（independent, apply, system/environment）
  - 🔒 **Instruction**: Use plain English unless a term is defined in-domain.

- **[2026-03-10] 高频 AI 味词**
  - ❌ **Wrong**: delve / tapestry / testament / multifaceted / fosters / in summary / to summarize
  - ✅ **Right**: examine/investigate/explore/analyze；network/complex system/combination；demonstrates/highlights/shows；complex/varied/layered；promotes/encourages/builds；直接结论句
  - 🔒 **Instruction**: Search and replace these terms; delete rigid summary openers.

- **[2026-03-23] 破折号长句**
  - ❌ **Wrong**: 用破折号在一句中连续插入补充说明，造成层级堆叠
  - ✅ **Right**: 改写为从句、并列句，或拆成两句并保持自然衔接
  - 🔒 **Instruction**: Avoid em-dash-heavy sentences in manuscript prose; split or reframe the sentence instead.

- **[2026-03-23] 冒号句式过多**
  - ❌ **Wrong**: 用冒号生硬地引出解释、列表或结论
  - ✅ **Right**: 用自然句法承接说明，如 which / including
  - 🔒 **Instruction**: Minimize colon-led prose; prefer natural continuation in academic English.

- **[2026-03-23] consume/consumes 用词不当**
  - ❌ **Wrong**: the physical layer consumes pilots; the map consumes priors
  - ✅ **Right**: the physical layer uses pilots; the map relies on priors; the algorithm incorporates prior information
  - 🔒 **Instruction**: Do not use consume/consumes for signals, priors, maps, or algorithms in wireless-communication writing.

- **[2026-03-26] Em-dash compound modifiers**
  - ❌ **Wrong**: delay--angle support, birth--death status, time--frequency observations
  - ✅ **Right**: delay and angle support, birth/death status, time-frequency observations (use en-dash only in ranges like pp.~10--27)
  - 🔒 **Instruction**: Replace em-dash compound modifiers with "and", "/", or single hyphen. Reserve en-dashes for numeric ranges.

- **[2026-03-26] Overclaiming with "substantially" / "significantly" / "confirms"**
  - ❌ **Wrong**: "substantially reduces overhead", "significantly outperforms", "simulations confirm its effectiveness"
  - ✅ **Right**: "can reduce overhead", "can outperform", "simulation results suggest"
  - 🔒 **Instruction**: Hedge unsupported quantitative claims. Use "can", "suggest", "indicate" unless citing exact numerical evidence.

- **[2026-03-26] Duplicate/near-duplicate sentences**
  - ❌ **Wrong**: "Deep-learning-based approaches offer another avenue. Deep-learning-based approaches also provide a promising alternative."
  - ✅ **Right**: "Data-driven approaches offer another avenue."
  - 🔒 **Instruction**: After drafting, run a near-duplicate sentence check; remove or merge repetitions.

- **[2026-03-26] Missing word-boundary spaces in LaTeX prose**
  - ❌ **Wrong**: "conditionaldiffusion", "channelparameters", "and , so"
  - ✅ **Right**: "conditional diffusion", "channel parameters", "and so"
  - 🔒 **Instruction**: Proofread for missing spaces and stray punctuation after each draft pass.

- **[2026-03-26] "symbiotic" / "bridge" metaphor overuse**
  - ❌ **Wrong**: Using "symbiotic loop", "bridge", "bridging" repeatedly across subsections
  - ✅ **Right**: "mutual dependence", "missing middle layer", "mutually reinforcing relationship"
  - 🔒 **Instruction**: Limit each metaphor to one occurrence per manuscript. Rotate phrasing.

- **[2026-03-26] Research-proposal tone in magazine articles**
  - ❌ **Wrong**: Detailed algorithmic formulation (Bayesian hierarchical models, deep unfolding layers) presented as proposals in magazine prose
  - ✅ **Right**: Briefly mention algorithmic classes as examples; focus on the problem structure, the mutual dependence, and open questions
  - 🔒 **Instruction**: In IEEE WCM magazine articles, keep co-design sections at the conceptual/directional level. Reserve algorithmic detail for journal papers.

- **[2026-04-09] 模糊代词 it / they 指代不清**
  - ❌ **Wrong**: 在前文连续出现多个技术名词后继续使用 "it" / "they"，导致读者无法快速判断指代对象
  - ✅ **Right**: 当先行词不唯一时，直接重复具体对象，如 the quasi-static map / the base station / the terminal position
  - 🔒 **Instruction**: Replace ambiguous pronouns with explicit technical referents whenever multiple candidate antecedents appear nearby.

- **[2026-04-09] 非并列对象上的搭配不当**
  - ❌ **Wrong**: "CSI acquisition cannot keep pace with the dimensionality increase and dynamics of next-generation channels"
  - ✅ **Right**: "CSI acquisition scales poorly with the growing dimensionality and rapid variation of next-generation channels"
  - 🔒 **Instruction**: Do not use rate-matching phrases such as "keep pace with" when the compared technical objects are not parallel agents or processes.

- **[2026-04-09] Survey 标题层级过细**
  - ❌ **Wrong**: 用实现细节直接给 survey 小节命名，先暴露具体技术而没有先给出分类层次
  - ✅ **Right**: 先按信息条件、建模方式或问题设定给出高层分类，再在正文中引入具体算法
  - 🔒 **Instruction**: In survey sections, title subsections by high-level taxonomy before naming specific methods or models.

- **[2026-04-09] Section opening 与首个 subsection 重复 framing**
  - ❌ **Wrong**: section 第一段和第一个 subsection 重复解释同一动机或同一 closed-loop 关系
  - ✅ **Right**: 将高度重复的 framing 合并为一到两段连续叙述，再进入具体子问题
  - 🔒 **Instruction**: Merge overlapping section-level and subsection-level framing when they serve the same narrative purpose.

- **[2026-04-27] 缩写首次出现未给全称**
  - ❌ **Wrong**: 直接写 CKM / RT-GSHCM / STO，而前文尚未展开其全称
  - ✅ **Right**: 先写 channel knowledge map (CKM)；首次出现其他非通用缩写时同样先给全称
  - 🔒 **Instruction**: Expand each non-universal abbreviation at first mention, then introduce the abbreviation in parentheses.

- **[2026-04-27] 词组搭配不透明，读者无法据词面理解机制**
  - ❌ **Wrong**: stochastic refinement
  - ✅ **Right**: model refinement, followed by an explicit explanation that measured data are used to calibrate parameters in the statistical model
  - 🔒 **Instruction**: If a compound term does not communicate the mechanism on its own, replace it with a plainer head noun and explain the update or inference mechanism explicitly.

- **[2026-04-27] 重复或重叠的近义表达并列**
  - ❌ **Wrong**: moving objects or dynamic-environment conditions
  - ✅ **Right**: moving objects
  - 🔒 **Instruction**: Do not stack overlapping nouns or modifiers when one term already captures the intended factor.

- **[2026-04-27] 介词搭配不能准确表达技术关系**
  - ❌ **Wrong**: Relative to the quasi-static map; Relative to the physical layer
  - ✅ **Right**: Based on the quasi-static map; To assist the physical layer
  - 🔒 **Instruction**: Choose prepositions that match the actual technical relation, such as basis, assistance, conditioning, source, or target.

- **[2026-04-27] 标签过于抽象，不能准确命名技术关系**
  - ❌ **Wrong**: This intermediate role gives rise to two paradigms.
  - ✅ **Right**: This intermediate role leads to two interaction patterns between dynamic CKM construction and physical-layer processing.
  - 🔒 **Instruction**: Prefer labels that explicitly name the technical relation or comparison axis; avoid abstract nouns that add little information.

- **[2026-04-27] 对比措辞削弱了真正想强调的差异**
  - ❌ **Wrong**: provides additional value beyond the quasi-static CKM alone
  - ✅ **Right**: provides value beyond the quasi-static CKM alone
  - 🔒 **Instruction**: In contrastive claims, avoid modifiers that unintentionally weaken the main distinction unless incremental framing is intended.

- **[2026-04-27] 表格或二元对比中的命名不对仗**
  - ❌ **Wrong**: 用 grid-based 对比一个不在同一命名轴上的说法
  - ✅ **Right**: 使用成对命名，例如 grid-based / grid-less
  - 🔒 **Instruction**: When two concepts are compared side by side, keep the labels parallel so that the contrast axis is immediately visible.

- **[2026-04-27] 冠词选择未经检查**
  - ❌ **Wrong**: 修改句子后忽略 a/an、the 或零冠词，导致泛指与特指混乱
  - ✅ **Right**: 根据首次引入、唯一性和泛指/特指关系逐一确认每个可数名词短语的冠词
  - 🔒 **Instruction**: Review article choice for every countable noun phrase, especially after rewrites that change modifiers or specificity.

- **[2026-04-28] 句首抛出未铺垫的新概念**
  - ❌ **Wrong**: Weak, spatially diffuse co-link interference is suppressed by subspace projection.
  - ✅ **Right**: This hierarchy follows the different spatial structures of the two interference types. Because co-link interference is generated by neighboring uplink users and arrives through rich-scattering paths, it is usually weaker and more spatially diffuse. Such interference is therefore better suppressed by subspace projection.
  - 🔒 **Instruction**: Start each sentence from the concept handed off by the previous sentence instead of introducing an unanchored new concept at the opening.

- **[2026-04-28] 单句同时引入过多新概念**
  - ❌ **Wrong**: 在一个句首同时引入干扰类型、空间特征和处理方法，让读者一次性消化多个新对象
  - ✅ **Right**: 先交代干扰来源和结构特征，再在后一句引出相应处理方法；必要时拆成多个短句
  - 🔒 **Instruction**: If a sentence would introduce several new concepts at once, split it so each sentence carries one local handoff.

- **[2026-05-04] 同级 survey 子节标题比较轴不统一**
  - ❌ **Wrong**: Scatterer-Position-Conditioned Generation / Measurement-Guided Hybrid Modeling / RF/Pose-Aware Bayesian Inference
  - ✅ **Right**: Known Dynamic-Scatterer Positions for Generative Map Construction / Measurement-Guided Hybrid Modeling of Quasi-Static and Dynamic Clusters / Limited-Pilot-Driven Multi-Factor Dynamic Channel Estimation
  - 🔒 **Instruction**: When sibling survey subsections compare representative approaches, title them on the same axis. If method names alone are not sufficiently parallel, retitle them by prerequisite information, modeled objects, or estimation target.

- **[2026-05-04] 子节标题与正文采用不同分类标准**
  - ❌ **Wrong**: 标题强调一组比较轴，但正文开头改用另一组不对应的区分方式
  - ✅ **Right**: 标题确定比较轴后，正文首句和次句立即解释该标题对应的前提条件、对象或估计目标
  - 🔒 **Instruction**: Keep title and body on the same comparison axis; restate that axis in the opening sentences of the subsection.

- **[2026-05-10] 动机例子后缺少目的句**
  - ❌ **Wrong**: 上一段刚给出数值例子或现象验证，下一段就直接切入相邻概念，读者看不出为什么此处要做概念辨析
  - ✅ **Right**: 先用一句话说明前一个例子已经证明了什么，再交代接下来为什么需要做概念区分或范围澄清
  - 🔒 **Instruction**: After a motivating example, begin the next paragraph with a purpose sentence that states what the example established and why the following clarification is needed.

- **[2026-05-10] 仿真图正文重复 caption 中的配置**
  - ❌ **Wrong**: caption 已经给出阵列规模、频率、scatterer 数量等设置，正文仍重复这些配置细节
  - ✅ **Right**: 将系统配置和参数设置集中写入 caption，正文只解释比较对象、主要趋势和工程含义
  - 🔒 **Instruction**: For simulation figures, let captions carry the configuration and keep the main text focused on comparison, trend, and implication.

- **[2026-05-15] 动词型谓语与主语不一致（subject-verb agreement）**
  - ❌ **Wrong**: "Next-generation wireless communications evolves toward..."
  - ✅ **Right**: "Next-generation wireless communication is evolving toward..."
  - 🔒 **Instruction**: When the subject is a singular uncountable noun such as "wireless communication" or "research", use a singular verb; avoid adding plural -s to the noun to patch agreement.

- **[2026-05-15] 状语结构语法断裂**
  - ❌ **Wrong**: "These signals are transmitted at periods of 5--160 ms and matching the millisecond-to-second variation timescale"
  - ✅ **Right**: "These signals are transmitted at periods of 5--160 ms, matching the millisecond-to-second variation timescale"
  - 🔒 **Instruction**: When appending a participial phrase, use a comma and a gerund (matching), not a coordinating conjunction (and) with a present participle.

- **[2026-05-15] 名词短语缺少必要冠词**
  - ❌ **Wrong**: "dynamic channel component becomes poorly identifiable"
  - ✅ **Right**: "the dynamic channel component becomes poorly identifiable"
  - 🔒 **Instruction**: Unique technical noun phrases referring to a specific object already introduced in context require the definite article "the".

- **[2026-05-15] 非并列对象的 but 结构语法错误**
  - ❌ **Wrong**: "Such interference exhibits moderate power but broadly spread in the angular domain."
  - ✅ **Right**: "Such interference exhibits moderate power and is broadly spread across the angular domain."
  - 🔒 **Instruction**: When "but" connects two predicates, both must be grammatically parallel (verb phrase vs. verb phrase). Replace with "and is" when the second element needs its own copula.

- **[2026-05-15] 被动语态目的补语错误**
  - ❌ **Wrong**: "what RF biases require compensated"
  - ✅ **Right**: "what RF biases require compensation"
  - 🔒 **Instruction**: The verb "require" takes a noun or gerund object, not a past participle. Use "require compensation" or "need to be compensated".

- **[2026-05-20] 动词原意-引申义失配：用描述路径偏离的词描述两个不同对象的不一致**
  - ❌ **Wrong**: "the map prior may deviate from the instantaneous channel"
  - ✅ **Right**: "the map prior may mismatch the instantaneous channel"
  - 🔒 **Instruction**: *deviate* literally means a single trajectory drifting from its own course (one object, two time points). When the sentence describes a mismatch between two distinct objects (e.g., a map prior vs. a channel), use *mismatch*, *diverge from*, or *no longer align with*. Before choosing a verb, ask: (a) what is the verb's core image—one object drifting, or two objects failing to match? (b) does the sentence's subject-object structure fit that image? If the subject and object are different entities, *deviate* is wrong.