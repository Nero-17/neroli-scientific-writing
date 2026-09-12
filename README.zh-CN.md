# Neroli Scientific Writing

把科学稿件（包括 GPT 生成的稿件）按 Nero Ziyu Li 的论述逻辑、语言选择和写作偏好统一修改的 skill。

本公开版本只包含论文写作，整合了原本放在 Nero-style 中的论文规则。研究陈述与申请、邮件和非论文中文表达及翻译继续保留在本地 Nero-style 中，不进入本仓库。

它以两篇数学论文为基础，将修改过程写成五个阶段：

1. **确认修改范围。** 默认允许实质性改写；明确要求轻改或直译时，保留原有推进方式。
2. **先弄清论证。** 识别研究问题、已有结果、具体障碍、解决方法、结论和限制，记录必须保留的数学内容。
3. **调整论述。** 让定义、引理、例子和公式有明确用途；复杂步骤保留推理，直接结果保持简短。
4. **修改语言。** 直白、具体，保留有根据的力度，删掉空泛宣传和重复说明，不增加非必要缩写变量。
5. **对照原稿。** 检查假设、量词、常数依赖、例外、符号、引用与结论状态有没有被悄悄改掉。

这些阶段是编辑时执行的工作，不会作为固定标题塞进论文。默认先交付改好的正文；实质修正或未解决的问题单独简述。

完整论文还遵循作者明确提出的结构规则：摘要尽量简短且不超过五句话；摘要之后立即放目录；引言直接重述主要定理并沿用正文编号，同时放解释模型的图；subsection 数量由论证需要决定，可以没有，也可以有一个、两个或更多，最多五个。三个不是目标或最低数量，各 section 不必整齐划一；不能为凑数拆分、合并或填充内容，也不能只是把多余标题机械降级。

主定理后加入一个具体计算例子：明确对象和参数，实际算出定理中的量，并说明计算结果的含义。引言中的定理重述后可给精简计算，正文主定理后给完整推导；不能仅列举例子名称，也不能把有限近似写成精确极限。

Introduction 从引人入胜的具体问题、真实的猜想背景或其他数学切入点开场，自然引出本文要回答的问题。随后用 Background 交代方向进展，再用一个 Main results subsection 集中叙述主要结果，按正文 section 的先后顺序推进并沿用正文编号，用过渡段连接不同问题与结论，最后说明 Lean formalisation 的实际范围。这是可调整的写作方式，不强制历史开场或整套固定标题；主要结果内部仍按正文 section 顺序叙述，必要时可以在背景和定理之间介绍模型。没有形式化材料时应指出缺失，不能编造已验证的结论。

公式不使用公式框；已有的框只去掉展示性边框，保留数学内容、公式编号和交叉引用。

几何引理可以先用简短开头交代必要对象，再按实际操作逐步说明，每步说明后紧接对应配图，最后用引理收束已经完成的证明，不重复推导。减少零碎的独立公式；图内优先用符号，位移和位置向量用箭头表示，需要时加入坐标，并以淡色母图保留几何背景。删除没有新增信息的图。三步、三张图和半页开头是具体任务中的选择，不是所有论文的固定模板。详见[几何推导与证明配图](references/proof-figures.md)。

## 调用示例

```text
用 $neroli-scientific-writing 修改下面这段 GPT 写的论文引言。
可以调整论述顺序，按我的逻辑和语言重写；保留数学主张、记号和引用。
先给我能直接放进论文的 LaTeX。
```

```text
用 $neroli-scientific-writing 检查这段证明的表述。
把真正困难的步骤解释清楚，不要增加非必要缩写变量。
发现不能成立的推理时单独指出，不要用润色遮住它。
```

```text
用 $neroli-scientific-writing 忠实翻译这段中文论文。
这次只做必要修改，保留原稿顺序和语气。
```

## 内容与依据

- [Skill 入口](SKILL.md)
- [论证与证明的处理](references/argument-and-proof.md)
- [语言与节奏](references/language-and-rhythm.md)
- [几何推导与证明配图](references/proof-figures.md)
- [修改前后示例](references/examples.md)
- [论文来源、阅读范围与归纳依据](references/evidence.md)
- [行为测试](evals/README.md)

本版只以作者选定的两篇论文为论文语料：[Fractal dimensions for Iterated Graph Systems](https://arxiv.org/html/2212.01987v4) 和 [Iterated Graph Systems (I): random walks and diffusion limits](https://arxiv.org/html/2603.13798v3)。归纳侧重写作组织与表述，不代表对两篇全文证明的验证；旧稿中的语病、压缩跳步或宣传性措辞不会被一概保存为偏好。

示例均为新构造，公开包不包含私人邮件、历史任务记录或私人 Drive 文件。普通调用无需联网。它是由模型执行的编辑流程，不是单独运行的程序；最有依据的应用范围是数学写作。

## 安装

```sh
git clone https://github.com/Nero-17/neroli-scientific-writing.git ~/.agents/skills/neroli-scientific-writing
```

已有旧版 `humanize-scientific-writing` 时，安装后将旧目录移到 skill 发现目录之外，避免重复匹配。

将整个目录放在个人 `~/.agents/skills/neroli-scientific-writing/`，或项目的 `.agents/skills/neroli-scientific-writing/`，保留 `SKILL.md` 与 `references/` 的相对位置。详见 [Codex 官方说明](https://learn.chatgpt.com/docs/build-skills)；新 skill 未显示时可重启 Codex。

本仓库原创内容采用 [MIT 许可](LICENSE)，不改变所链接论文原有的版权与许可。
