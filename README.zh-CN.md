<!--lint disable awesome-list-item-->

# 注意力工程（Attention Engineering） [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

```bash
npx skills add ghostbody/attention-engineering --skill attention-engineering -y
```

**TL;DR** —— 装上面这个 skill，直接问你的 agent。它自带本列表的原则与目录，你不需要读这个仓库。下面的一切是给想浏览或贡献的人看的。126 条资源，9 个分类，一句话：把读者的注意力当预算。

<img src="assets/banner.svg" alt="Attention Engineering — 在 AI 时代，节省你最珍贵的资源" width="100%">

注意力工程（attention engineering）指设计 AI 系统和信息流，让人的注意力只花在真正需要它的决策和卡点上。AI 让生成几乎免费，而审查生成内容的成本并没有下降，瓶颈因此从生产移到了判断。这里每一条资源都从这份负荷里削掉可度量的一块：少读几页、少逐行看几个 diff、少几次点击、少几次等待、少几次被打断。我们只收录让人读得更少、看得更少、点得更少、等得更少的资源。

## 目录

- [基础与阅读](#基础与阅读)
- [资源清单与索引](#资源清单与索引)
- [蒸馏：从文档到答案](#蒸馏从文档到答案)
- [分诊：排序、去重、分批](#分诊排序去重分批)
- [地图与渐进呈现](#地图与渐进呈现)
- [平静与专注](#平静与专注)
- [省注意力的开发流程](#省注意力的开发流程)
- [反模式与研究](#反模式与研究)
- [组织与生活](#组织与生活)
- [五条原则](#五条原则)
- [当作 Skill 使用](#当作-skill-使用)
- [反模式](#反模式)

> English version: [README.md](README.md)

## 基础与阅读

从这里开始看「注意力有限」的证据；每一条都用一套框架替代零散的二手阅读。

- [Why Is It So Hard to Do My Work?](https://doi.org/10.1016/j.obhdp.2009.04.002) - 说明没做完的任务切换会留下注意力残留（attention residue），所以做完一件胜过开五件。
- [On the Need for Attention-Aware Systems](https://doi.org/10.1016/j.chb.2005.12.009) - 把打断成本拆成绩效、出错和情绪三项，为任何通知策略给出基线。
- [Cognitive Load During Problem Solving](https://doi.org/10.1016/0364-0213%2888%2990023-7) - 区分内在、外在和关联负荷，于是冗余的呈现可以直接删掉，而不是压缩。
- [The Concept of Information Overload](https://doi.org/10.1080/01972240490507974) - 把四十年的信息过载研究收进一页的成因与结果框架，替代一摞论文。
- [Guidelines for Human-AI Interaction](https://doi.org/10.1145/3290605.3300233) - 给出 18 条可测试的规则，判断 AI 何时该开口，于是大部分主动消息根本不会发出。
- [Humans and Automation](https://doi.org/10.1518/001872097778543886) - 区分自动化的正确使用、误用、弃用和滥用，说清哪些任务才值得人亲自看。
- [Persuasive Computers](https://doi.org/10.1145/274644.274677) - 提出「说服性技术」（captology）及其功能三角，让设计者在上线前先审一遍产品的说服手法。
- [The Attention Economy and the Net](https://doi.org/10.5210/fm.v2i4.519) - 把注意力定义为网络市场里的稀缺资源，下面每个分诊决策都以此为前提。
- [The Attention Economy](https://www.nngroup.com/articles/attention-economy) - 把注意力当成设计约束，指出界面在哪消耗它却没有回报。
- [Charts of the Week: Attention is All You Need](https://www.a16z.news/p/charts-of-the-week-attention-is-all) - 给每周媒体消费设一个上限，注意力预算才有真实容量可依据。
- [Is Google Making Us Stupid?](https://www.theatlantic.com/magazine/archive/2008/07/is-google-making-us-stupid/306868) - 追溯「扫读式」媒介如何削弱持续阅读，主张奖励深读的格式。
- [Attention economy](https://en.wikipedia.org/wiki/Attention_economy) - 一页讲清概念与主要批评，替代一整排入门读物。
- [如何在信息过载时代开启「独立思考」的人生](https://sspai.com/post/82646) - 用「提问—拆解—综合」的循环，把阅读从收集变成判断。
- [开篇语：你的注意力去哪儿了？](https://sspai.com/prime/story/vol012-opening-words) - 先讲注意力是一种预算，再谈工具，读者因此不会在换工具上打转。
- [Designing Organizations for an Information-Rich World](https://gwern.net/doc/design/1971-simon.pdf) - 提出信息丰富即注意力匮乏，后面所有文献都以这个前提起步。
- [The Magical Number Seven, Plus or Minus Two](https://psychclassics.yorku.ca/Miller) - 把工作记忆限制在少数几个块内，任何超过这个长度的清单都会漏信息。
- [The Computer for the 21st Century](https://doi.org/10.1038/scientificamerican0991-94) - 把计算放进环境背景，交互不再抢占前台注意力。
- [Information Foraging](https://doi.org/10.1037/0033-295X.106.4.643) - 把阅读建模为跟随「信息气味」，解释一个链接或标题何时值得点击。
- [Augmenting Long-term Memory](http://augmentingcognition.com/ltm.html) - 用间隔重复让知识保持可检索，用回忆替代反复搜索。
- [Information overload](https://en.wikipedia.org/wiki/Information_overload) - 一页讲清成因、度量和对策，给出这个领域的快速地图。
- [何为「注意力经济」](https://www.aisixiang.com/data/182419.html) - 讲平台如何把用户时间换成收入，点明这条抽取链。

## 资源清单与索引

缩短「找一个可复用技能」这件事的目录和索引。

- [skills.sh](https://skills.sh) - 按使用量给可安装的 agent skill 排序，装现成的替代从零搭建。
- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) - 按任务索引 skill，扩展 agent 之前先缩短搜索时间。
- [Vercel skills CLI](https://vercel.com/changelog/introducing-skills-the-open-agent-skills-ecosystem) - 一条命令装好 skill，不用通读手写的安装说明。
- [e2b-dev/awesome-ai-agents](https://github.com/e2b-dev/awesome-ai-agents) - 按任务索引 agent，分派工作从一个候选开始，而不是一张白纸。
- [Meirtz/Awesome-Context-Engineering](https://github.com/Meirtz/Awesome-Context-Engineering) - 汇集上下文工程的论文与工具，减少「该给模型喂什么」的试错。
- [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - 精选 Claude Code 的工作流与命令，用验证过的自动化替代手动读改。
- [plenaryapp/awesome-rss-feeds](https://github.com/plenaryapp/awesome-rss-feeds) - 提供精选订阅源和 OPML 文件，用自选订阅替代算法时间线。
- [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official) - 列出官方插件，工作流直接安装，而不是照着文档拼装。

## 蒸馏：从文档到答案

这些工具把长文档、长日志或代码库，压缩成做一次决策所需的少数几个答案。

- [anthropics/skills](https://github.com/anthropics/skills) - 提供 docx、pdf、pptx、xlsx 技能，直接从文档里取出答案，不用整篇通读。
- [MCP reference servers](https://github.com/modelcontextprotocol/servers) - 把抓取、记忆和结构化推理移出提示词，上下文里装的是结论而不是原始页面。
- [Exa MCP](https://exa.ai/mcp) - 一次语义查询就返回抽取好的网页内容，替代「浏览、点击、抓取」的循环。
- [Context7](https://github.com/upstash/context7) - 按需拉取版本匹配的库文档，结束因示例过期导致的反复重试。
- [mcp-summarization-functions](https://www.npmjs.com/package/mcp-summarization-functions) - 命令、文件和目录在进入上下文前先摘要，把长输出压到决策点。
- [读者用 AI“代读”公众号，转发的人反而更多了](http://mp.weixin.qq.com/s?__biz=Mzg5NDg2NjY1NQ==&mid=2247484990&idx=1&sn=b5477a19ae90cf941f44d86434961fdd) - 区分「过滤」和「理解」，说明 AI 代读在哪里省时间、在哪里丢掉要点。
- [mozilla/readability](https://github.com/mozilla/readability) - 抽取文章正文、丢掉广告和侧栏，一页只留下真正相关的那几段。
- [trafilatura](https://github.com/adbar/trafilatura) - 批量抽取正文，把一堆噪声页面的抓取结果压成可读内容。
- [Full-Text RSS](https://fivefilters.org/content-only) - 从订阅链接直接给出正文，省掉这次页面访问和它周围的杂乱元素。
- [summarize](https://github.com/steipete/summarize) - 把网址或视频先压成要点，读者再决定是否投入时间。
- [docling](https://github.com/docling-project/docling) - 把文档转成结构化数据，PDF 因此可检索、可问答，而不必扫读。
- [marker](https://github.com/datalab-to/marker) - 高准确率地把 PDF 转成干净的 Markdown，长报告一遍就能查询。
- [firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) - 为 agent 把网页抓成 Markdown，替代「浏览再复制」的循环。
- [简悦 SimpRead](https://github.com/Kenshin/simpread) - 去掉页面外壳，得到干净的阅读视图，不用先扫过导航和广告。

## 分诊：排序、去重、分批

这些资源减少最终递到人手上的条目数量。

- [Effects of Intelligent Notification Management](https://doi.org/10.1145/1357054.1357070) - 把通知推迟到任务边界能显著降低干扰，所以批量投递优于即时投递。
- [An In-Situ Study of Mobile Phone Notifications](https://doi.org/10.1145/2628363.2628364) - 实测每天约 63.5 条通知，多数被评为低价值，给出可用的截断线。
- [Indicators, Validations, and Notifications](https://www.nngroup.com/articles/indicators-validations-notifications) - 把消息分成三类，大部分反馈因此变成行内状态，而不是通知。
- [Five Mistakes in Designing Mobile Push Notifications](https://www.nngroup.com/articles/push-notification) - 说明「一上来就要权限」和「群发推送」如何训练用户无视提醒，以及该改成发什么。
- [@yonki/dedup](https://www.npmjs.com/package/@yonki/dedup) - 在重复和近似重复的文件被读第二遍之前就检出它们。
- [Info-Pigu 信息辟谷](https://github.com/bluelava/infopigu) - 按论点对页面去重，只展示新增的认知增量，省掉重复阅读。
- [apprise](https://github.com/caronc/apprise) - 把许多通知来源汇进一个网关，人只需看一个渠道，而不是八个。
- [Notification settings on iPhone](https://support.apple.com/guide/iphone/iph7c3d96bab/ios) - 把提醒归组、定时汇总成摘要，大部分提示被移出当下这一刻。
- [Notification Cooldown](https://www.androidauthority.com/android-16-notification-cooldown-3501276/) - 压制同一应用反复发出的提醒，把一阵轰炸收到第一个有用信号。
- [信息过载时代，我的漏斗式阅读工作流](https://sspai.com/post/107554) - 先对订阅源去重、摘要、排序，再交人看，只有活下来的才到读者眼前。

## 地图与渐进呈现

这些资源先给结构，细节按需展开，没人需要再从原始文件里重建地图。

- [The Coming Age of Calm Technology](https://calmtech.com/papers/coming-age-calm-technology.html) - 主张技术在中心与外围之间移动，大部分状态留在背景。
- [Progressive Disclosure](https://www.nngroup.com/articles/progressive-disclosure) - 二级控件留到用户要时才出现，首屏只留少数真正要紧的选择。
- [Agent Skills 官方文档](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) - 触发前只加载技能的元数据，上下文里带的是地图，不是每一本手册。
- [Equipping agents with Agent Skills](https://www.anthropic.com/research/equipping-agents-for-the-real-world-with-agent-skills) - 解释为什么「元数据优先」的加载方式能让 agent 扩展，又不必撑大每条提示词。
- [Calm Technology 原则](https://calmtech.com) - 给出八条低干扰原则，把状态移到外围，中心留空。
- [Designing and Evaluating Glanceable Peripheral Displays](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2007/EECS-2007-56.pdf) - 确立「一瞥」如何在不切换任务的情况下承载状态。
- [Ambient Displays](https://doi.org/10.1007/3-540-69706-3_4) - 说明光和声如何在注意力边缘传递信息。
- [pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) - 先加载技能元数据、正文按需加载，提示词里只留相关的那一片。

## 平静与专注

这些资源移除或推迟那些打断专注时段的东西。

- [A Pace Not Dictated by Electrons](https://doi.org/10.1145/2207676.2207754) - 发现不使用邮件的小组压力更低、专注时段更长，量化了查收件的成本。
- [Disconnecting Distraction](https://paulgraham.com/distraction.html) - 用另一台机器上网，专注不靠意志力也能维持。
- [It's Time to Dismantle the Technopoly](https://www.newyorker.com/tech/annals-of-technology/its-time-to-dismantle-the-technopoly) - 主张砍掉工具而不是默认全用，每砍一个就少一条信息流。
- [How to Thrive in the Attention Economy](https://greatergood.berkeley.edu/article/item/how_to_thrive_in_the_attention_economy) - 在刺激和回应之间插入停顿，把条件反射式的回复变成有意的回复。
- [Your Attention Didn't Collapse. It Was Stolen](https://www.theguardian.com/science/2022/jan/02/attention-span-focus-screens-apps-smartphones-social-media) - 把专注力丧失重新定义为结构问题而非个人问题，把力气放在设计上而不是自责。
- [我用这些方法夺回被侵占的注意力](https://sspai.com/post/59606) - 在四层上减少打断：应用设置、推送、RSS 和快捷指令。
- [重建注意力的边界](https://sspai.com/post/110789) - 用刻意的摩擦（如 Opal）提高冲动打开应用的成本。
- [zenfeed](https://github.com/glidea/zenfeed) - 把整份 RSS 变成打分的每日简报，用读一次替代反复刷。
- [Folo](https://github.com/RSSNext/Folo) - 聚合订阅并在展示前用 AI 摘要，一份信息流当作简报来读。
- [miniflux/v2](https://github.com/miniflux/v2) - 只给纯标题列表、没有推荐，刷进推荐内容这条路直接断掉。
- [newsboat](https://github.com/newsboat/newsboat) - 在终端读订阅，没有图片和算法，列表读完会话就结束。
- [RSSHub](https://github.com/DIYgod/RSSHub) - 把没有订阅源的站点变成订阅，替代反复手动访问。
- [wallabag](https://github.com/wallabag/wallabag) - 把文章剥到只剩正文留待以后读，阅读时不带广告和版式。
- [SelfControl](https://github.com/SelfControlApp/selfcontrol) - 在设定时段内封掉指定站点，直接取消「去检查一下」这个选项。
- [one sec](https://one-sec.app) - 打开应用前强制停顿，打断自动点开应用的动作。
- [Set up a Focus on iPhone](https://support.apple.com/guide/iphone/set-up-a-focus-iphd6288a67f/ios) - 按场景静音指定的应用和人，打断只来自选定的一组。
- [Digital Wellbeing](https://support.google.com/android/answer/9346420) - 限制应用时长并安排专注时段，让过度使用在占满一天之前被看见。
- [changedetection.io](https://github.com/dgtlmoon/changedetection.io) - 监控页面并只报告变化，替代反复刷新检查。
- [为什么我们要减少阅读新闻](https://sspai.com/post/77426) - 论证新闻消费价值低且带偏，为整类信息源被砍掉提供理由。
- [信息断舍离：取关 70 个公众号](https://sspai.com/post/75569) - 批量退订并容忍空出来的位置，减少同质化输入。
- [科技爱好者周刊](https://github.com/ruanyf/weekly) - 把一周科技新闻压进一期精选，替代每天刷信息流。

## 省注意力的开发流程

这些资源把评审从数行数变成看风险，并让机器先吃掉第一遍。

- [Expectations, Outcomes, and Challenges of Modern Code Review](https://doi.org/10.1109/ICSE.2013.6606617) - 发现评审的价值主要在沟通，逐行挑刺可以砍掉。
- [Modern Code Review: A Case Study at Google](https://doi.org/10.1145/3183519.3183525) - 说明小改动与快速周转支撑起这套实践，让每次评审控制在一个固定的注意力预算内。
- [The End of Code Review](https://arxiv.org/abs/2606.13175) - 主张编码 agent 可以接手强制评审，人的注意力转向规格与验收。
- [Best Practices for Peer Code Review](https://smartbear.com/learn/code-review/best-practices-for-peer-code-review) - 给出有效上限：每次 200 到 400 行、60 到 90 分钟。
- [CodeRabbit](https://docs.coderabbit.ai/guides/code-review-overview) - 摘要一个 PR 并按风险给评论排序，评审从风险最高的那段开始。
- [Graphite AI Reviews](https://graphite.com/features/ai-reviews) - 在人之前先跑一遍机器评审，队列里只剩下需要判断的地方。
- [Greptile](https://www.greptile.com/docs/introduction) - 把一处改动映射到整个仓库，省掉人工跨文件追踪。
- [serena](https://github.com/oraios/serena) - 按符号和引用检索代码，agent 只读相关函数，而不是整个文件。
- [repomix](https://github.com/yamadashy/repomix) - 把仓库打包成一份结构化提示词，替代逐个文件地读。
- [claude-mem](https://github.com/thedotmack/claude-mem) - 跨会话保留上下文，省掉每个任务开头重新解释一遍。
- [i-have-adhd](https://github.com/ayghri/i-have-adhd) - 强制先给答案、后给细节，缩短读到结论之前的那一段。
- [DeepSeek Super-agent 原型](https://github.com/deepseek-ai/dsh-superagent-prototype) - 常驻 Router 负责事件分级与派单，Worker 独立上下文并行，人只跟一个队列而不是三到五个会话。

## 反模式与研究

这些材料记录注意力是怎么被浪费的，设计评审因此可以引一项失败案例，而不是争论个人偏好。

- [The Cost of Interrupted Work](https://doi.org/10.1145/1357054.1357072) - 实测打断之后压力更高，即使工作反而变快，给「就问你一句」标了价。
- [No Task Left Behind?](https://doi.org/10.1145/1054972.1055017) - 发现 57% 的工作片段被中断，记录下一天已经被切得多碎。
- [Disruption and Recovery of Computing Tasks](https://doi.org/10.1145/1240624.1240730) - 记录打断后的恢复时间和切换模式，给每次提示算出一个可测成本。
- [If Not Now, When?](https://doi.org/10.1145/985692.985727) - 说明打断成本随时刻差异极大，只靠选时机就能省注意力。
- [A Diary Study of Task Switching and Interruptions](https://doi.org/10.1145/985692.985715) - 记录真实工作周里频繁的切换和缓慢的恢复。
- [Alarm Fatigue: A Patient Safety Concern](https://doi.org/10.4037/NCI.0b013e3182a903f9) - 报告 72% 到 99% 的临床报警是误报，导致脱敏并漏掉真实的报警。
- [Alert Fatigue in Security Operations Centres](https://doi.org/10.1145/3723158) - 综述安全运营中心（SOC）的告警疲劳（alert fatigue）及对策，是同一个失败在运维侧的版本。
- [Does Automation Bias Decision-Making?](https://doi.org/10.1006/ijhc.1999.0252) - 发现人会信任自动化建议到漏掉明显错误，所以必须强制校验。
- [The Flaws of Policies Requiring Human Oversight](https://doi.org/10.1016/j.clsr.2022.105681) - 主张「人在环内」的审核常常沦为形式，削弱而不是增加了控制。
- [Does the Whole Exceed Its Parts?](https://doi.org/10.1145/3411764.3445717) - 说明 AI 解释反而可能加重依赖，解释的设计必须防止注意力偷懒。
- [IM, Not IP](https://doi.org/10.1145/966712.966731) - 把实时打断称作信息污染，主张改为受管理的信息流。
- [Losing in the Attention Economy](https://stratechery.com/2026/losing-in-the-attention-economy) - 用停滞的游戏行业说明注意力是一个零和市场。
- [The Acceleration of Addictiveness](https://paulgraham.com/addiction.html) - 解释技术如何把「想要」压缩成「过度想要」，这是强迫性检查背后的机制。
- [How Technology Hijacks People's Minds](https://medium.com/@tristanharris/how-technology-hijacks-peoples-minds-from-a-magician-and-google-s-design-ethicist-56d62ef5edf3) - 列出十种劫持模式，可作为审查界面的清单。
- [AI slop](https://en.wikipedia.org/wiki/AI_slop) - 定义大批量的低质 AI 内容，这是信息流过滤器首先要清掉的一类。
- [2025 Word of the Year: Slop](https://www.merriam-webster.com/wordplay/word-of-the-year) - 记录该词进入主流用法，坐实「slop」是一个有名字的过滤目标。
- [We Are Hopelessly Hooked](https://www.nybooks.com/articles/2016/02/25/we-are-hopelessly-hooked) - 从内部审视说服式设计的实践，揭开习惯回路背后的伦理。
- [TikTok's Enshittification](https://doctorow.medium.com/tiktoks-enshittification-bb3f5df91979) - 追踪信息流如何从服务用户退化为服务广告主，解释噪声为什么只增不减。
- [How Wikipedia Is Fighting AI Slop Content](https://www.theverge.com/report/756810/wikipedia-ai-slop-policies-community-speedy-deletion) - 说明社区级的快速删除加 AI 功能清单，能在早期拦住低质页面。
- [Enshittification](https://en.wikipedia.org/wiki/Enshittification) - 给平台衰败的三阶段模式命名，让这种流失在被感受到之前就被认出。
- [当我们的注意力成为货币](https://zhuanlan.zhihu.com/p/1924124186651099843) - 讲平台如何把注意力变现，以及该在哪一环切掉这条抽取链。
- [大脑的“硬伤”，竟然被“快餐式”AI 读书无限放大了](http://m.chinanews.com/wap/detail/cht/zw/10608985.shtml) - 说明 AI 书摘会放大既有的阅读偏差，这是「代读」的边界。
- [Deceptive Patterns — Types](https://www.deceptive.design/types) - 给暗黑模式（dark patterns）分类并附法律对应，几秒内就能给一个操纵性流程定性。
- [Dark Patterns at Scale](https://arxiv.org/abs/1907.07032) - 审计 11,000 个购物网站并量化操纵性设计，把个案变成证据。
- [Doomscrolling](https://en.wikipedia.org/wiki/Doomscrolling) - 给「强迫性刷负面新闻」命名，让这个行为可见到足以被打断。

## 组织与生活

这些资源把同一套分诊用在团队目标、会议和个人的信息摄入上。

- [Getting the Attention You Need](https://hbr.org/2000/09/getting-the-attention-you-need) - 把注意力当作组织资源，它被过载和人员精简两头挤压。
- [It's Time to Embrace Slow Productivity](https://www.newyorker.com/culture/office-space/its-time-to-embrace-slow-productivity) - 用短的串行队列替代并行工作，省掉大部分切换成本。
- [如何应对信息过载？](https://www.zhihu.com/question/297546899) - 汇集可复用的阅读与过滤工作流，而不是推荐某一个工具。
- [Getting Things Done](https://gettingthingsdone.com) - 把待办移进一份可信的清单，未完成的事不再以注意力残留的形式反复冒头。
- [Inbox Zero](https://web.archive.org/web/2020/https://www.43folders.com/izero) - 在固定批次里把消息清到零，替代不停地查收件箱。
- [Progressive Summarization](https://fortelabs.com/blog/progressive-summarization-a-practical-technique-for-designing-discoverable-notes/) - 分层压缩笔记，以后再读时从摘要开始，而不是回到原文。
- [Deep Work](https://calnewport.com/writing) - 主张长时间不被打断的区块，把切换成本变成一项排程决策。

## 五条原则

| 原则       | 含义                             | 检验问题                      |
| -------- | ------------------------------ | ------------------------- |
| 压缩       | 删整条，不是删字，直到一眼就能承载决策。           | 读者能在 10 秒内说出结论和下一步吗？      |
| 分层       | 只有最上层可以打断；准确率优先于召回。            | 这条为真的概率，高到足以支撑一次打断吗？      |
| 地图       | 先给全局结构，细节默认折叠。                 | 有没有一行字或一张图，说清这是什么、由几部分组成？ |
| 人负责决策与卡点 | 人只处理价值判断和无法绕开的障碍，别的不管。         | 这个动作是决策，还是本该由 AI 完成的执行？   |
| AI 闭环    | AI 收集、核实、修复、复查，最后落在「已决」或「已完成」。 | 这次交互之后，任务状态变了吗？           |

## 当作 Skill 使用

装好这个 skill 后，agent 直接按这份目录回答，不需要克隆或读仓库。

```bash
npx skills add ghostbody/attention-engineering
```

装好后可以这样问：

- 「我们的 agent 每天早上发一份 40 条的状态报告，该砍什么？」
- 「上个月告警太吵，团队把所有提醒都静音了。怎么把这个渠道重建起来？」
- 「来了一个 3000 行的 PR，合并前该怎么审？」

## 反模式

- 输出越长当作价值越高——交付结论和要做的决策，不是完整过程。
- 每个异常都立刻推送——打断只留给最上层，并记录被丢掉的是什么。
- 把长报告一句一句地缩短——整节删掉那些不改变决策的内容。
- 对机器生成的 diff 逐行评审——改成审风险点和架构。
- 为了「可见性」加更多看板——一个排好序、有负责人的队列胜过二十块面板。
- 让人「快速确认」细节——让 agent 自己核实并报告结果。
- 追召回的告警设计——接受漏报，以保住人还愿意看的那些告警。
- 不核对来源就叠 AI 摘要——任何驱动决策的说法都要保留原文链接。
- 本可以写成一份决策的会——改为发一页决策文档，带截止时间。
- 首次启动就申请通知权限——先用可验证的价值换来这次打断。

## 贡献

提 PR 前先读 [CONTRIBUTING.md](CONTRIBUTING.md)，并使用[资源推荐 issue 模板](https://github.com/ghostbody/attention-engineering/issues/new?template=add-resource.yml)。每个 PR 最多三条新条目，且只涉及一个分类。
