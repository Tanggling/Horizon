---
layout: default
title: "Horizon Summary: 2026-10-24 (EN)"
date: 2026-10-24
lang: en
---

> From 33 items, 7 important content pieces were selected

---

**Technology News**
1. [Calif reports iPhone hacking demos involving Signal and iMessage](#item-tech-news-1) ⭐️ 7.0/10
2. [Dessa: the most authentic full-duplex speech model ever built](#item-tech-news-2) ⭐️ 7.0/10
3. [Kimi K3.1 Pro launches on API, with weights promised by November 4](#item-tech-news-3) ⭐️ 7.0/10
4. [PHP Foundation Advises Temporarily Disabling Upload Progress](#item-tech-news-4) ⭐️ 7.0/10

**Financial News**
1. [Report: EU ends tariffs on Chinese solar glass](#item-finance-news-1) ⭐️ 7.0/10
2. [New CCC rules for e-bikes and children’s products take effect November 1](#item-finance-news-2) ⭐️ 7.0/10
3. [China Seeks to Limit AI-Related Job Displacement](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Calif reports iPhone hacking demos involving Signal and iMessage](https://blog.calif.io/p/iphone) ⭐️ 7.0/10

Calif says it presented four iPhone-hacking demonstrations at Hexacon in Paris, including one labeled “Signal 1-click” and another involving iMessage. Its October 16 post promises a later release but supplies no exploit mechanisms, affected iOS versions, or mitigation details in the accompanying text. The post therefore does not establish a publicly available jailbreak or independently verified exploit capabilities. \(\[blog.calif.io\]\(https://blog.calif.io/p/iphone\)\)

hackernews · pavel\_lishin · Oct 23, 16:21 · [Discussion](https://news.ycombinator.com/item?id=50211474)

**「Demonstrations, Not Full Disclosure」** Calif presents the work as a series of demonstrations shown at Hexacon in Paris, including a Signal “1-click” demo and an iMessage demo, with releases promised later. The supplied excerpt does not establish the exploit mechanisms, affected iOS versions, or whether Lockdown Mode would block the attacks.

**「Device control and unanswered defenses」** Commenters ask whether Lockdown Mode blocks the demonstrated attacks and whether root access could survive Apple updates; the supplied discussion answers neither question, while one participant worries that jailbreaking could jeopardize access to Apple services. Another commenter argues that restricted access to frontier AI models disadvantages outside security researchers, but the comments do not establish which models, if any, were used for these demonstrations.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.calif.io/p/iphone">iPhone - Calif Newsletter</a></li>

</ul>
</details>

**Tags**: `#iOS security`, `#Exploit research`, `#Jailbreaking`, `#AI-assisted security`

---

<a id="item-tech-news-2"></a>
### [Dessa: the most authentic full-duplex speech model ever built](https://block.xyz/dessa) ⭐️ 7.0/10

Dessa is presented as a full-duplex speech model with expressive conversation demos and reported local execution on high-end Apple hardware, drawing both technical enthusiasm and skepticism about its positioning.

hackernews · dsr12 · Oct 23, 19:09 · [Discussion](https://news.ycombinator.com/item?id=50213925)

**Tags**: `#speech-models`, `#full-duplex-audio`, `#on-device-ai`, `#human-ai-interaction`

---

<a id="item-tech-news-3"></a>
### [Kimi K3.1 Pro launches on API, with weights promised by November 4](https://simonwillison.net/2026/Oct/23/kimi-k31-pro/) ⭐️ 7.0/10

Moonshot released Kimi K3.1 Pro on its API on October 23, 2026, priced at $2 per million input tokens and $10 per million output tokens; Simon Willison tested its OpenAI-compatible endpoint with low, medium, and max reasoning settings. Moonshot also offers a Highspeed variant advertised as 2–3 times faster at twice the standard price, except cached input tokens, which retain the same pricing. Willison reports an Artificial Analysis score of 55, ahead of GPT-6 Astra, Claude Fable 5.1, and Gemini 4 Argon at 53 but behind Claude Opus 5.5 at 58; Moonshot’s separate claims of comparable performance come from its own benchmarks. Model weights were not available at launch: Moonshot promises to release the full weights by November 4, 2026.

rss · Simon Willison · Oct 23, 19:40

**「Built on Kimi K3」** Moonshot describes Kimi K3.1 Pro as a post-trained version of Kimi K3, with substantially more compute devoted to post-training. K3 is therefore the direct predecessor behind the launch’s before-and-after capability comparisons.

**「API Evaluation, Not Yet Self-Hosting」** Developers can evaluate Kimi K3.1 Pro using existing OpenAI-compatible tooling, as Willison demonstrates with LLM’s openai endpoint command. Organizations requiring self-hosting cannot deploy it from model weights yet; November 4, 2026 is Moonshot’s promised release deadline, not confirmed availability.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.ai/blog/kimi-k3-1-pro">Kimi K3.1 Pro Tech Blog: Advancing Open Intelligence</a></li>

</ul>
</details>

**Tags**: `#large language models`, `#AI APIs`, `#model benchmarks`, `#model weights`

---

<a id="item-tech-news-4"></a>
### [PHP Foundation Advises Temporarily Disabling Upload Progress](https://x.com/ThePHPF/status/2113580383875019242) ⭐️ 7.0/10

According to the supplied report, the PHP Foundation recommends setting \`session.upload\_progress.enabled\` to \`0\` until the next PHP release to mitigate a remote code execution vulnerability identified as CVE-2026-115560. The report says only applications that switch from a non-default session serialization handler to \`php\` at runtime may be affected. It does not identify affected PHP versions, provide technical vulnerability details, or specify a fix release date.

telegram · zaihuapd · Oct 23, 13:46

**「The Configuration Behind the Risk」** The relevant distinction is between the session serializer configured initially and the one selected at runtime. Red Hat describes the affected configuration as session.serialize\_handler initially set to php\_binary or php\_serialize, then changed to php using ini\_set\(\) before session\_start\(\)—not simply an application using the default php serializer.

<details><summary>References</summary>
<ul>
<li><a href="https://access.redhat.com/security/vulnerabilities/RHSB-2026-013">RHSB-2026-013 Request handling memory corruption - php (CVE ...</a></li>

</ul>
</details>

**Tags**: `#PHP`, `#安全漏洞`, `#远程代码执行`, `#会话处理`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Report: EU ends tariffs on Chinese solar glass](https://www.163.com/dy/article/L9R94K6105484D40.html) ⭐️ 7.0/10

According to the report, the EU removed trade-protection tariffs of up to 84.2% on Chinese solar glass effective October 22, 2026, saying there were no longer any active EU producers to protect.

telegram · zaihuapd · Oct 23, 06:54

**「Background」** On July 22, 2025, the EU opened a review of whether to retain duties on Chinese solar glass aimed at offsetting government subsidies.

**「Impact」** Importers can apply for refunds of the affected duties paid since July 22, 2025, without interest, the report says.

<details><summary>References</summary>
<ul>
<li><a href="https://eur-lex.europa.eu/eli/C/2025/4010/oj/eng">EUR-Lex - 52025XC04010 - EN - EUR-Lex</a></li>

</ul>
</details>

**Tags**: `#欧盟贸易政策`, `#太阳能玻璃`, `#反倾销与反补贴`, `#中欧贸易`

---

<a id="item-finance-news-2"></a>
### [New CCC rules for e-bikes and children’s products take effect November 1](https://www.gelonghui.com/live/2726360) ⭐️ 7.0/10

China’s market regulator will implement upgraded China Compulsory Certification \(CCC\) rules for electric bicycles, toys and children’s vehicles on November 1, 2026; e-bikes must follow a “one vehicle, one battery, one charger, one code” system, leave factories with all required components, and face tighter post-certification checks.

telegram · zaihuapd · Oct 23, 10:12

**「Background」** China already requires electric bicycles to obtain CCC, its compulsory product certification, before they can be sold, so the changes tighten an existing approval system.

**「Impact」** Manufacturers and certification holders will face additional compliance work, including retaining tested vehicle samples until at least 12 months after certificate expiry and undergoing factory, port or market sampling.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gov.cn/gongbao/content/2019/content_5407678.htm">gov.cn/gongbao/content/2019/content_5407678.htm</a></li>
<li><a href="https://news.dahe.cn/2026/06-02/2094122.html">电动自行 车 、 童 车 类 产 品 、 玩 具 迎来新版 强 制 性 产 品 认 证 实 施 规 则 -大河网</a></li>

</ul>
</details>

**Tags**: `#CCC认证`, `#电动自行车`, `#玩具与童车`, `#产品监管`, `#市场监管`

---

<a id="item-finance-news-3"></a>
### [China Seeks to Limit AI-Related Job Displacement](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 7.0/10

China’s State Council General Office issued an opinion aimed at limiting AI-related job displacement, prioritizing AI use in labor-shortage and high-risk jobs while urging caution over its scale and pace in labor-intensive industries; it also encourages companies to explore a buffer period for affected workers, give advance notice and provide transition and job-placement support.

telegram · zaihuapd · Oct 23, 12:54

**「Background」** The guidance, published on October 23, 2026, encourages companies to explore a buffer period before AI-related job losses, with advance notice and help moving to other work; it does not make that measure mandatory.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gov.cn/zhengce/zhengceku/202610/content_7084108.htm">国务院办公厅关于适应人工智能技术发展助力构建就业友好型发展方式的...</a></li>

</ul>
</details>

**Tags**: `#人工智能`, `#就业政策`, `#劳动力市场`, `#企业用工`, `#中国政策`

---