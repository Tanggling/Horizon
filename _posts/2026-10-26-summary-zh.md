---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 28 条内容中筛选出 4 条重要资讯。

---

**科技新闻**
1. [Brotli 高危漏洞影响 Node.js 与 Python 组件](#item-tech-news-1) ⭐️ 8.0/10
2. [十年前的 CNN 在皮肤癌分类基准中胜过前沿 LLM](#item-tech-news-2) ⭐️ 7.0/10
3. [Nanbeige 发布 33B Apache 2.0 教师模型](#item-tech-news-3) ⭐️ 7.0/10
4. [苹果据报道将发布首款触屏 OLED MacBook Pro](#item-tech-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Brotli 高危漏洞影响 Node.js 与 Python 组件](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 8.0/10

据 Aikido Security，CVE-2026-111497 影响 Brotli 1.0.3 至 1.2.0，CVSS 4.0 评分为 9.2。远程未认证攻击者可通过发送特制压缩流，触发内存损坏、敏感数据泄露、进程崩溃或潜在任意代码执行；受影响范围包括 Node.js 和 Python HTTP 相关组件。Python Brotli 应升级至 1.2.1，brotlicffi 应升级至 1.2.1.0；Node.js 的修复版本为 22.23.4、24.22.1 或 26.12.1。

telegram · zaihuapd · 10月25日 02:42

**「漏洞背景」** CVE-2026-111497 的根源是 Google 参考实现中的 C 语言 Brotli 解码器越界写入；“Node2Shell”“HTTP2Shell”和“Python2Shell”是围绕同一漏洞出现的不同称呼，而非彼此独立的漏洞。\[1\] 在 Python 环境中，即使应用未直接导入 Brotli，requests、urllib3、httpx 或 aiohttp 等 HTTP 组件也可能在检测到相关库已安装时自动使用它，因此依赖链可能扩大实际受影响范围。\[2\]

**「升级受影响依赖」** 使用受影响 Brotli 解码器的 Python 服务可能在处理攻击者提交的压缩数据时发生越界写入，进而导致进程崩溃、内存泄露或远程代码执行；维护者应将 Python 的 Brotli 升级至 1.2.1、brotlicffi 升级至 1.2.1.0，并检查其他 HTTP 组件是否仍依赖 1.0.3 至 1.2.0 版本。该漏洞的 CWE 记录包含未检查返回值和越界写入，相关资料将其评为 CVSS 4.0 9.2 的严重漏洞。 

<details><summary>参考链接</summary>
<ul>
<li><a href="https://phoenix.security/http2shell-node2shell-cve-2026-111497-brotli-decoder-out-of-bounds-write/">HTTP2Shell CVE-2026-111497: Brotli RCE in Node.js and Python ...</a></li>
<li><a href="https://bytemuni.com/cyber-security/http2shell-brotli-cve-2026-111497/">HTTP2Shell (CVE-2026-111497): Brotli Bug Beyond Node.js</a></li>
<li><a href="https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497">Node 2Shell Brotli vuln ( CVE - 2026 - 111497 ) evolves to HTTP2Shell, as...</a></li>
<li><a href="https://broccoli2shell.com/">Brotli decoder RCE ( CVE - 2026 - 111497 ) in Node . js , Python and more</a></li>

</ul>
</details>

**标签**: `#安全漏洞`, `#Brotli`, `#Node.js`, `#Python`, `#HTTP`

---

<a id="item-tech-news-2"></a>
### [十年前的 CNN 在皮肤癌分类基准中胜过前沿 LLM](https://lynchlab.net/llm-skin-cancer) ⭐️ 7.0/10

这篇文章称，在受控的皮肤病变分类评测中，一款约十年前的专用 CNN 比前沿 LLM 表现更好。评测使用了独立留出的 200 个病变样本；文章强调，模型训练和测试数据控制使这些样本及同一病变或患者的其他照片未被用于训练、验证或阈值选择。该结果只说明专用视觉模型在这一特定医学影像任务上的表现，不能直接推导出其在临床诊断或更广泛任务中优于通用 LLM。

hackernews · sungam · 10月25日 17:15 · [社区讨论](https://news.ycombinator.com/item?id=50233779)

**「背景」** 卷积神经网络（CNN）是专门处理图像模式的模型，通常会针对特定任务和数据集进行微调；通用大语言模型则并非主要为皮肤病灶图像分类设计。该比较使用了 200 个经活检确认的病灶，并要求模型从 6 种诊断中选择，因此考察的是一个范围明确的图像分类任务，而不是完整的临床诊断流程。

**「实际影响」** 开发皮肤病变筛查系统时，不能仅因模型更新或参数规模更大就替换经过任务专门训练的分类器；在考虑部署前，仍需用代表真实使用场景的数据验证泛化能力，并进行临床和安全评估。

**「社区争议」** 评论者普遍认为，专门模型在狭窄任务上胜过通用模型并不意外，并将其类比为计算器更擅长算术；也有人质疑这种针对固定基准的优化可能属于“刷榜”，或指出 LLM 若能结合病历、主动询问患者并处理低质量或分布外图像，评测结论可能不同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lynchlab.net/llm-skin-cancer">A 10 - year - old CNN outperforms frontier LLMs for skin... | Lynch Lab</a></li>

</ul>
</details>

**标签**: `#AI evaluation`, `#computer vision`, `#medical AI`, `#neural networks`

---

<a id="item-tech-news-3"></a>
### [Nanbeige 发布 33B Apache 2.0 教师模型](https://www.reddit.com/r/MachineLearning/comments/1xf6x35/nanbeige_releases_nanbeige4333b_an_apache_20/) ⭐️ 7.0/10

Nanbeige 发布了 Nanbeige4.3-33B，定位为训练更小型智能体（包括计划中的 3B 模型）的教师模型，权重采用 Apache 2.0 许可证，模型卡标称支持 512K 上下文。发布团队称，该模型在 Terminal-Bench 2.1 中得分 80.9，高于其对 Qwen3.8-27B 的 73.0；但在 SWE-Bench Pro 中为 60.3，低于后者的 61.7。上述结果来自发布方评测，尚无独立复现。

reddit · r/MachineLearning · /u/jatingargiitk · 10月25日 16:32

**「背景」** 在模型蒸馏中，教师模型通常先生成带有推理过程或工具使用轨迹的示例，再用于训练参数更小、部署成本更低的学生模型。Nanbeige 将 Nanbeige4.3-33B 定位为这一流程中的教师模型，并计划据此开发更小的智能体模型。

**「使用注意事项」** 开发者若要复现其多轮工具调用结果，应注意评测保留了此前推理内容，并使用了 preserve\_thinking=true；该设置不适用于一般聊天。比较部署效果时，还应在相同设置下同时记录任务成功率和生成 Token 总量，而不能仅依据单项基准分数选择模型。

**标签**: `#open-source AI`, `#language models`, `#AI agents`, `#benchmarking`, `#model distillation`

---

<a id="item-tech-news-4"></a>
### [苹果据报道将发布首款触屏 OLED MacBook Pro](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 7.0/10

据报道，苹果将于本周三发布首款支持触控和 OLED 屏幕的 MacBook Pro，提供 14 英寸和 16 英寸版本，并加入灵动岛设计。报道还称，新机起售价将高于现款 2499 美元；目前这些信息仍属于发布前报道，具体规格和价格需等待苹果正式公布。

telegram · zaihuapd · 10月25日 14:25

**「此前进展」** 彭博社此前报道称，苹果计划在今年秋季推出首款触屏 Mac，并在屏幕顶部加入灵动岛；10 月 19 日，苹果确认将于 10 月 28 日举行发布会，计划展示首款触屏 MacBook。上述信息说明本次发布并非临时传闻，但具体配置仍应以正式发布为准。

**「购买预算需上调」** 若报道属实，准备购买新款 MacBook Pro 的用户应按高于现款 2499 美元起售价的预算规划，并等待苹果公布正式价格；相关报道还称，苹果已在 2026 年 6 月将 Mac 产品价格至少上调 300 美元，但这不等同于新机的最终涨幅。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-02-24/apple-s-touch-screen-macbook-pro-to-have-dynamic-island-new-interface">Apple ’s Touch - Screen Laptop to Have Dynamic Island ... - Bloomberg</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-10-19/apple-announces-oct-28-event-for-touch-screen-macbook-pro">Apple Announces Oct. 28 Event for Touch - Screen MacBook Pro</a></li>
<li><a href="https://www.macrumors.com/guide/touchscreen-macbook-pro/">Apple&#x27;s Touchscreen OLED MacBook Pro: Everything We Know</a></li>

</ul>
</details>

**标签**: `#苹果`, `#MacBook Pro`, `#OLED`, `#触控交互`, `#笔记本电脑`

---