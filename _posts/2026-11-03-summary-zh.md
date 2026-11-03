---
layout: default
title: "Horizon Summary: 2026-11-03 (ZH)"
date: 2026-11-03
lang: zh
---

> 从 47 条内容中筛选出 11 条重要资讯。

---

**科技新闻**
1. [vLLM v0.33.0rc3 停发 CUDA 12.9 制品](#item-tech-news-1) ⭐️ 7.0/10
2. [Ubuntu 内核漏洞补丁被指延迟近三周](#item-tech-news-2) ⭐️ 7.0/10
3. [LightMIS：面向边缘设备的 13.1 万参数医学分割模型](#item-tech-news-3) ⭐️ 7.0/10
4. [ChatGPT 修复可泄露私密对话的分享链接漏洞](#item-tech-news-4) ⭐️ 7.0/10
5. [WIRED：逾 400 个 AI 应用与网站被指暗藏色情深伪](#item-tech-news-5) ⭐️ 7.0/10

**科技博客**
1. [读写权重不等于超人研究](#item-tech-blog-1) ⭐️ 6.0/10
2. [受众俘获：流量与真实目标](#item-tech-blog-2) ⭐️ 5.0/10

**财经新闻**
1. [甲骨文拟融资扩建人工智能业务，Marvell 达成收购协议](#item-finance-news-1) ⭐️ 7.0/10
2. [Marvell 同意收购 Lumentum，雅诗兰黛上调盈利预期](#item-finance-news-2) ⭐️ 7.0/10
3. [Anthropic 据报更新上市招股书](#item-finance-news-3) ⭐️ 7.0/10
4. [英国拟将多数移民永居申请年限延至 10 年](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [vLLM v0.33.0rc3 停发 CUDA 12.9 制品](https://github.com/vllm-project/vllm/releases/tag/v0.33.0rc3) ⭐️ 7.0/10

vLLM 发布 v0.33.0rc3 候选版，发布说明称 CUDA 版 wheel 和容器镜像改为仅提供 CUDA 13.0，停止发布 CUDA 12.9 wheel 及 \`-cu129\`、\`-cu129-ubuntu2404\` 镜像，依赖这些旧制品的部署需调整安装或拉取配置。依赖版本升级至 PyTorch 2.14.0、torchvision 0.29.0 和 Triton 3.8.0，项目同时称 CUDA wheel 与 libtorch 之间的 ABI 现已稳定。新增模型支持包括 Reflection Beam-1.0 及其 DFlash2 草稿模型、Yandex AliceAI-Foundation-80B-A3B 和 Recursive Flint 等。随附说明列出了 v0.33.0 正式版制品，但保留了链接与标签的核验待办，部署前应确认实际可用的版本，不能将本次候选版发布视为正式版已全部上线。

github · khluu · 11月2日 10:10

**「理解两层兼容性」** libtorch 是 PyTorch 的 C++ 库，其 ABI（应用二进制接口）约定编译后组件之间的交互方式，关系到 vLLM 原生扩展与 PyTorch 的二进制兼容性。它与 CUDA 运行环境的兼容性是不同问题：libtorch ABI 稳定并不意味着同一预编译包可以在任意 CUDA 环境下运行。

**「CUDA 部署需调整升级配置」** 固定使用官方 CUDA 12.9 wheel 或 \`-cu129\`／\`-cu129-ubuntu2404\` 镜像标签的部署，升级时需改用默认 CUDA 13.0 构建，并先核验宿主机驱动兼容性。v0.33.0rc3 仍是候选版本，建议先在测试环境验证；暂无法迁移的生产环境应保留已验证的旧版构建。

**标签**: `#vLLM`, `#LLM inference`, `#CUDA`, `#PyTorch`, `#ABI compatibility`

---

<a id="item-tech-news-2"></a>
### [Ubuntu 内核漏洞补丁被指延迟近三周](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 7.0/10

一则 Hacker News 投稿声称，截至投稿时，Ubuntu 已近三周未为一项 Linux 内核远程代码执行（RCE）漏洞发布补丁。链接路径提及 Ubuntu LTS 和 CVE-2026-98432，但当前材料没有原文或官方安全公告。因此，漏洞编号、受影响版本、利用条件及“近三周未修补”的说法均无法据此核实。

hackernews · majorchord · 11月2日 18:39 · [社区讨论](https://news.ycombinator.com/item?id=50341462)

**「漏洞机制与修复状态」** AlmaLinux 公告称，CVE-2026-98432 是 Linux 内核建立入站 IPv4 TCP 连接时的“释放后使用”漏洞，即代码访问已释放的内存；内核 CVE 团队将其评为 CVSS 9.8，攻击无需权限或用户交互。所提供的 Ubuntu 官方跟踪页摘录仅显示 Ubuntu 26.10 的相关内核条目处于“易受攻击、修复中”状态，不足以确认各 LTS 版本的修复进度，也无法核实标题所称的“近三周未修复”。

**「临时过滤不能视为已修复」** Ubuntu 管理员不应将评论中的 iptables 规则视为已验证的修复方案，采用前需核对所用内核是否受影响以及规则的适用性。Red Hat 为 CVE-2026-98432 提供了 nftables 缓解步骤，并说明升级到修复版内核后应移除规则，但现有材料不足以证明这些措施在 Ubuntu 上能完全阻断利用。

**「缓解措施的有效性存疑」** 一位评论者声称，可在 iptables 的 raw 表 PREROUTING 链使用 u32 丢包规则阻止漏洞利用，但所给材料未验证其效果。另一位评论者转述 Red Hat 对其缓解方案的说明，称该方案只能降低暴露风险、无法完全防止利用，并质疑这一限制为何未获充分解释。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ubuntu.com/security/CVE-2026-98432">CVE - 2026 - 98432 | Ubuntu</a></li>
<li><a href="https://almalinux.org/blog/2026-10-30-cve-2026-98432/">CVE - 2026 - 98432 : Patched kernels available in testing | AlmaLinux OS</a></li>
<li><a href="https://access.redhat.com/security/vulnerabilities/RHSB-2026-016">RHSB-2026-016 Use-after-free - kernel IPv4 (CVE-2026-98432)</a></li>

</ul>
</details>

**标签**: `#linux-kernel`, `#ubuntu`, `#remote-code-execution`, `#patch-management`, `#network-security`

---

<a id="item-tech-news-3"></a>
### [LightMIS：面向边缘设备的 13.1 万参数医学分割模型](https://www.reddit.com/r/MachineLearning/comments/1xm8dbo/lightmis_ultralightweight_medical_image/) ⭐️ 7.0/10

研究团队公开了 LightMIS，一款面向边缘设备的二维医学图像二值分割模型，含 13.1 万个参数，直接聚合编码器的多尺度特征，不使用可学习的逐级解码器。作者报告，在采用 nnU-Net v2.3.1 统一训练与评估流程、覆盖 6 个数据集和 5 种成像模态的实验中，其按模态计算的宏平均 Dice 和 IoU 接近 nnWNet，而参数量和 GFLOPs 分别减少 98.14% 和 94.58%。在作者的真实设备测试中，完整 LightMIS 在 Arm Mali-G52 MC2 GPU 上的推理速度约为 nnWNet 的 10.5 倍，所有 LightMIS 变体均实现 100% GPU 算子覆盖，没有回退至 CPU 执行。

reddit · r/MachineLearning · /u/OkLion2068 · 11月2日 20:22

**「任务与评测背景」** 二维二分类医学图像分割需要逐像素区分目标与背景，而不只是对整张图像作分类。文中的 nnU-Net v2.3.1 用于统一各模型的训练与评估流程，nnWNet 则是对照模型。论文采用五折交叉验证，覆盖 DRIVE、Kvasir-SEG、DSB18、BUSI、ISIC-2017 和 ISIC-2018 六个数据集。

**「部署与复现」** 代码、模型检查点和复现细节均已公开，开发者可在自有数据和目标设备上复现实验，评估部署可行性。帖文未列出各数据集的具体精度，跨模态平均指标接近并不代表每个任务上都与 nnWNet 相当。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.28327">[ 2609 . 28327 ] LightMIS : Ultra-Lightweight Medical Image Segmentation...</a></li>

</ul>
</details>

**标签**: `#medical-image-segmentation`, `#edge-ai`, `#efficient-neural-networks`, `#gpu-inference`

---

<a id="item-tech-news-4"></a>
### [ChatGPT 修复可泄露私密对话的分享链接漏洞](https://www.parameter.ai/labs/we-found-a-gap-at-openai) ⭐️ 7.0/10

据所附消息，OpenAI 已于 10 月 26 日修复 Parameter 研究团队发现的 ChatGPT 分享链接漏洞，风险涉及打开恶意分享链接的已登录用户。该漏洞利用预览功能与图表组件之间的消息处理缺陷，使攻击者能够在用户会话中执行代码、读取私密对话并将数据发送至外部服务器，受害者无需安装应用。材料称 OpenAI 将漏洞定级为 P1，并向研究团队支付了 5,000 美元赏金。现有内容未提供复现及权限范围细节，不足以确认原文标题所称的完整账号接管。

telegram · zaihuapd · 11月2日 10:24

**「分享链接与会话权限」** ChatGPT 的正常分享功能允许用户将一段对话发布为链接，供他人查看。Parameter 的技术说明称，此次攻击载荷以 chatgpt.com 的身份运行，能访问查看者已登录的网页会话；关键区别在于，它利用的是查看者的会话权限，而非仅展示分享者公开的对话。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.parameter.ai/labs/we-found-a-gap-at-openai">Do the Math: How We Took Over ChatGPT Accounts - Parameter</a></li>

</ul>
</details>

**标签**: `#ChatGPT`, `#漏洞研究`, `#会话安全`, `#数据泄露`

---

<a id="item-tech-news-5"></a>
### [WIRED：逾 400 个 AI 应用与网站被指暗藏色情深伪](https://www.wired.com/story/hundreds-of-mundane-ai-apps-are-hiding-abusive-deepfake-features/) ⭐️ 7.0/10

据材料转述的 WIRED 调查，400 多个关联 AI 应用与网站被指以宠物画像、语言学习等普通工具为掩护，在特定条件下加载色情深度伪造界面，允许用户上传他人照片生成露骨图像或视频。研究人员通过代码、域名及广告追踪发现其关联；9 月仍在 Google Play 上架的 27 款应用累计下载超过 35 万次，不少被标为适合所有年龄。苹果收到 WIRED 提供的线索后下架了 19 款应用，并称开发者在审核通过后替换远端网页内容；谷歌在被联系前已移除多数涉事应用。Meta 表示已阻止相关 209 款应用投放广告，这属于广告限制，并不等于将这些应用下架。

telegram · zaihuapd · 11月2日 12:45

**「远端内容的审核盲区」** 应用若通过远端网页提供界面，实际显示的内容就不完全固定在送审的安装包中。材料转述的苹果回应称，涉事开发者在审核通过后替换了远端网页内容，这解释了为什么送审时展示的普通工具界面未必反映上架后的实际功能。

**标签**: `#AI安全`, `#色情深度伪造`, `#应用商店审核`, `#平台治理`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [读写权重不等于超人研究](https://seangoedecke.com/llms-are-not-superhuman-at-reading-and-writing-neural-network-weights/) ⭐️ 6.0/10

rss · Sean Goedecke · 11月3日 00:00

**「背景」** 一篇论文报告，GPT-6 Astra 能从权重识别小网络所玩的游戏，还能直接修改 8 亿参数 Qwen 模型以改善数学表现。Sean Goedecke 质疑，这是否足以证明可能引发递归自我改进的“超人 AI 研究能力”。

**「方案」** 游戏网络的输入已对应网格位置，并标注“玩家”“移动物体”等类别；对每个输入连接到首层的 32 个权重求 L2 范数并画成热图，就能显出球拍位置或迷宫布局等线索。作者认为，Astra 不运行代码就能计算范数，展示的是超人心算，而非超人研究。Qwen 的瓶颈则是推理超过 32k token 后陷入循环，测试中需要更短推理的题，原模型已全部答对。Astra 在可使用 Python 的条件下构造四对循环与非循环文本，通过残差激活差异定位促成循环的权重，逐步削弱并测试，最终消除循环，让模型能继续长程解题；作者将此归为熟悉的激活引导式修复。

**「启示」** 在 Goedecke 看来，直接改权重类似手写机器码：低层操作能力令人印象深刻，却不意味着研究范式改变；他主张，LLM 对 AI 研究的主要帮助仍将来自改进常规训练，而非直接微调权重的奇技。

**标签**: `#LLM capabilities`, `#Neural network interpretability`, `#Weight editing`, `#Activation steering`

---

<a id="item-tech-blog-2"></a>
### [受众俘获：流量与真实目标](https://seangoedecke.com/audience-capture/) ⭐️ 5.0/10

rss · Sean Goedecke · 11月3日 00:00

**「背景」** Sean Goedecke 担心网络写作中的“受众俘获”：平台不断展示并奖励阅读量和互动数，诱使有工程师心态的他优化这些数字。可它们只是代理指标；他真正想要的是认真思考的读者、有经验者的反馈，以及善于思考和写作的声誉。

**「方案」** 他以批评微服务的文章为假设：追逐热点可能让流量持续上升，却因重复抨击赶走认真读者，换来只点击、不阅读的人，而指标无法区分这两类受众。同理，工程师可能忙于提升 Jira 工单指标，却偏离真正有助于晋升的工作；晋升本身是目的还是做好技术工作的手段，则取决于个人目标。他认为，自己一些热门的行业感慨只是给读者提供了焦虑出口；相比之下，他喜欢的技术解释文章常常少人关注。浏览量能扩大触达，却不足以判断是否吸引了目标读者，为此他仍主要依靠自己的品味和少量深入回复。

**「启示」** 作者并不反对为收入或机会作出妥协；关键在于清醒地知道自己换来了什么，而不是习惯性地牺牲真实目标，赢下一个已不能带来所需价值的指标游戏。

**标签**: `#audience capture`, `#proxy metrics`, `#incentive design`, `#engineering culture`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [甲骨文拟融资扩建人工智能业务，Marvell 达成收购协议](https://www.cnbc.com/2026/11/02/stocks-making-the-biggest-moves-midday-orcl-spcx-tem-rivn.html) ⭐️ 7.0/10

甲骨文向美国证券交易委员会提交的文件显示，公司拟发行 100 亿美元新股及 100 亿美元优先偿付债券，为人工智能扩建计划筹资。另据 CNBC 报道，Marvell 已同意以股票支付方式收购激光器制造商 Lumentum，交易价值 1,150 亿美元，预计于 2028 年上半年完成。

rss · CNBC Finance · 11月2日 20:00

**「背景」** 据双方公告，Marvell 拟以自身股票而非现金支付收购款；按两家公司 2026 年 10 月 28 日、收购传闻出现前的收盘价计算，每股收购价较 Lumentum 当时股价高约 23.9%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://investor.marvell.com/news-events/press-releases/detail/1040/marvell-and-lumentum-to-combine-creating-a-category-leader-in-ai-connectivity">Marvell and Lumentum to Combine, Creating a Category Leader ...</a></li>

</ul>
</details>

**标签**: `#Corporate financing`, `#Mergers and acquisitions`, `#Corporate earnings`, `#AI infrastructure`, `#Equity markets`

---

<a id="item-finance-news-2"></a>
### [Marvell 同意收购 Lumentum，雅诗兰黛上调盈利预期](https://www.cnbc.com/2026/11/02/stocks-making-the-biggest-moves-premarket-crwd-rivn-mu.html) ⭐️ 7.0/10

据 CNBC 报道，Marvell 同意收购 Lumentum，交易全部以股票支付，对后者估值为 1150 亿美元。雅诗兰黛公布第一财季剔除部分项目影响后的每股收益为 72 美分，高于 FactSet 调查的分析师预期 51 美分，并上调全财年盈利预期。

rss · CNBC Finance · 11月2日 12:49

**「背景」** 据《纽约时报》，Marvell 收购 Lumentum 是在押注光网络技术（利用光信号传输数据）将在人工智能数据中心建设中发挥关键作用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/02/technology/marvell-lumentum-115-billion-merger-ai.html">Driven by A.I. Boom, Marvell and Lumentum Announce $ 115 Billion ...</a></li>

</ul>
</details>

**标签**: `#Mergers and acquisitions`, `#Corporate earnings`, `#Premarket trading`, `#Analyst upgrades`, `#Memory stocks`

---

<a id="item-finance-news-3"></a>
### [Anthropic 据报更新上市招股书](https://www.cnbc.com/2026/11/02/anthropic-ant-s-1-quarter-financials.html) ⭐️ 7.0/10

据该 Telegram 消息援引 CNBC 报道，Anthropic 更新上市招股书，披露 2026 年前三季度净亏损 1040 亿美元，上年同期亏损 251 亿美元。公司称，上半年亏损主要受部分负债重新估值影响，并不完全代表实际经营现金消耗。

telegram · zaihuapd · 11月2日 15:12

**「背景」** 据该消息转述，公司称 2026 年上半年净亏损主要受部分债务和金融合约的账面价值变化影响，并不完全代表经营中实际消耗的现金。

**标签**: `#Anthropic`, `#IPO`, `#企业财报`, `#AI基础设施`, `#公允价值变动`

---

<a id="item-finance-news-4"></a>
### [英国拟将多数移民永居申请年限延至 10 年](https://www.gov.uk/government/news/home-secretary-unveils-new-rules-for-migrants-settling-in-the-uk) ⭐️ 7.0/10

英国内政部提出定居改革方案，拟将多数移民申请永久居留的标准年限由 5 年延长至 10 年。方案拟为部分高收入者及医生、护士、教师等公共服务岗位人员设置较短申请通道。

telegram · zaihuapd · 11月2日 23:50

**「背景」** 英国内政部提出的“凭贡献定居”框架，拟按收入和公共服务岗位等因素区分永久居留的等待年限，并设定守法、英语及税费缴纳要求。

**「现有移民的过渡安排」** 政府咨询参与者担忧，若新规不设过渡安排，并适用于已按现行规则等待永久居留的签证持有人，可能打乱他们原有的定居计划。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gov.uk/government/news/home-secretary-unveils-new-rules-for-migrants-settling-in-the-uk">Home Secretary unveils new rules for migrants settling in the UK - GOV.UK</a></li>
<li><a href="https://assets.publishing.service.gov.uk/media/6ae88073232b813648f37545/earned-settlement-public-consultation-findings-021126.pdf">Earned Settlement: Public Consultation analysis - GOV.UK</a></li>

</ul>
</details>

**标签**: `#英国移民政策`, `#永久居留`, `#劳动力市场`, `#公共服务`

---