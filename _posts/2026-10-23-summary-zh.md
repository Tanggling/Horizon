---
layout: default
title: "Horizon Summary: 2026-10-23 (ZH)"
date: 2026-10-23
lang: zh
---

> 从 44 条内容中筛选出 12 条重要资讯。

---

**科技新闻**
1. [Quad9 计划退出法国](#item-tech-news-1) ⭐️ 8.0/10
2. [Switch 2 越狱报告引发关注，技术范围尚待核实](#item-tech-news-2) ⭐️ 8.0/10
3. [研究称部分智能电视关闭 ACR 后仍上报内容相关流量](#item-tech-news-3) ⭐️ 8.0/10
4. [333 个疑遭 Ebury 后门感染的 Tor 出口中继下线](#item-tech-news-4) ⭐️ 8.0/10
5. [eMudhra 宣布计划退出全球 SSL/TLS 证书业务](#item-tech-news-5) ⭐️ 7.0/10
6. [Earstrip 宣称 489 毫秒完成 370 万个地图多边形三角剖分](#item-tech-news-6) ⭐️ 7.0/10
7. [Carbon-X 开放 148 亿参数 DNA 与文本联合模型](#item-tech-news-7) ⭐️ 7.0/10
8. [GameScaling 开放八个游戏操作模型检查点](#item-tech-news-8) ⭐️ 7.0/10
9. [Java SE JSSE 高危漏洞预警：补丁及版本范围待核实](#item-tech-news-9) ⭐️ 7.0/10

**科技博客**
1. [软件提速的关键是设计，而非语言](#item-tech-blog-1) ⭐️ 6.0/10

**财经新闻**
1. [沪深 300 据报较 6 月高点一度回落 20%](#item-finance-news-1) ⭐️ 7.0/10
2. [澳大利亚法院裁定苹果开放第三方应用安装与支付](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Quad9 计划退出法国](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

DNS 解析服务 Quad9 宣布计划退出法国，受影响的是在法国使用该服务的用户。一名自称 Quad9 首席技术官、参与相关法律事务的评论者表示，Quad9 很可能在 11 月 24 日之后使用 GeoIP（按 IP 地址判断地理位置）过滤，阻止法国用户访问其服务；这一实施方式仍是可能方案，并非已上线措施。所提供的材料不含公告正文，无法确认退出的完整范围、具体安排或法律要求。

hackernews · farrokhi · 10月22日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=50195959)

**「退出范围」** Quad9 是 DNS 解析服务商，负责将域名解析为网络地址，而非托管域名所指向的网站内容。其公告将此次退出的范围界定为：自 11 月 24 日起，不再向位于法国的用户提供免费网络安全防护服务；这并非宣布全球停运。

**「用户影响」** 如果按上述方案实施，被识别为来自法国的用户将无法继续通过 Quad9 解析域名，因此依赖该服务的用户和网络管理员需要准备替代 DNS 解析服务。

**「讨论焦点」** 讨论集中在地域封锁能否满足合规要求：这位自称 Quad9 首席技术官的评论者承认，用 GeoIP 阻止法国用户访问，与此前认为 GeoIP 不足以对特定域名实施地域性解析限制之间存在张力。另有评论者引述一段关于索尼音乐通过 VPN 绕过封锁、运营方仍被认定不合规并受罚的叙述，质疑解析服务商应承担的责任边界；所给材料不足以独立核实这一案件叙述。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://quad9.net/news/blog/au-revoir-france/">Farewell, France | Quad 9</a></li>

</ul>
</details>

**标签**: `#DNS`, `#Internet Infrastructure`, `#Internet Regulation`, `#Geoblocking`

---

<a id="item-tech-news-2"></a>
### [Switch 2 越狱报告引发关注，技术范围尚待核实](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 8.0/10

一篇题为《Jailbreaking the Switch 2》的博文报告了针对任天堂 Switch 2 的越狱，涉及主机安全与逆向工程研究。当前提供的材料不包含博文正文，因此无法核实漏洞机制、获得的权限、适用固件版本、复现条件或工具是否已公开；也不能据此认定已实现解密文件系统读写或游戏导出。

hackernews · ledoge · 10月22日 08:01 · [社区讨论](https://news.ycombinator.com/item?id=50192536)

**「越狱的权限边界」** 主机越狱的关键不仅是能否执行自定义代码，还包括代码获得哪些系统权限。原文的检索摘录将 ns2jb 描述为 Switch 2 的纯软件、需连接外部设备的越狱方案，称其可在普通系统模块及内置文件系统模块 fs 的权限下运行任意原生代码；这仍是作者的能力声明，不能据此认定游戏已可在其他硬件上运行。

**「讨论焦点：自动化实机测试」** 评论者 valgaze 引述了一套 AI 辅助实机测试方案：通过 JetKVM 让 Codex 经 USB 发送控制器输入、经 HDMI 接收画面，并用机械按键装置在主机崩溃后按下电源键；KeplerBoy 认为，这类硬件组合带来的测试自动化比争论 AI 与研究者各自的贡献更值得关注。另有评论者推测越狱可能促成游戏导出和跨硬件运行，但其前提是尚未证实的解密文件系统读写能力，不能视为已经实现的结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/">pepsipu.com</a></li>

</ul>
</details>

**标签**: `#reverse engineering`, `#console security`, `#jailbreaking`, `#AI-assisted research`

---

<a id="item-tech-news-3"></a>
### [研究称部分智能电视关闭 ACR 后仍上报内容相关流量](https://watchingthewatchers.github.io/watchingthewatchers/index.html) ⭐️ 8.0/10

一项针对美国智能电视自动内容识别（ACR）的研究称，在对 10 家厂商的 12 台电视进行 5943 次受控实验后，发现部分机型关闭 ACR 后仍上报内容相关流量。研究还称，VIDAA OS 通过明文 MQTT 发送包含不可重置设备 ID 和音频指纹的数据；Vizio WatchFree+ 则将节目名写入未加密的域名查询，且用户无法关闭这一行为。所供材料仅为研究转述，未列出受影响型号、固件版本或完整测试方法，因此无法据此确定影响范围，也不能将结果推广至所有智能电视。

telegram · zaihuapd · 10月22日 09:50

**「背景：内容识别与数据传输」** 自动内容识别（ACR）用于识别电视正在播放的内容，音频指纹是这类识别所用的数据之一。本研究涉及两个不同的隐私问题：关闭识别功能后是否仍有内容相关数据外传，以及传输是否加密；发现相关流量并不等于已经证明内容识别仍在运行。

**「隐私影响」** 对研究涉及的部分机型，关闭 ACR 不能被视为停止所有观看内容相关数据外传的保证。所报告的明文传输还意味着，能够观察相应网络流量的一方可能获取设备标识、音频指纹或节目名，而不只是接收这些数据的平台。

**标签**: `#智能电视`, `#自动内容识别`, `#隐私安全`, `#物联网安全`, `#网络流量分析`

---

<a id="item-tech-news-4"></a>
### [333 个疑遭 Ebury 后门感染的 Tor 出口中继下线](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

据该消息，一名 Tor 运营者用脚本扫描约 3000 个出口中继，发现 333 个被植入 Ebury 后门，约占扫描数量的 10%；这些中继于 10 月 4 日被标记为 BadExit，次日全部下线。消息称，受感染中继可将发往 22 端口的 SSH 连接劫持至 12 台拦截服务器并窃取凭据。攻击者据称早在今年 8 月已入侵这些服务器，并屏蔽部分端口以专门收集未加密邮件流量，但入侵途径尚无定论。所提供的转述未包含检测方法、原始证据或凭据窃取成功的具体条件，相关结论仍需结合原始报告核实。

telegram · zaihuapd · 10月22日 14:52

**「攻击范围与时间线」** KABA 原文称，Tor 全网约有 3000 个出口中继，因此这批 333 个受感染中继约占总数的 10%；这一比例指中继数量，并不等于受影响流量的比例。原文还将协同拦截 SSH 连接、收集未加密数据的行动起点记为 10 月 2 日，早于转述所列的 10 月 4 日标记与次日下线。

**「用户风险」** 对曾通过这些出口中继传输未加密邮件或建立 SSH 连接的用户而言，中继下线并不能消除此前流量可能被截获的风险；不过，现有消息不足以判断哪些用户实际受影响，也不能据此认定所有经过这些中继的 SSH 凭据均已泄露。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kaba.cx/posts/20261020_Tor/">How I got over 300 Tor exit nodes removed - KABA</a></li>

</ul>
</details>

**标签**: `#Tor`, `#Ebury 后门`, `#SSH 劫持`, `#凭据窃取`, `#网络安全`

---

<a id="item-tech-news-5"></a>
### [eMudhra 宣布计划退出全球 SSL/TLS 证书业务](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 7.0/10

eMudhra 宣布计划退出全球 SSL/TLS 证书业务，涉及其面向网站等服务提供的证书业务，而非已完成退出。此次公告受到社区对其证书颁发机构（CA）安全事件的质疑，但所供材料没有公告正文，无法确认退出时间表、现有证书的后续安排或客户迁移要求。材料也不足以确定该安全事件的具体技术原因及影响范围。

hackernews · bo0tzz · 10月22日 13:33 · [社区讨论](https://news.ycombinator.com/item?id=50195110)

**「此前的中间证书私钥事件」** 中间证书颁发机构（CA）的私钥用于签发证书，一旦泄露，攻击者就可能冒用该机构签发证书。Mozilla 在 10 月 20 日的安全公告中表示，其于 10 月 17 日收到报告，称八张 eMudhra 中间证书关联的私钥已遭泄露；这一事件构成了此次退出声明的安全背景。

**「社区关注私钥安全与问责」** 评论者主要质疑 CA 私钥安全及公司的解释是否充分；有人提供了据称是 Chrome 团队公开提问的 Bugzilla 链接，但所供材料不含问题正文。另有评论者针对其引述的“受影响 CA 未签发终端实体证书”说法指出，这并不能排除他人利用受影响 CA 签发证书的风险；这一质疑不等于已有伪造证书的证据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.mozilla.org/security/2026/10/20/protecting-firefox-users-following-the-compromise-of-emudhra-intermediate-certificates/">Protecting Firefox users following the compromise of eMudhra ...</a></li>

</ul>
</details>

**标签**: `#TLS`, `#public-key-infrastructure`, `#certificate-authorities`, `#security`

---

<a id="item-tech-news-6"></a>
### [Earstrip 宣称 489 毫秒完成 370 万个地图多边形三角剖分](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 7.0/10

这篇面向地图渲染与计算几何开发者的文章介绍了多边形三角剖分库 Earstrip，宣称其速度超过 Earcut，并在 489 毫秒内处理了 370 万个地图多边形。当前提供的材料没有原文正文，也未包含实现细节、测试硬件、输入复杂度或对照测试方法，因此这一数字只能视为文章的性能主张，不能据此认定它在其他数据集或部署环境中同样领先。

hackernews · molind · 10月22日 09:31 · [社区讨论](https://news.ycombinator.com/item?id=50193170)

**「算法与运行环境」** 多边形三角剖分将地图中的多边形拆成三角形；Earcut 使用的“耳切法”通过逐步切下符合条件的三角形完成这一过程。理解 Earstrip 的性能主张还需区分运行环境：原文称，原生运行时 earcut.hpp 比 Earstrip 慢 14%，而编译为 WebAssembly 并在 V8 中运行后，两者的性能损失分别为 67% 和 23%；这些是作者报告的结果，并非独立验证。

**「速度之外的取舍」** 自称 Earcut 作者的 mourner 表示有兴趣借鉴优化，但也指出 Earcut 为控制体积而主动放弃过部分优化；据他介绍，其 JavaScript 版本压缩并经 gzip 后为 4.1 KB，对 Mapbox GL JS 等实际应用已足够快，因此他关心 Earstrip 的 WASM 构建体积。另有评论者质疑优化后的耳切法为何比理论复杂度更优的方法更普及；自称 Delaunay32 作者的评论者则希望参与比较，但明确表示尚未在该数据集上测试，且其当前多边形 API 要求简单环与互不接触的孔洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://globus.software/blog/2026/10/16/cutting-map-polygons/">Faster than earcut : triangulating 3.7M map polygons in 489 ms</a></li>

</ul>
</details>

**标签**: `#computational-geometry`, `#polygon-triangulation`, `#performance-optimization`, `#geospatial`

---

<a id="item-tech-news-7"></a>
### [Carbon-X 开放 148 亿参数 DNA 与文本联合模型](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 7.0/10

据介绍，Carbon-X 是一款开放权重的 148 亿参数纯解码器模型，联合训练 DNA 与文本，可在普通聊天中接收原始 DNA 序列并用英语回答。它将文本与 DNA 放入同一 token 流，以 6-mer 编码 DNA，中期训练使用了 3020 亿 token；权重采用 Apache 2.0 许可，据称以 bfloat16 精度可装入单张 80 GB GPU。帖子援引 Hugging Face 数据称，在关闭思考模式时，该模型在五项 DNA 基准上的平均得分为 66.7%，对比 GPT-6.1 Sol 的 67.5%，但所给材料没有独立验证这一比较，也未证实其在私有变异数据集上的泛化表现。

reddit · r/MachineLearning · /u/jatingargiitk · 10月22日 12:32

**「DNA 如何进入聊天模型」** Carbon-X 将 DNA 序列与自然语言放在同一 token 流中训练，其中 DNA 使用 6-mer（六碱基片段）作为编码单位。模型卡描述的交互方式是将原始 DNA 放入普通聊天，由模型用英语回答突变性质、基因调控区域或序列所属生物类别等问题，而不只是生成 DNA 序列。

**「本地部署与使用边界」** 对拥有相应 GPU 资源的基因组研究团队，这提供了在本地处理敏感序列、减少向外部服务传输数据的可选路径，但并不构成临床可用性证明：模型尚未经过临床验证，模型卡也明确建议将精确序列操作交给代码处理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/HuggingFaceBio/Carbon-X/blob/main/README.md">README.md · HuggingFaceBio/Carbon-X at main</a></li>

</ul>
</details>

**标签**: `#DNA language models`, `#Genomics`, `#Open-weight models`, `#Local inference`

---

<a id="item-tech-news-8"></a>
### [GameScaling 开放八个游戏操作模型检查点](https://arxiv.org/abs/2610.28698v1) ⭐️ 7.0/10

据条目介绍，米哈游崩坏 AI 团队联合清华大学等发布 GameScaling，基于 Qwen3.5 视觉语言模型进行键鼠操作继续预训练，模型规模覆盖 0.8B 至 27B 参数，每次输出未来 200 毫秒的键鼠动作。项目以 Apache-2.0 许可证开放八个模型检查点和推理客户端，但未提供训练代码。论文通过 120 组训练配置考察数据量、数据多样性与模型规模，报告称增加数据可改善同源表现，提高数据多样性有助于迁移到相近游戏，但对差异较大的游戏世界提升有限。所附内容未给出具体基准成绩或对照结果，因此尚不能据此判断其相对现有方法的性能优势。

telegram · zaihuapd · 10月22日 11:32

**「从视觉理解到游戏控制」** GameScaling 将视觉语言模型用于游戏控制：输入当前游戏画面及短期的历史画面、动作，输出键鼠操作，而非仅生成文字回答。项目说明显示，每次输出覆盖未来约 200 毫秒，其中键盘动作分为 6 个约 33 毫秒的步骤，鼠标移动与滚轮操作则按整个动作片段给出。

**「可试用，但训练复现受限」** 开发者可利用已开放的检查点和推理客户端开展游戏操作推理测试，但由于缺少训练代码，现有发布内容不足以直接复现论文的训练流程及扩展规律实验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/THUSI-Lab/GameScaling">GitHub - THUSI-Lab/GameScaling: Scaling in Games: Continued ...</a></li>

</ul>
</details>

**标签**: `#游戏智能体`, `#视觉语言模型`, `#模型扩展规律`, `#迁移学习`, `#开源模型`

---

<a id="item-tech-news-9"></a>
### [Java SE JSSE 高危漏洞预警：补丁及版本范围待核实](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 7.0/10

所提供的 Telegram 消息称，Oracle 已为 Java SE 的 JSSE 组件漏洞 CVE-2026-91403 发布修复补丁；该漏洞 CVSS 评分为 9.1，攻击者无需身份验证即可通过网络远程利用，可能损害数据机密性与完整性。消息列出的受影响版本包括 Java SE 8u511、11.0.33、17.0.21、21.0.13、25.0.5、27.0.1，以及未具体列明的多个 GraalVM 版本。当前材料仅包含转述与 Oracle 公告链接，未提供公告原文，因此漏洞编号、评分、版本范围及补丁可用性均尚未独立核实，具体触发条件也不明确。

telegram · zaihuapd · 10月22日 12:30

**「补丁涉及证书信任」** Oracle 公告说明，此次 Java 更新的具体措施是不再信任一组与 eMudhra 相关的受影响中间 CA 证书，而非仅笼统描述为 JSSE 漏洞修复。这补充了 Telegram 摘要未交代的证书信任背景；公告给出的应对方式是更新至最新 Java 版本，或应用其推荐的缓解措施。

**「维护建议」** 维护上述 Java SE 或 GraalVM 环境的团队应先核对所链接的 Oracle 公告，确认实际受影响版本及修复版本后安排升级；这份转述未给出补丁版本号，不能单凭其版本清单确定升级目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.oracle.com/security-alerts/alert-cve-2026-91403.html">Oracle Security Alert Advisory - CVE-2026-91403</a></li>

</ul>
</details>

**标签**: `#Java SE`, `#JSSE`, `#漏洞预警`, `#补丁管理`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [软件提速的关键是设计，而非语言](https://seangoedecke.com/software-is-slow-because-of-bad-design-not-slow-languages/) ⭐️ 6.0/10

rss · Sean Goedecke · 10月23日 00:00

**「背景」** 面对用 AI 将软件重写为 C、Rust 或汇编的热潮，Sean Goedecke 认为，语言执行速度的差距通常不会等比例转化为程序提速。他指出，许多程序的瓶颈是等待数据库、网络或磁盘，而非执行代码，因此换语言未必触及主要耗时。

**「方案」** 作者用一个假设说明阿姆达尔定律：若请求耗时的一半用于数据库查询，即使其余代码瞬间完成，整体也最多提速两倍。计算密集型任务也可能早已通过原生库或 GPU 执行，重写外围 Python 代码并不能加快这些计算。设计差异则可能改变结果：他援引一例 C 到 Rust 的改写，原本预期变慢，实际却快了 30%，原因归结于 B 树比二叉搜索树更适合缓存；他自己的主要优化收益也来自缓存、异步或并行执行、合并 N+1 查询以及跳过不必要的工作。

**「启示」** 作者主张，AI 优化应先测量性能、定位热点，再重新设计程序做什么、如何做，而不是先整体换语言。只有热点确实受 CPU 限制、又无法通过减少工作量改善时，局部改用更快语言才是有针对性的选择。

**标签**: `#software performance`, `#Amdahl’s law`, `#software design`, `#profiling`, `#programming languages`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [沪深 300 据报较 6 月高点一度回落 20%](https://www.bloomberg.com/news/articles/2026-10-22/china-stocks-set-for-bear-market-as-ai-trade-policy-hopes-fade) ⭐️ 7.0/10

据 Telegram 帖文转述彭博报道，沪深 300 指数于 2026 年 10 月 22 日较同年 6 月高点一度累计回落 20%，触及通常所称的熊市门槛，即指数从近期高点下跌 20%。该行情数据未获独立核实。

telegram · zaihuapd · 10月22日 05:05

**「背景」** 市场通常将主要股指较近期高点下跌约 20%称为进入“技术性熊市”，这里的比较基准是沪深 300 指数的 6 月高点，并不意味着每只 A 股都下跌了 20%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbctv18.com/market/chinese-stock-market-in-bear-territory-after-20-fall-from-june-peak-20016636.htm">Chinese stock market in &#x27;bear territory&#x27; after 20% fall from ...</a></li>

</ul>
</details>

**标签**: `#A股`, `#沪深300`, `#科技股`, `#企业业绩`, `#财政政策`

---

<a id="item-finance-news-2"></a>
### [澳大利亚法院裁定苹果开放第三方应用安装与支付](https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/) ⭐️ 7.0/10

据所供的 9to5Mac 报道转述，澳大利亚联邦法院裁定，苹果须自 2027 年 3 月 1 日起允许澳区 iPhone 用户通过第三方应用商店和网站安装应用，并开放替代支付方式及外部支付链接。裁决源于 Epic 的反垄断诉讼；苹果表示将上诉并申请暂缓执行，实施进程仍有不确定性。

telegram · zaihuapd · 10月22日 06:54

**「背景」** 据报道，此次裁决源于游戏开发商 Epic Games 的反垄断诉讼，法院认定苹果利用其在 iPhone 应用分发和支付市场的强大地位限制竞争，违反澳大利亚竞争法。

**「直接影响」** 若裁决按期执行，澳区 iPhone 用户将获得 App Store 之外的应用安装渠道，开发者也可提供苹果支付体系之外的付款选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/">Apple must open iPhone to alternative app stores in Australia ...</a></li>

</ul>
</details>

**标签**: `#苹果`, `#澳大利亚反垄断`, `#应用分发`, `#应用内支付`

---