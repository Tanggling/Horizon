---
layout: default
title: "Horizon Summary: 2026-10-31 (ZH)"
date: 2026-10-31
lang: zh
---

> 从 43 条内容中筛选出 11 条重要资讯。

---

**科技新闻**
1. [Cursor 市场出现带后门的 Claude Code 扩展](#item-tech-news-1) ⭐️ 8.0/10
2. [研究报告 Azure 五例跨租户攻陷](#item-tech-news-2) ⭐️ 8.0/10
3. [Northflank 被指遭入侵，细节待核实](#item-tech-news-3) ⭐️ 7.0/10
4. [Nesformer 用约 1 GB Qwen 权重模拟 NES](#item-tech-news-4) ⭐️ 7.0/10
5. [Tangled 重构架构并新增组织支持](#item-tech-news-5) ⭐️ 7.0/10
6. [Bunny 停用亚美尼亚节点并重签 TLS 证书](#item-tech-news-6) ⭐️ 7.0/10
7. [Soft-MTP 提出一行梯度修正方案](#item-tech-news-7) ⭐️ 7.0/10
8. [百度网盘 iOS 摇一摇广告被指使用磁力计](#item-tech-news-8) ⭐️ 7.0/10
9. [Apple 智能拟于 11 月 4 日在华开启开发者测试](#item-tech-news-9) ⭐️ 7.0/10

**财经新闻**
1. [SpaceX 逾三成季度营收来自单一客户](#item-finance-news-1) ⭐️ 7.0/10
2. [DeepSeek 第二轮融资据报达 1055 亿元](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Cursor 市场出现带后门的 Claude Code 扩展](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 8.0/10

据事件报告，Cursor 扩展市场出现了带有 SSH 后门的 Claude Code 扩展副本，风险涉及安装该恶意副本的 Cursor 用户。评论中转引的 Cursor 安全公告称，该扩展会向 SSH 的 \`authorized\_keys\` 文件追加标记为 \`svc-telemetry\` 的攻击者公钥。自称来自 Anthropic 的 Felix 在评论中表示，恶意副本并非 Anthropic 构建或发布，官方渠道版本不受影响，Anthropic 的系统和员工电脑也未遭入侵。现有摘录未给出受影响版本、完整暴露范围或攻击者最初获得市场访问权限的途径。

hackernews · \_chall · 10月30日 07:09 · [社区讨论](https://news.ycombinator.com/item?id=50300683)

**「SSH 后门的原理」** SSH 的 \`authorized\_keys\` 文件记录获准登录相应账户的公钥，写入攻击者公钥可能使其用对应私钥获得访问权限。Cursor 的安全公告将恶意扩展的行为描述为尝试安装“持久化 SSH 后门”；能否实际远程登录，仍取决于 SSH 服务是否可达及其认证配置。

**「卸载扩展不等于清除后门」** 曾从 Cursor 市场安装 Claude Code 扩展的用户应检查 \`~/.ssh/authorized\_keys\` 是否出现标记为 \`svc-telemetry\` 的公钥，发现后应移除该未授权密钥并进一步排查主机。由于后门修改了扩展之外的 SSH 授权文件，不能把卸载或更新扩展视为已经完成清理。

**「社区讨论」** 评论者 jonas21 转引公告中的排查方法，提示 macOS 用户检查 \`~/.ssh/authorized\_keys\` 是否含有 \`svc-telemetry\` 标记。另有评论者追问恶意副本如何进入市场，并对 Open VSX、Cursor 与微软扩展市场之间的受影响边界表示不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cursor.com/blog/claude-code-extension-security-notice">Security notice — malicious version of Anthropic. claude - code ...</a></li>
<li><a href="https://phorion.io/blog/offical-claude-code-vsx-compromise/">Official Claude Code Extension Compromise: Security Advisory</a></li>

</ul>
</details>

**标签**: `#supply-chain-security`, `#ide-extensions`, `#cursor`, `#claude-code`, `#ssh`

---

<a id="item-tech-news-2"></a>
### [研究报告 Azure 五例跨租户攻陷](https://www.binarysecurity.no/posts/2026/10/one-root-case) ⭐️ 8.0/10

一篇安全研究文章报告了 Microsoft Azure 的五个完整跨租户攻陷案例，涉及不同客户之间的租户隔离边界。当前材料只有标题、摘要与社区评论，没有技术正文，因此无法核实受影响的服务、利用条件、攻陷范围或修复状态，也不能据此认定发生了真实客户数据泄露。

hackernews · swq115 · 10月30日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=50301854)

**「租户隔离」** 多租户云服务的安全前提是：即使不同客户共用底层基础设施，一个客户也不能未经授权访问另一客户的数据或资源；跨租户漏洞破坏的正是这条隔离边界。当前材料缺少技术原文，不能仅凭标题和评论确定所称“五次完全跨租户攻陷”涉及的服务、权限范围或修复状态。

**「社区关注认证与访问控制」** 评论者 unddoch 另行声称，攻击者知道其他客户的租户 ID 时，可伪造 Microsoft 管理员同意（adminconsent）流程结束时的回调，并质疑仅靠文档警告不要将 tenant 参数用于认证或授权是否足够。另一位评论者提到了路径遍历和不安全直接对象引用（IDOR），但这些说法及其与五个攻陷案例的关系均无法从现有材料核实。

**标签**: `#Azure`, `#cloud security`, `#vulnerability research`, `#tenant isolation`

---

<a id="item-tech-news-3"></a>
### [Northflank 被指遭入侵，细节待核实](https://status.northflank.com/) ⭐️ 7.0/10

Hacker News 上一则投稿称托管基础设施平台 Northflank 遭到入侵，并链接至其状态页。所提供材料不含状态页正文或官方事件说明，因此无法据此确认入侵情况、攻击途径、暴露的数据或受影响客户范围。

hackernews · js4ever · 10月30日 15:10 · [社区讨论](https://news.ycombinator.com/item?id=50305025)

**「平台背景」** Northflank 是一个应用构建与部署平台，开发者可连接 Git 仓库，部署微服务、数据库和后台任务等工作负载。它提供平台即服务（PaaS），由平台承担底层基础设施管理，而非要求开发者全部自行运维。

**「社区讨论」** 评论者 dangoodmanUT 称自己已加密环境变量，并将解密密钥硬编码进应用代码，试图在平台被入侵时增加攻击者获取敏感信息的难度。这一防护思路依赖于攻击者无法取得密钥所在的代码或二进制文件，而其关于本次攻击者不具备这类访问权限的推测，未得到所提供材料的证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://northflank.com/about">About — Northflank</a></li>
<li><a href="https://northflank.com/features/platform">Platform — Features — Northflank</a></li>

</ul>
</details>

**标签**: `#security`, `#cloud-infrastructure`, `#data-breaches`, `#secrets-management`

---

<a id="item-tech-news-4"></a>
### [Nesformer 用约 1 GB Qwen 权重模拟 NES](https://github.com/dbreunig/nesformer) ⭐️ 7.0/10

GitHub 项目 Nesformer 宣称，用约 1 GB 的 Qwen 权重实现了可运行的任天堂 NES 游戏机模拟器。评论中引用的项目性能数据称，它比原版主机慢 150–290 倍，因此仍是实验性实现，而非实时游玩的实用方案。现有材料未提供独立测试，也不足以确认完整实现细节、游戏兼容范围和模拟精度。

hackernews · dbreunig · 10月30日 16:40 · [社区讨论](https://news.ycombinator.com/item?id=50306442)

**「技术背景」** Qwen 是以开放权重模型为主的语言模型系列；这里的“权重”指神经网络用于计算的数值参数。作者在评论中称，这次尝试以 Qwenputer 文章及相关源码为起点，探索能否用同类技术模拟 NES 的芯片与 RAM，而不只是生成游戏画面。

**「社区讨论」** jacquesm 等评论者欣赏这种技术探索，但认为它凸显了神经网络计算相较于传统确定性程序的效率代价。armcat 则设想将小型虚拟机、解释器和命令行工具嵌入模型权重，以减少外部工具调用；这些用途仍是社区设想，并非该项目已验证的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>

</ul>
</details>

**标签**: `#NES emulation`, `#Qwen`, `#Neural computation`, `#Computer architecture`

---

<a id="item-tech-news-5"></a>
### [Tangled 重构架构并新增组织支持](https://tangled.org/blog/forge/) ⭐️ 7.0/10

Tangled 联合创始人在发布讨论中表示，这个联邦式代码托管平台已稳定其 AT Protocol Lexicon 数据规范，全面重构架构与界面，并推出面向团队的组织支持。团队还称，用户现在更容易自托管整个技术栈或部分组件；私有仓库则计划在随后两周左右逐步推出，并非此次已交付的功能。所给材料不含文章正文，尚无法据此核实自托管的具体要求或跨平台互操作的实现程度。

hackernews · zlliang · 10月30日 15:44 · [社区讨论](https://news.ycombinator.com/item?id=50305573)

**「协议与互操作」** Tangled 使用 AT Protocol，其中 lexicon 用于定义应用数据的结构，为不同实现交换记录提供共同约定。代码协作平台之间的互操作不只是同步 Git 仓库，还涉及议题、拉取请求和评论等协作记录的组织方式与归属。

**「互操作与迁移需求」** 开发 juju.bi 的评论者希望让其公开仓库与 Tangled 互通，并追问稳定后的规范是否已将 issue、PR 和评论记录从用户作用域移至仓库作用域；所给讨论未包含这一问题的答复。另一位自托管 Gitea 用户表达了迁移代码与发布内容、同时保留 GitHub 镜像的意愿，但仍希望 git-bug 增加 Tangled 桥接以同步 issue。

**标签**: `#Code Hosting`, `#AT Protocol`, `#Federation`, `#Self-Hosting`, `#Developer Tools`

---

<a id="item-tech-news-6"></a>
### [Bunny 停用亚美尼亚节点并重签 TLS 证书](https://status.bunny.net/incidents/p6gf1by9kr7m) ⭐️ 7.0/10

据评论中转引的 Bunny 通报，Bunny 在接到基础设施供应商警报后 20 分钟内，停止向该供应商托管的亚美尼亚 CDN 节点路由流量，随后将该服务器永久移出其基础设施。供应商报告的未授权访问涉及第三方服务器管理软件；Bunny 称，调查未发现其服务器遭未授权访问的迹象，但仍不能完全排除这种可能。若该节点确实遭未授权访问，可能暴露的信息包括该服务器上的临时 CDN 缓存内容、Pull Zone 配置和 TLS 证书。作为预防措施，Bunny 已撤销并重新签发 b-cdn.net 和 bunny.run 平台域名的全部 TLS 证书。

hackernews · SondreDag · 10月30日 19:05 · [社区讨论](https://news.ycombinator.com/item?id=50308697)

**「CDN 节点与 TLS 证书」** CDN 节点除缓存内容外，也可能保存服务配置和用于 HTTPS 的 TLS 证书。HTTPS 使用 TLS 加密客户端与服务器之间的通信，并依赖受信任的服务器证书验证服务端身份，因此节点安全排查不能只关注缓存内容。

**「社区关注」** 有评论者认为，报道应突出这是供应商侧事件，避免将 Bunny 下游节点可能受影响表述为其服务器已确认失陷。另有评论者针对擦除服务器的步骤强调取证材料保全；通报摘录称已保留相关安全日志，但现有材料不足以评估取证是否完整。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/HTTPS">HTTPS - Wikipedia</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Glossary/HTTPS">HTTPS - Glossary | MDN - MDN Web Docs</a></li>

</ul>
</details>

**标签**: `#security`, `#cdn`, `#tls`, `#incident-response`, `#third-party-risk`

---

<a id="item-tech-news-7"></a>
### [Soft-MTP 提出一行梯度修正方案](https://www.reddit.com/r/MachineLearning/comments/1xjnz40/multitoken_prediction_done_right_r/) ⭐️ 7.0/10

研究作者提出 Soft Multi-Token Prediction（Soft-MTP），旨在改善大语言模型的推测解码，同时减少多词元预测（MTP）训练对下一词元预测的干扰。作者称，标准 MTP 梯度中包含有益的 KL 自蒸馏信号，但混杂了会损害下一词元预测的噪声残差。其给出的关键修改是一行代码 \`h\_ntp += h\_mtp.detach\(\) - h\_mtp\`，用于提取 KL 梯度；帖子同时提供了论文、GitHub 代码和 Hugging Face 资源链接。该帖未展示基准测试、消融实验或量化结果，因此仅凭帖子无法验证作者所称的多任务收益。

reddit · r/MachineLearning · /u/jayden\_teoh\_ · 10月30日 18:53

**「MTP 与推测解码」** 多词元预测（MTP）在常规下一词元预测（NTP）之外，增加对后续多个位置词元的预测目标。它也可为推测解码提供候选词元，但候选仍需经过目标模型验证，接受率会影响实际加速收益。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/papers/2610.38331">Paper page - Multi - Token Prediction Done Right</a></li>

</ul>
</details>

**标签**: `#llm-training`, `#multi-token-prediction`, `#speculative-decoding`, `#self-distillation`

---

<a id="item-tech-news-8"></a>
### [百度网盘 iOS 摇一摇广告被指使用磁力计](https://www.landian.news/archives/127843.html) ⭐️ 7.0/10

据蓝点网转述的开发者逆向分析，百度网盘 iOS 13.36.0 广告框架中存在 NoShake 变体：它绕开 CoreMotion，使用 Core Location 的 CLHeading 读取磁力计数据来判断手机晃动。报告称，即使禁用陀螺仪和加速度计权限，该变体仍可触发摇一摇广告跳转。报告还提到，在特定参数下，框架等待约 1 秒后会自动执行广告点击。所供材料仅为二手摘要，未附代码或完整复现条件，具体影响范围尚不明确。

telegram · zaihuapd · 10月30日 15:00

**「传感器接口的区别」** Core Motion 与 Core Location 是不同的框架，所述报告中的 CLHeading 通过后者提供磁力计方向信息。因此，限制陀螺仪和加速度计的数据访问，并不等于屏蔽所有可用于判断手机动作的信号。

**「广告审计需覆盖替代触发路径」** 对广告行为审计者而言，这份报告提示，仅检查 CoreMotion 调用可能漏掉百度网盘 iOS 13.36.0 的广告触发路径，还需核查 CLHeading 调用及特定参数下的自动点击分支。所供摘要未包含完整复现条件，实际触发范围及其他版本是否受影响仍不明确。

**标签**: `#iOS`, `#逆向工程`, `#磁力计`, `#移动广告`, `#权限控制`

---

<a id="item-tech-news-9"></a>
### [Apple 智能拟于 11 月 4 日在华开启开发者测试](https://www.apple.com.cn/newsroom/2026/10/apple-intelligence-features-are-coming-to-users-in-china/) ⭐️ 7.0/10

据附有 Apple Newsroom 链接的 Telegram 转述，Apple 智能首批功能计划于 11 月 4 日随最新 iOS 开发者 Beta 在中国开放测试，并于 12 月随 iOS 27.3 正式推出。首批功能包括实时翻译、照片消除和写作工具，不含下一代 Siri AI 功能；其他平台的支持须待必要审批后推出。帖文还称，苹果与阿里巴巴合作，将千问接入 Siri、写作工具和视觉智能，面向在中国购买支持 Apple 智能的 iPhone 的用户，或设备定位与 Apple 账户国家/地区均在中国的用户提供。所供材料未包含官方公告正文，具体上线时间与适用条件仍需以官方原文为准。

telegram · zaihuapd · 10月30日 21:44

**「模型接入与 Siri 换代」** Apple 智能是一组融入系统功能的 AI 能力，接入第三方模型与 Siri 助手本身的换代是不同层面的更新。所供 Telegram 转述将千问接入 Siri 等入口与“下一代 Siri”明确区分，不能把前者理解为后者同步上线。

**标签**: `#Apple Intelligence`, `#iOS`, `#千问`, `#生成式 AI`, `#中国市场`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [SpaceX 逾三成季度营收来自单一客户](https://www.cls.cn/detail/2519914) ⭐️ 7.0/10

据财联社报道，SpaceX 在申报文件中称，其上季度约 34.5% 的总营收来自算力业务的一名客户；知情人士称，该客户是 Anthropic。

telegram · zaihuapd · 10月30日 06:20

**「背景」** Claude 人工智能模型开发商 Anthropic 据报道于 2026 年早些时候签约，使用 SpaceX 位于田纳西州孟菲斯的数据中心计算资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#SpaceX`, `#AI算力采购`, `#营收集中度`

---

<a id="item-finance-news-2"></a>
### [DeepSeek 第二轮融资据报达 1055 亿元](https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players) ⭐️ 7.0/10

据 Telegram 帖文转述 The Information 报道，DeepSeek 第二轮融资规模达 1055 亿元人民币，高于 2026 年 6 月首轮的约 510 亿元人民币。上述信息来自二手转述，融资金额及交易完成情况仍待核实。

telegram · zaihuapd · 10月30日 12:37

**「背景」** 据该帖对 The Information 报道的转述，DeepSeek 于 2026 年 6 月完成约 510 亿元的首轮融资，其中国资背景投资者出资占比为 2%。

**标签**: `#DeepSeek`, `#企业融资`, `#企业估值`, `#国资投资`

---