# Bilingual Prose Craft

[简体中文](README.md) | [English](README_EN.md)

**帮你润色或审阅中文、英文文本，在表达更清楚的同时保留原意、事实和写作语气。**

它是一套让 AI 按照特定方法完成任务的操作指南，需要配合支持它的工具使用。Bilingual Prose Craft 是一份 Agent Skill，由 Markdown 指令和参考文件组成，不是独立软件，也不自带 AI 模型。

[快速上手](#quick-start)

[![格式：Agent Skill](https://img.shields.io/badge/format-Agent%20Skill-5B5BD6)](https://agentskills.io/)
[![语言：中文 + English](https://img.shields.io/badge/language-%E4%B8%AD%E6%96%87%20%2B%20English-1F6FEB)](skills/bilingual-prose-craft/SKILL.md#language-references)
[![内容：Markdown](https://img.shields.io/badge/content-Markdown-000000?logo=markdown&logoColor=white)](https://daringfireball.net/projects/markdown/)
[![许可证：MIT](https://img.shields.io/badge/license-MIT-2ea44f)](LICENSE)

## 目录

- [为什么需要它](#why)
- [先看效果](#examples)
- [适合谁用](#fit)
- [快速上手](#quick-start)
- [装好之后怎么用](#usage)
- [装好之后怎么管](#manage)
- [安全性与卸载](#safety)
- [常见问题](#faq)
- [版本与许可](#version)
- [为什么值得 Star](#star)
- [防骗提醒](#authenticity)
- [关于作者与继续探索](#about)

<a id="why"></a>
## 1. 为什么需要它？

写文章、产品介绍、邮件或说明文档时，常见的麻烦不是“没有内容”，而是句子绕、重复铺垫、语气像模板，或者改得顺了却把原来的事实和语气也改掉。

这个 Skill 会先看文本的语言、读者和用途，再用对应的中英文表达线索检查明显问题。它把这些线索当作需要结合上下文判断的提示，不会把某个词、标点或句式当成必须删除的规则。

- **你提供：**现有的中文或英文稿件，以及受众、用途、语气等必要背景。
- **AI 处理：**按要求润色、只给诊断建议，或先诊断再改写。
- **你得到：**一版可继续编辑的文本，或针对原文的具体修改建议。
- **你复核：**对照原文检查事实、数字、引用、语气和范围。这个 Skill 不替你核实外部事实。

目前参考文件包含 **26 类英文写作线索**，以及 **31 个中文主题和 1 项共享的读者上下文检查**。使用效果取决于原文、指令和所用 AI 工具；它不会保证每次都改得更好。

<a id="examples"></a>
## 2. 先看效果

下面是为说明用途而编写的**示意例子**，不是一次模型运行记录，也不代表每篇文章都应这样修改。

**中文**

- 提供：“这项工具的设计目标，是希望能够帮助团队成员在报告撰写方面提升效率。”
- 请求：“请润色，保留原意，只返回修改稿。”
- 示例结果：“这项工具旨在帮助团队提高报告撰写效率。”
- 完成后：对照原句确认主张仍然是“帮助团队提高报告撰写效率”，再按实际情况核对这项主张是否成立。

**English**

- Provide: “The purpose of this feature is to help users to be able to find the information that they need more quickly.”
- Ask: “Polish this sentence while preserving its meaning. Return only the revision.”
- Example result: “This feature is designed to help users find the information they need faster.”
- Check: Confirm that the feature, audience, and promised outcome still match the source.

### 四个不同主题的短例子

**自媒体平台文案**

- 原稿：我每天晚上会留十分钟泡杯茶，坐在窗边。这个小习惯让我慢下来，也提醒我别把所有时间都交给工作。找到适合自己的放松方式，可以从一件小事开始。
- 润色：我每天晚上会泡杯茶，在窗边坐十分钟。它让我慢下来，也提醒我别把时间都交给工作。适合自己的放松方式，可以从一件小事开始。

**产品更新**

- 原稿：本次更新旨在为用户带来更加流畅、便捷的文件查找体验。现在，用户可以按文件名称搜索，也可以根据修改日期筛选结果。
- 润色：这次更新优化了文件查找。现在可以按文件名搜索，也可以按修改日期筛选。

**操作说明**

- 原稿：如果你想要进行文件导入，只需在设置页面点击“导入”按钮，选择本地文件并确认，就可以完成导入。
- 润色：打开设置，点击“导入”，选择本地文件并确认。

**English email**

- Before: “I just wanted to reach out to ask whether we might be able to move Friday's review to 3 p.m., if that would still be convenient for you. Please let me know if this might possibly work.”
- After: “Could we move Friday's review to 3 p.m.? Let me know if that works for you.”

### 长篇示例：青屿镇一日游

下面是原创示意稿，借鉴上游 [Full example](https://github.com/blader/humanizer/blob/v4.0.0/README.md#full-example) 的“原稿→润色稿”展示方式，不是上游文本翻译，也不是一次真实模型运行。

**原稿**

> 上周六，我和朋友去了青屿镇，开始了一次令人难忘的海边之旅。我们早早到了车站，怀着期待的心情踏上旅程。天气预报说下午可能下雨，所以我们决定先去海边。海边风很大，沙子吹进鞋里；但眼前开阔的景色让人豁然开朗，所有烦恼仿佛都被海风带走了。
>
> 中午，我们在老街一家小店吃了鱼丸汤。店面不大，店主十分热情，汤鲜味美，鱼丸 Q 弹，值得一试。这里不仅有美食，还有浓浓的人情味。饭后，我们沿街散步，经过旧码头、杂货铺和一个卖海盐的摊位。
>
> 下午果然下起雨，我们躲进车站旁的咖啡店，点了两杯热饮，隔着窗户看雨落在屋檐上。这趟旅行让我明白，放慢脚步才能发现生活中的小确幸。青屿镇不仅是一座小镇，更是一处让人重新找回内心平静的地方。

**润色稿**

> 上周六，我和朋友去了青屿镇。天气预报说下午可能下雨，我们早早到车站后先去了海边。风很大，沙子吹进鞋里；开阔的海景让我觉得轻松了些。
>
> 中午我们在老街一家小店吃鱼丸汤。店面不大，店主很热情，鱼丸有弹性，汤也鲜。饭后我们经过旧码头、杂货铺和一个卖海盐的摊位。
>
> 下午下雨了，我们到车站旁的咖啡店点了两杯热饮，隔着窗看雨落在屋檐上。这趟旅行让我愿意慢下来。青屿镇给我留下的印象，是海边的风、老街的小店和屋檐上的雨。

<a id="fit"></a>
## 3. 适合谁用？

### 特别适合

- 正在修改中文或英文初稿，希望表达更直接、自然的 AI 用户和创作者。
- 要处理产品文案、文章、邮件或说明文档，并且需要保留原有事实与语气的人。
- 想让 AI 先指出问题、暂时不改稿，或按指定方式输出修改结果的人。
- 适用于润色 AI 生成的自媒体平台文案，减少模板化表达，让文字更贴近作者语气；这不代表识别作者身份，也不保证规避 AI 检测。

### 不适合或需要先准备

- 需要识别作者是不是使用了 AI，或要求绕过 AI 检测器：本 Skill 不提供这些能力。
- 需要独立核查事实、引文或数据：本 Skill 不会自动验证来源。
- 要求扩写事实内容：请提供可用资料或指定允许使用的来源；否则它会避免补造事实。
- 使用的 AI 工具不支持 Agent Skills：需要先按该工具自己的说明安装或提供这套指令。

<a id="quick-start"></a>
## 4. 快速上手

### 使用前准备

- 一个支持 Agent Skills 的 AI 工具。下面以 Codex 为例；其他工具可使用 Skills CLI 支持的 Agent。
- 安装 [Node.js 22.20 或更高版本](https://nodejs.org/en/download/)。Skills CLI 通过 npx 运行。
- 使用 AI 模型或外部服务可能产生费用，具体取决于你的工具和服务商；本仓库不附带模型或 API 服务。

在 PowerShell、Terminal 或其他命令行中运行：

~~~sh
node --version
~~~

看到 v22.20.0 或更高版本后继续。如果没有 node 命令，请先从 Node.js 官网安装，再重新打开终端。

### 安装与启用

用 Skills CLI 安装时，指定目标 Agent 为 Codex。想让它只在当前项目可用，请先进入项目目录，再运行：

~~~sh
npx skills add yangjing6213-dev/bilingual-prose-craft --skill bilingual-prose-craft --agent codex
~~~

若要在当前 Windows 用户的所有项目中使用，运行全局安装命令：

~~~sh
npx skills add yangjing6213-dev/bilingual-prose-craft --skill bilingual-prose-craft --agent codex --global
~~~

按终端提示确认安装方式。Windows 不支持符号链接时，可选择复制文件。查看全局安装结果：

~~~sh
npx skills ls -g
~~~

列表中出现 bilingual-prose-craft 表示 CLI 已找到该 Skill。随后在 Codex 中开始新会话。

#### 让 Codex 在文案任务中自动选择此 Skill

全局安装后，可将下面的内容加入 Codex 的全局指令。Windows 用户可在文件资源管理器地址栏输入 %USERPROFILE%/.codex，打开或新建 AGENTS.md 并粘贴。若该文件夹里已有 AGENTS.override.md，应把指令加到这个优先文件中。保存后开始新会话。此设置会提示 Codex 在匹配的任务中调用已安装的 Skill；它不会让不支持 Agent Skills 的工具自动获得该能力。

~~~text
当我让你撰写、改写或润色中文或英文文案、文章、邮件、产品介绍或社交媒体内容时，优先调用已安装的 bilingual-prose-craft Skill。

- 有现成稿件：保留事实、原意、确定程度和作者语气，再进行润色。
- 从零写稿：只根据我提供的信息起草，再按该 Skill 自检；缺少事实时先询问或标出待补内容。
- 默认只返回最终稿，除非我要求诊断、解释或多个版本。
- 只在文案创作和编辑时使用；不要用于事实核查、翻译、判断文本是否由 AI 写成或规避 AI 检测。
- 如果 Skill 未加载，说明这一点，并按以上保真要求继续。
~~~

Skills CLI 的安装选项见[官方命令说明](https://github.com/vercel-labs/skills/blob/main/docs/commands.md#skills-add)；Codex 全局指令的配置方式见[官方文档](https://developers.openai.com/codex/guides/agents-md)。

如果要手动安装到 Codex，把整个 [skills/bilingual-prose-craft](skills/bilingual-prose-craft) 文件夹复制到：

- 当前项目：项目目录下的 .agents/skills/bilingual-prose-craft/ 子目录
- 当前 Windows 用户：%USERPROFILE%\\.agents\\skills\\bilingual-prose-craft\\

不要只复制 SKILL.md；references/ 中的中英文检查线索也是 Skill 的一部分。Codex 的目录说明见[官方文档](https://developers.openai.com/api/reference/cli)。

### 完成第一次使用

把下面的指令和一小段文本发给 AI：

~~~text
请润色下面这段中文，保留事实、原意和我的语气，不要补充信息，只返回修改稿：

[在这里粘贴你的文本]
~~~

看到修改后的文本后，对照原文核对姓名、数字、时间、引用、否定、因果和承诺。如果原文已经清楚，Skill 也可能建议保持不变；这同样符合它的工作方式。

<a id="usage"></a>
## 5. 装好之后怎么用

根据任务，把文本和下面一种指令一起发给 AI：

| 你想做什么 | 可以这样说 |
|---|---|
| 直接润色 | **请润色以下文本，保留事实、原意和语气，只返回修改稿。** |
| 只看问题，不改写 | **请审阅以下文本，列出最重要的问题和修改建议，不要重写。** |
| 先诊断再改写 | **请先简要指出主要问题，再给出修改稿。** |
| 查看完整过程报告 | **请按完整报告模式依次给我：初稿改写、仍然存在的问题、最终润色稿。** |
| 扩写 | **请根据我提供的资料扩写，清楚区分新增事实与原文内容。** |
| 写虚构内容 | 明确说明“这是虚构创作”，并提供体裁、人物或情节要求。 |

处理中英混合文本时，它默认按原有语言工作，不擅自翻译。想让 AI 参考你的表达习惯，可以一并提供你愿意分享的写作样本。修改已有文件时，请明确要求它编辑文件；Skill 会只改文字，尽量保留代码、命令、路径、链接、ID、数据和标题结构。改完后仍需由你确认内容适合发布或使用。

<a id="manage"></a>
## 6. 装好之后怎么管

| 想做什么 | 在命令行中操作 | 如何确认 |
|---|---|---|
| 查看已安装的 Skill | npx skills list | 列表中能找到 bilingual-prose-craft |
| 检查更新 | npx skills check | CLI 显示是否有可用更新 |
| 更新这个 Skill | npx skills update bilingual-prose-craft | 更新后再用 npx skills list 查看 |
| 移除项目级安装 | npx skills remove bilingual-prose-craft | 列表中不再出现 |
| 移除用户级安装 | npx skills remove --global bilingual-prose-craft | 用户级列表中不再出现 |

文件位置取决于安装范围。Codex 项目级目录位于项目目录下的 .agents/skills/bilingual-prose-craft/；Windows 用户级目录是 %USERPROFILE%\\.agents\\skills\\bilingual-prose-craft\\。通常不需要修改其中的文件。要检查具体安装情况，以 npx skills list 和工具自身的目录说明为准。

<a id="safety"></a>
## 7. 安全性与卸载

### 安全性

- 仓库中的 Skill 是 Markdown 指令和参考文档，不含可执行脚本、模型或 API 密钥，也没有独立的数据上传功能。
- 使用时，文本会如何传输和保存取决于你使用的 AI 工具及模型服务。不要在公开对话或仓库中粘贴密码、验证码、访问密钥或不应外传的个人资料。
- 安装命令会联网从 GitHub 获取 Skill，并通过 npx 使用 Skills CLI。CLI 的匿名使用统计和数据说明请查看 [Skills CLI 官方说明](https://github.com/vercel-labs/skills#telemetry)。
- Skill 只在你要求时编辑文件，并按指令只修改文字内容。实际读写范围仍受所用 AI 工具的权限和执行方式影响。

### 卸载

在安装它的项目目录中运行：

~~~sh
npx skills remove bilingual-prose-craft
~~~

如果当初用了 -g 安装到用户级，运行：

~~~sh
npx skills remove --global bilingual-prose-craft
~~~

卸载前确认命令选择的是这个 Skill。移除 Skill 不会卸载共享的 Node.js 或 Skills CLI，也不应删除其他 Skill、你的项目文件或个人设置。手动安装的用户只需移除对应的 bilingual-prose-craft 文件夹；先核对路径，避免误删同目录中的其他内容。

<a id="faq"></a>
## 8. 常见问题

### 为什么有时几乎没有改动？

原文可能已经清楚，或者进一步修改只剩个人偏好。Skill 允许保留清楚的句子，不为显示工作量而改写。

### 它能判断文本是不是 AI 写的吗？

不能。它只根据上下文检查表达方式，不判断作者身份，也不以规避检测为目标。

### 它会帮我核实事实吗？

不会自动核实。它会尽量保留原文的事实和确定程度；若要核查，请另行提供可靠来源并明确要求核查。

### 安装后没有生效怎么办？

先运行 npx skills list 确认已安装，再检查 Skill 是否安装到了当前使用的 Agent 和项目范围。之后新开对话或按该工具文档刷新 Skill。不同 Agent 的支持方式与目录可能不同，可查看 [Skills CLI 文档](https://github.com/vercel-labs/skills)和对应工具说明。

### 使用会不会产生费用？

仓库中的内容是 Markdown 文件，没有自带 AI 模型。模型或服务费用由你选择的 AI 工具和服务商决定。

### 这个 Skill 按什么原理检查文本？

它把常见写作线索当作上下文提示，不把词语或标点当成判断作者身份的依据。英文参考的 26 项沿用 A—F 分类；前五项是较明确的结构线索，单个弱线索则需结合重复、别扭程度、读者和作者样本判断。下面是各类线索的中文概括；详细操作仍以仓库中的中英文参考文件为准。

| 分类 | 检查范围 |
|---|---|
| A：铺垫代替陈述（1—5） | 为强调而否定对比、重复或戏剧化收尾、伪深度格言、起跑式铺垫、回应不存在的异议 |
| B：公式化节奏（6—11） | 强凑三项、重复句首、破折号作万能连接、限定词堆叠、过度使用连字符、被动句或缺少主语 |
| C：拔高与借用权威（12—18） | 套用高频 AI 词、拔高意义、模糊关联、空泛补充、宣传语代替事实、借权威背书、绕开普通动词 |
| D：公式化排版（19—21） | 装饰性粗体、装饰性标题、与目标格式不一致的引号 |
| E：聊天与草稿残留（22—25） | 客服式套话、重复免责与猜测、首句重复标题、叙述文档或写作过程 |
| F：读者背景与中文补充检查（26、27—32） | 复述读者已经知道的背景，以及六类中文表达线索；上下文不足时保留必要说明 |

中文版还增加六类表达检查：多层“的”连续修饰、“进行 + 动词”、连续堆叠“被”字句、同义四字词排比、没有信息的“随着……发展”开头、套话式收尾。因此中文参考文件共含 31 个中文主题和 1 项共享的读者上下文检查。

### 编辑时遵循哪些原则？

1. 优先保留信息和确定程度，再遵守用户给定的范围与文本要求，匹配作者语气，最后处理具体表达问题。
2. 不新增功能、数据、来源、人物身份或第一人称经历；不把“可能”改成“确定”，也不把“计划”改成“已经完成”。
3. 保留否定、条件、归因、范围、时间和完成状态，以及句子之间真实的因果关系。
4. 三项列表、四字格、被动句、破折号和引号都可能有用；不因形式本身就删除。
5. 保留个人表达、学术和商务文本的正式程度；中英混排时默认不翻译。
6. 编辑文件时保留代码、命令、路径、链接目标、YAML、数据、标题和锚点；若调整标题或结构，检查引用它们的链接。
7. 默认只交付最终稿，不要求展示中间草稿、命中清单或自评分数。

以上原则和检查分类参考了 [blader/humanizer 的 26 项写作线索](https://github.com/blader/humanizer/blob/v4.0.0/README.md#the-26-patterns)。本项目保留其 MIT 来源声明，见 [第三方版权声明](THIRD_PARTY_NOTICES.md)。

### 为什么 README 显示的字体不是微软雅黑？

GitHub 按自己的页面样式呈现 Markdown，仓库无法可靠指定每位访客设备上的字体。本 README 已统一正文标记，说明文字不额外使用字体标签，命令示例仍放在便于复制的代码块中。本地浏览器是否使用微软雅黑由设备和浏览器设置决定。GitHub 的 Markdown 格式说明见[官方文档](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)。

<a id="version"></a>
## 9. 版本与许可

- Skill 文件当前标注版本：1.0.0。仓库目前没有单独的变更日志；后续变化以 GitHub 提交记录为准。
- 本项目采用 [MIT License](LICENSE)。
- 本 Skill 改编整合了其他 MIT 许可 Skill 的材料。请一并保留 [第三方版权声明](THIRD_PARTY_NOTICES.md)和原许可信息。

<a id="star"></a>
## 10. ⭐ 为什么值得 Star

如果你以后还会让 AI 修改不同类型的中英文稿件，这套可重复使用的编辑步骤和参考线索可以省去每次重新解释规则的麻烦。

如果这个项目对你有帮助，欢迎点个 Star，方便以后再找到，也给我一点继续打磨的动力。

<a id="authenticity"></a>
## 11. 防骗提醒

请通过本仓库和[恩禾 ENHE AI 官网](https://www.enhe-tech.com.cn/)确认项目及作者信息。若有人以本项目或作者名义联系你收费、索要合作款或提供其他授权信息，请先通过下方列出的官网或作者联系方式核实。不要向陌生人提供密码、验证码或访问密钥。

<a id="about"></a>
## 12. 关于作者与继续探索

### 关于作者

**Enhe（恩禾）｜产品设计师 · 一人公司实践者 · AI Builder**

用 AI 打造一人公司。

- GitHub：[yangjing6213-dev](https://github.com/yangjing6213-dev)
- X / Twitter：[Amenenhe_ai](https://x.com/Amenenhe_ai)
- 网站：[恩禾 ENHE AI](https://www.enhe-tech.com.cn/)
- 微信：Hu-Amen
- 邮箱：[amen.enhe@gmail.com](mailto:amen.enhe@gmail.com)

本 Skill 由 Enhe（恩禾）统筹整合和编写，并使用 AI 辅助；相关来源和版权信息见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

### 相关项目

- [blader/humanizer](https://github.com/blader/humanizer)：适合想了解英文文本编辑线索来源的读者。
- [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh)：适合想了解中文文本编辑线索来源的读者。

### 继续探索

我把对中英文表达的编辑方法整理成这份可复用的 Skill，方便在 AI 写作和日常工作中反复使用。也可以访问[恩禾 ENHE AI 官网](https://www.enhe-tech.com.cn/)，了解 AI 工具、AI 技能和相关行业动态。
