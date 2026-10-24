---
layout: default
title: "Horizon Summary: 2026-10-24 (ZH)"
date: 2026-10-24
lang: zh
---

> 从 33 条内容中筛选出 7 条重要资讯。

---

**科技新闻**
1. [Calif 展示 iPhone 攻击演示，技术细节待公开](#item-tech-news-1) ⭐️ 7.0/10
2. [Dessa: the most authentic full-duplex speech model ever built](#item-tech-news-2) ⭐️ 7.0/10
3. [Kimi K3.1 Pro 上线 API，权重计划于 11 月 4 日前发布](#item-tech-news-3) ⭐️ 7.0/10
4. [PHP 基金会建议暂时禁用上传进度功能](#item-tech-news-4) ⭐️ 7.0/10

**财经新闻**
1. [据报欧盟取消对中国太阳能玻璃的反倾销和反补贴关税](#item-finance-news-1) ⭐️ 7.0/10
2. [三类产品 CCC 认证新规将于 11 月 1 日实施](#item-finance-news-2) ⭐️ 7.0/10
3. [国办意见提出减缓人工智能对就业的替代影响](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Calif 展示 iPhone 攻击演示，技术细节待公开](https://blog.calif.io/p/iphone) ⭐️ 7.0/10

Calif 发布了四段据其称在巴黎 Hexacon 展示的 iPhone 攻击演示，其中包括标为“Signal 单次点击”的演示，以及涉及 iMessage 的演示。作者表示后续会公开相关内容，但页面文字未提供漏洞机制、受影响的 iOS 版本、修复状态或可复现步骤，因此尚不能据此确认攻击适用范围，也不能将其视为已发布的通用越狱工具。\(\[blog.calif.io\]\(https://blog.calif.io/p/iphone\)\)

hackernews · pavel\_lishin · 10月23日 16:21 · [社区讨论](https://news.ycombinator.com/item?id=50211474)

**「演示与公开细节」** 现场展示与公开可复现的漏洞细节并不是一回事。该帖称，这些演示在巴黎 Hexacon 揭晓，完整内容将在之后发布，因此现有材料尚不能确认具体利用机制或受影响的 iPhone 版本。

**「社区关注」** 评论者关注能否获得并保留自己手机的 root 权限，以及启用“锁定模式”是否能阻止这些攻击；所提供的评论没有给出实测答案，也未证实越狱会导致苹果服务被封锁。另有评论者批评前沿 AI 模型面向安全研究的受限访问机制，认为它让圈外研究人员处于不利地位，但这属于其观点，不能据此认定本次演示使用了此类模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.calif.io/p/iphone">iPhone - Calif Newsletter</a></li>

</ul>
</details>

**标签**: `#iOS security`, `#Exploit research`, `#Jailbreaking`, `#AI-assisted security`

---

<a id="item-tech-news-2"></a>
### [Dessa: the most authentic full-duplex speech model ever built](https://block.xyz/dessa) ⭐️ 7.0/10

Dessa is presented as a full-duplex speech model with expressive conversation demos and reported local execution on high-end Apple hardware, drawing both technical enthusiasm and skepticism about its positioning.

hackernews · dsr12 · 10月23日 19:09 · [社区讨论](https://news.ycombinator.com/item?id=50213925)

**标签**: `#speech-models`, `#full-duplex-audio`, `#on-device-ai`, `#human-ai-interaction`

---

<a id="item-tech-news-3"></a>
### [Kimi K3.1 Pro 上线 API，权重计划于 11 月 4 日前发布](https://simonwillison.net/2026/Oct/23/kimi-k31-pro/) ⭐️ 7.0/10

据 Simon Willison 10 月 23 日的报道，Moonshot 已在 Kimi API 上线 Kimi K3.1 Pro，支持 low、medium、max 三档推理强度，可通过 OpenAI 兼容接口调用。标准版每百万输入 token 收费 2 美元、输出 token 收费 10 美元；官方称 Highspeed 版速度为标准版的 2—3 倍，价格翻倍，但输入缓存命中的价格不变。Moonshot 自有基准测试显示其表现接近 Claude Opus 5.5 和 GPT-6 Astra；报道另引述 Artificial Analysis 评分，Kimi 得到 55 分，高于 GPT-6 Astra 等模型的 53 分、低于 Opus 5.5 的 58 分，这些结果不等同于所有实际任务中的表现。发布时模型权重尚未开放，Moonshot 承诺于 2026 年 11 月 4 日前公布完整权重，因此目前可用的是 API 服务，而非已可下载部署的开放权重模型。

rss · Simon Willison · 10月23日 19:40

**「与 K3 的关系」** 据 Moonshot 技术博客，Kimi K3.1 Pro 是 K3 的后训练版本，采用了显著增加的后训练计算投入。理解此次发布还需区分 API 与开放权重：前者提供托管模型的调用服务，后者提供模型权重供下载和部署，因此 API 已上线不等于权重已公开。

**「接入测试需自行保存日志」** 使用 LLM 0.32 或更高版本的开发者，可通过其 OpenAI 兼容端点命令调用 Kimi K3.1 Pro，无需等待专用插件。但该命令不会自动记录调用结果；若要保留输出和推理轨迹用于评估，应像文中示例一样分别保存标准输出与标准错误。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.ai/blog/kimi-k3-1-pro">Kimi K3.1 Pro Tech Blog: Advancing Open Intelligence</a></li>

</ul>
</details>

**标签**: `#large language models`, `#AI APIs`, `#model benchmarks`, `#model weights`

---

<a id="item-tech-news-4"></a>
### [PHP 基金会建议暂时禁用上传进度功能](https://x.com/ThePHPF/status/2113580383875019242) ⭐️ 7.0/10

据所附消息，PHP 基金会建议用户在下一个 PHP 版本发布前，将 session.upload\_progress.enabled 设为 0，暂时禁用上传进度功能，以防范远程代码执行漏洞 CVE-2026-115560。消息称，只有在运行时将非默认的 serialize\_handler 切换为“php”的应用才可能受影响，并非所有 PHP 应用均受影响。所附内容未提供受影响版本范围、漏洞技术细节或修复版本的具体发布时间。

telegram · zaihuapd · 10月23日 13:46

**「受影响的配置条件」** 会话序列化处理器决定 PHP 如何编码和解码会话数据，此处的“php”是处理器名称。Red Hat 的说明进一步限定了受影响条件：应用在配置中使用 php\_binary 或 php\_serialize，随后在调用 session\_start\(\) 前，通过 ini\_set\(\) 将 session.serialize\_handler 切换为 php；并非所有启用上传进度功能的应用都符合这一条件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://access.redhat.com/security/vulnerabilities/RHSB-2026-013">RHSB-2026-013 Request handling memory corruption - php (CVE ...</a></li>

</ul>
</details>

**标签**: `#PHP`, `#安全漏洞`, `#远程代码执行`, `#会话处理`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [据报欧盟取消对中国太阳能玻璃的反倾销和反补贴关税](https://www.163.com/dy/article/L9R94K6105484D40.html) ⭐️ 7.0/10

据所提供报道，欧盟自 2026 年 10 月 22 日起取消对原产于中国的太阳能玻璃征收的反倾销和反补贴关税。报道援引欧盟解释称，欧盟境内已无活跃的太阳能玻璃生产企业，相关保护措施已失去原有目的。

telegram · zaihuapd · 10月23日 06:54

**「背景」** 欧盟曾于 2025 年 7 月 22 日启动对中国太阳能玻璃反补贴措施的到期复审，以评估现有关税到期后是否仍需继续征收。

**「退税影响」** 报道还称，相关进口商可申请退还自 2025 年 7 月 22 日起缴纳的上述关税，但退税不计利息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://eur-lex.europa.eu/eli/C/2025/4010/oj/eng">EUR-Lex - 52025XC04010 - EN - EUR-Lex</a></li>

</ul>
</details>

**标签**: `#欧盟贸易政策`, `#太阳能玻璃`, `#反倾销与反补贴`, `#中欧贸易`

---

<a id="item-finance-news-2"></a>
### [三类产品 CCC 认证新规将于 11 月 1 日实施](https://www.gelonghui.com/live/2726360) ⭐️ 7.0/10

据格隆汇报道，电动自行车、玩具和童车的 CCC 认证（强制性产品认证）新规将于 2026 年 11 月 1 日起实施。电动自行车须落实“一车一池一充一码”，出厂时配齐全部必需部件，并随车附带一致性证书。

telegram · zaihuapd · 10月23日 10:12

**「背景」** CCC 即强制性产品认证，电动自行车此前就须获得该认证才能销售；此次是升级既有认证和监督规则，并非首次设立认证要求。

**「影响」** 电动自行车认证流程须在型式试验完成后保留整车样品，直至认证证书有效期结束后至少 12 个月，获证产品还将接受跟踪检查及生产现场、口岸或市场抽样检测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gov.cn/gongbao/content/2019/content_5407678.htm">gov.cn/gongbao/content/2019/content_5407678.htm</a></li>

</ul>
</details>

**标签**: `#CCC认证`, `#电动自行车`, `#玩具与童车`, `#产品监管`, `#市场监管`

---

<a id="item-finance-news-3"></a>
### [国办意见提出减缓人工智能对就业的替代影响](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 7.0/10

据该消息转述的财联社报道，国务院办公厅印发意见，提出优先在劳动力紧缺、环境高危岗位推广人工智能，审慎把握其在劳动密集型行业的应用范围、力度和节奏。意见鼓励企业探索失业缓冲期制度，提前告知受影响劳动者并提供转岗支持；这些鼓励性措施不等于强制要求。

telegram · zaihuapd · 10月23日 12:54

**「背景」** 该意见于 2026 年 10 月 16 日成文、10 月 23 日发布，其中建立失业缓冲期属于鼓励企业探索的安排，并非统一强制要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mee.gov.cn/zcwj/gwywj/202610/t20261024_1184583.shtml">国务院办公厅关于适应人工智能技术发展助力构建就业友好型发展方式的...</a></li>
<li><a href="https://www.gov.cn/zhengce/zhengceku/202610/content_7084108.htm">国务院办公厅关于适应人工智能技术发展助力构建就业友好型发展方式的...</a></li>

</ul>
</details>

**标签**: `#人工智能`, `#就业政策`, `#劳动力市场`, `#企业用工`, `#中国政策`

---