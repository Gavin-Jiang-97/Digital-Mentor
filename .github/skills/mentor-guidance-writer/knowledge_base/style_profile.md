# Style Profile

This file owns prose style, rhetorical choices, and user writing preferences. See `memory.md` for terminology and technical conventions.

## Core Style DNA

- **Tone**: Formal, technical, evidence-bound, and forward-looking.
- **Abstract Pattern**: One or two sentence on context, one sentence on the gap, main body for the method, one sentence for simulation results.
- **Paragraph Logic**: Topic sentence states the local claim. The next sentence explains why that claim matters. Middle sentences supply mechanism, contrast, or evidence. The closing sentence hands one keyword or tension to the next paragraph.
- **Sentence Pattern**: Prefer medium-length sentences with one main clause and one supporting clause. Use shorter sentences to land key claims.
- **Lexical Preference**: Use precise verbs such as enable, characterize, reveal, facilitate, mitigate, predict, generalize, reconstruct, and validate. Prefer plain technical nouns over fashionable buzzwords.
- **Figure/Table Narration**: Introduce each figure with the question it answers; discuss the dominant trend, the comparison baseline, and the indication/suggestion. For simulation figures of magzine, place configuration details in the caption and keep the body focused on interpretation. For simulation figures of letter or journal, place configuration details at the beginning of the simulation section.


## Writing Preferences（写作风格）

**采用的风格**

- 用上一句或上一段句尾的关键词或概念承接下一句或下一段，再在句尾引出下一个对象，形成 sentence-by-sentence handoff。解释概念、方法或现象时，让下一个论述单元接着解释上一个单元留下的结果或问题。
- 用明确的语义关系衔接，例如 This mismatch motivates...、That limitation becomes critical when...、With this representation in place...、The same observation also affects...，代替段首机械堆叠 Moreover / Additionally。
- 将中文材料的思想重写为自然的学术英语，把并列堆叠的表述改写为明确的对比、因果或推论关系，补全主语，并将抽象空泛的总结写具体。
- 使用简洁的英语分句结构，减少修饰语堆叠；一句话需要引入多个新概念时，拆成两句或多句，让每一步承接清楚。
- 对非技术概念使用简明英文表达（simple first），对技术概念使用标准术语。
- 保持段落首句可独立成立，让审稿人快速抓住该段主旨。
- 用自然衔接改写冒号句式，让解释顺着前一句展开。
- 当前句附近存在多个技术名词时，用明确名词替换 it / they，消除指代歧义。
- 描述系统压力和规模增长关系时，优先用 scale poorly with / challenge / limit / complicate 等直接搭配；当这些表达更清楚时，用它们替换较生僻的词语，例如 strain。
- 几个代表性方法的 scope 明显不对等时，合并铺垫性工作，把覆盖范围更广的方法作为主体展开，按内容分配篇幅。
- 使用能说明机制的直白中心词，再解释其如何校准、推断或更新。例如，将不透明的 stochastic refinement 改写为明确说明如何利用实测数据校准模型参数的表述。
- 命名交互关系、方法或对比项时，使用能直接反映技术关系且形式对仗的名称。例如，仅有两种交互关系时，用 interaction patterns 表述，而不笼统称为 paradigms。
- 同级 survey 子节采用统一的高层比较轴，再展开实现细节；标题确定比较轴后，正文开头两句立即复现这一比较轴。
- 对每一个可数名词短语检查 a/an、the 或零冠词是否符合该处的特指性和泛指性。
- 选择动词时检查其核心意象与主宾结构是否匹配。描述两个对象之间的不一致时，优先用 mismatch，而不用表示单一对象偏离自身轨迹的 deviate。

**避免的风格**

- 偏口语化的表达，例如 leaves performance on the table。
- 夸张形容词与副词，例如 paramount / revolutionary / groundbreaking / vital。
- 绝对化结论，例如 This proves that... / This guarantees...。
- 领域外隐喻和商业化表达，例如 ecosystem / game-changer / next-generation solution。
- 高频 AI 味词，例如 coupling。
- 用破折号承载额外说明。
- 用近义或范围重叠的表达重复描述同一因素，例如 moving objects or dynamic-environment conditions。
- 在需要突出核心区分时，使用削弱对比力度的修饰语，例如 additional value。
