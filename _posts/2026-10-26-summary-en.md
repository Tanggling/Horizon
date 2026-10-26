---
layout: default
title: "Horizon Summary: 2026-10-26 (EN)"
date: 2026-10-26
lang: en
---

> From 28 items, 4 important content pieces were selected

---

**Technology News**
1. [Brotli Vulnerability Affects Node.js and Python HTTP Components](#item-tech-news-1) ⭐️ 8.0/10
2. [Specialized CNN Beats Frontier LLMs on Skin-Lesion Classification](#item-tech-news-2) ⭐️ 7.0/10
3. [Nanbeige releases Apache 2.0 33B teacher model for agent development](#item-tech-news-3) ⭐️ 7.0/10
4. [Apple reportedly set to unveil its first touchscreen MacBook Pro](#item-tech-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Brotli Vulnerability Affects Node.js and Python HTTP Components](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 8.0/10

CVE-2026-111497, a Google Brotli decoder vulnerability rated CVSS 4.0 9.2, reportedly affects Brotli versions 1.0.3 through 1.2.0 and related Node.js and Python HTTP components. The source says unauthenticated remote attackers can send crafted compressed streams that may cause memory corruption, sensitive-data disclosure, process crashes, or potentially arbitrary code execution. Python users should upgrade Brotli to 1.2.1 and brotlicffi to 1.2.1.0; Node.js fixes are listed as 22.23.4, 24.22.1, and 26.12.1.

telegram · zaihuapd · Oct 25, 02:42

**「Background」** Node2Shell, HTTP2Shell, and Python2Shell refer to the same CVE-2026-111497 flaw in Google’s reference C Brotli decoder, rather than separate vulnerabilities. Python applications may be exposed indirectly because HTTP libraries such as requests, urllib3, httpx, and aiohttp can use Brotli when it is installed, even if the application does not import it directly. 

**「Required upgrade」** Organizations using Brotli-based Node.js or Python HTTP components should inventory their dependencies and upgrade to the fixed versions—Python Brotli 1.2.1, brotlicffi 1.2.1.0, or Node.js 22.23.4, 24.22.1, or 26.12.1—because affected versions may permit a crafted compressed stream to cause an out-of-bounds write, crash, memory disclosure, or remote code execution.

<details><summary>References</summary>
<ul>
<li><a href="https://bytemuni.com/cyber-security/http2shell-brotli-cve-2026-111497/">HTTP2Shell (CVE-2026-111497): Brotli Bug Beyond Node.js</a></li>
<li><a href="https://strobes.co/blog/http2shell-brotli-rce-cve-2026-111497/">HTTP2Shell: Brotli RCE in Node . js and Python</a></li>
<li><a href="https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497">Node 2Shell Brotli vuln ( CVE - 2026 - 111497 ) evolves to HTTP2Shell, as...</a></li>

</ul>
</details>

**Tags**: `#安全漏洞`, `#Brotli`, `#Node.js`, `#Python`, `#HTTP`

---

<a id="item-tech-news-2"></a>
### [Specialized CNN Beats Frontier LLMs on Skin-Lesion Classification](https://lynchlab.net/llm-skin-cancer) ⭐️ 7.0/10

A controlled benchmark reported that a roughly 10-year-old, specialized convolutional neural network classified skin lesions more accurately than frontier large language models. The evaluation used a held-out test set of 200 lesions, but its narrow medical-imaging task, small test set, and benchmark-specific design limit how broadly the result can be generalized.

hackernews · sungam · Oct 25, 17:15 · [Discussion](https://news.ycombinator.com/item?id=50233779)

**「Specialized versus general models」** A convolutional neural network \(CNN\) is designed to recognize visual patterns, while a frontier large language model \(LLM\) is a general-purpose system that is not necessarily specialized for medical-image classification. In this comparison, the CNN identified the correct diagnosis for 125 of 200 biopsy-proven lesions, versus 84 and 85 for the two LLMs, across six possible diagnoses.【tool-1-1】

**「Practical consequence」** For developers building skin-lesion screening systems, the result supports evaluating or fine-tuning a vision model for the specific task rather than assuming that a more general-purpose frontier LLM will perform best; the benchmark does not establish clinical usefulness or justify deployment on its own.

**「Community debate」** Commenters generally viewed the result as unsurprising: a model trained specifically for lesion classification should outperform a general-purpose model on that task. Others argued that LLMs may still add value by incorporating clinical notes, asking follow-up questions, or handling imperfect and out-of-distribution images, while one commenter criticized the tightly optimized benchmark as “benchmaxxing.”

<details><summary>References</summary>
<ul>
<li><a href="https://lynchlab.net/llm-skin-cancer">A 10 - year - old CNN outperforms frontier LLMs for skin... | Lynch Lab</a></li>

</ul>
</details>

**Tags**: `#AI evaluation`, `#computer vision`, `#medical AI`, `#neural networks`

---

<a id="item-tech-news-3"></a>
### [Nanbeige releases Apache 2.0 33B teacher model for agent development](https://www.reddit.com/r/MachineLearning/comments/1xf6x35/nanbeige_releases_nanbeige4333b_an_apache_20/) ⭐️ 7.0/10

Nanbeige has released Nanbeige4.3-33B, an Apache 2.0-licensed model intended as a teacher for smaller agents, including a planned 3B model. Its model card lists a 512K-token context window, and the team reports 80.9 on Terminal-Bench 2.1 versus 73.0 for Qwen3.8-27B, but 60.3 versus 61.7 on SWE-Bench Pro. These results come from the releasing team and have not been independently replicated; the evaluations also preserve earlier reasoning with \`preserve\_thinking=true\`.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 25, 16:32

**「Teacher models and distillation」** A teacher model is a larger model used to provide examples, reasoning traces, or other training signals for smaller student models. Nanbeige is positioning this 33B release as the teacher for a planned 3B agent, so its value depends not only on standalone benchmark scores but also on whether its outputs can support effective distillation.

**「Practical consideration」** Developers reproducing the reported multi-turn tool-use results should match the model&\#x27;s \`preserve\_thinking=true\` setting and compare both task success and total generated tokens, since the setting may affect reasoning behavior and inference cost; it is not recommended for general chat.

**Tags**: `#open-source AI`, `#language models`, `#AI agents`, `#benchmarking`, `#model distillation`

---

<a id="item-tech-news-4"></a>
### [Apple reportedly set to unveil its first touchscreen MacBook Pro](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 7.0/10

Apple is reportedly preparing to unveil its first touchscreen MacBook Pro on Wednesday, with OLED displays, a Dynamic Island, and 14-inch and 16-inch models. The touchscreen is expected to supplement the keyboard and trackpad rather than replace them, while pricing is said to exceed the current model’s $2,499 starting price. The report remains unverified, and detailed specifications, pricing, and availability have not been confirmed.

telegram · zaihuapd · Oct 25, 14:25

**「此前进展」** 此前的报道已将这款产品描述为苹果首款触屏 Mac，并称苹果确认于 10 月 28 日举行发布活动；因此，本次消息仍属于发布前的计划与报道，而非已经上市的产品事实。\[tool-2-2\]

**「购买成本可能上升」** 如果此次发布属实，准备购买 MacBook Pro 的用户需要预留高于现款 2,499 美元起售价的预算；MacRumors 还报道称，苹果已在 2026 年 6 月将 Mac 产品价格至少上调 300 美元，但触屏 OLED 机型的最终定价仍未确认。

<details><summary>References</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-10-19/apple-announces-oct-28-event-for-touch-screen-macbook-pro">Apple Announces Oct. 28 Event for Touch - Screen MacBook Pro</a></li>
<li><a href="https://www.macrumors.com/guide/touchscreen-macbook-pro/">Apple&#x27;s Touchscreen OLED MacBook Pro: Everything We Know</a></li>

</ul>
</details>

**Tags**: `#苹果`, `#MacBook Pro`, `#OLED`, `#触控交互`, `#笔记本电脑`

---