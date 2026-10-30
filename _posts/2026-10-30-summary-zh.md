---
layout: default
title: "Horizon Summary: 2026-10-30 (ZH)"
date: 2026-10-30
lang: zh
---

> 从 38 条内容中筛选出 3 条重要资讯。

---

**科技新闻**
1. [Mistral 宣布发布 Large 4 模型权重](#item-tech-news-1) ⭐️ 8.0/10
2. [PHP2Shell 利用链据称攻陷 25 台服务器](#item-tech-news-2) ⭐️ 7.0/10
3. [Lean 4 证明据报确定范德瓦尔登数 w\(2;3,21\)=416](#item-tech-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Mistral 宣布发布 Large 4 模型权重](https://mistral.ai/news/mistral-large-4-oss/) ⭐️ 8.0/10

Mistral 宣布发布 Mistral Large 4 的模型权重，为希望自行部署该模型的开发者提供 API 之外的获取途径。所提供材料不含公告正文，无法核实权重的完整获取条件、部署要求或性能指标；权重发布也不应被等同于不受限制的商业使用许可。

hackernews · kuberwastaken · 10月29日 14:13 · [社区讨论](https://news.ycombinator.com/item?id=50289418)

**「权重开放与使用许可」** 模型权重是运行模型所需的训练后参数；发布权重与通过托管 API 提供访问是不同的交付方式，但权重可获取并不等于商业用途不受限制。此次评论引用的许可条款要求，经营模型即服务（MaaS）业务的使用方或其关联企业，在将模型或衍生作品用于任何商业目的前另行取得 Mistral 商业许可；由于所供材料没有完整许可文本，具体适用范围仍需核对原文。

**「商业托管需核查授权」** 计划将权重用于商业服务的企业应先核查许可证，而不能将权重发布视为不受限制的商用授权。根据评论者引用的条款，若被许可方或其关联公司经营模型即服务（MaaS）业务，在将模型或其衍生作品用于任何商业目的前，须另行与 Mistral 签订商业许可；当前材料未提供完整许可证，这一限制仍需以正式文本核实。

**「商用限制与 API 降价」** 评论者 maxloh 引述许可条款称，若被许可方或其关联方经营模型即服务（MaaS）业务，在将模型或其衍生作品用于任何商业目的之前，必须另行与 Mistral 签订商业许可，并据此质疑“开放权重”的表述；该条款尚未通过完整许可文本核实。评论者 Topfi 则称，API 每百万输入／输出 token 的价格已从预览版的 1.36／4.18 美元降至 0.70／2.10 美元，认为这一降幅值得重新评估模型的性价比，但所提供材料中没有官方价目表正文。

**标签**: `#large-language-models`, `#model-weights`, `#AI-licensing`, `#inference-pricing`

---

<a id="item-tech-news-2"></a>
### [PHP2Shell 利用链据称攻陷 25 台服务器](https://dreamgroup.com/blog/chained-php2shell-exploit-roots-25-servers) ⭐️ 7.0/10

Dream 的一篇报告声称，攻击者通过串联 PHP2Shell 漏洞利用，在 25 台服务器上取得 root 权限，其中包括美国政府系统。所提供评论引述报告称，利用链的第二阶段涉及 Linux 内核 XFRM ESP-in-TCP 子系统漏洞，用于权限提升。由于缺少文章正文，目前无法核实受害服务器数量、政府系统归属，也无法确认受影响产品、版本、利用前提或修复状态。

hackernews · 882542F3884314B · 10月29日 10:42 · [社区讨论](https://news.ycombinator.com/item?id=50286987)

**「漏洞链背景」** 漏洞链将不同漏洞串联使用：获得 PHP 应用层面的代码执行能力，并不等于已取得服务器的 root 权限，攻击者可能还需要利用本地提权漏洞。所提供的评论引用称，本次攻击的第二阶段涉及 Linux 内核的 XFRM ESP-in-TCP 子系统；但由于缺少报道正文，尚无法核实具体漏洞、受影响版本及利用条件。

**「讨论焦点」** 有评论者借 XFRM 提权环节质疑服务器默认启用非必需内核功能所带来的攻击面，并询问能否禁用相关功能，但所提供讨论没有给出经过验证的缓解办法。另有评论者依据其所称的 PAN-OS 设置和 SELinux 配置线索，猜测涉事防火墙厂商为 Palo Alto Networks；这尚非已确认的产品归属。

**标签**: `#exploit-chaining`, `#PHP`, `#Linux-kernel`, `#privilege-escalation`

---

<a id="item-tech-news-3"></a>
### [Lean 4 证明据报确定范德瓦尔登数 w\(2;3,21\)=416](https://www.reddit.com/r/MachineLearning/comments/1xivpue/w2321_416_a_van_der_waerden_number_conjectured_by/) ⭐️ 7.0/10

一则 Reddit 公告称，研究者已证明范德瓦尔登数 w\(2;3,21\)=416：对 \{1,…,416\} 的任意红蓝染色，都存在红色三项或蓝色二十一项等差数列，而 \{1,…,415\} 存在避开两者的染色；据发帖者称，这一数值由 Kullmann 于 2010 年猜想。公告描述的证明涵盖 209 个案例和 38,661,140 个叶子公式，由 Lean 4 内核检查定理，并由经 CakeML 验证的 LRAT 检查器 cake\_pr 检查各个反驳证明，再以摘要绑定至对应的 Lean 项。发帖者称证明由 Hupyy 的神经符号系统 LPM（Large Proof Model）生成，并提供预印本及 13.6 GB 的证据包，内含 Lean 源码、检查器记录和重放工具。现有材料仅为这则公告，未提供独立复核结果，也不足以判断 LPM 在证明过程中的具体贡献。

reddit · r/MachineLearning · /u/Rodriguez909 · 10月29日 20:46

**「这个数表示什么」** 这里的范德瓦尔登数 w\(2;3,21\) 指一个最小阈值 N：无论怎样将整数 1 至 N 染成红、蓝两色，都必然出现红色的三项等差数列或蓝色的二十一项等差数列。要证明它等于 416，既要证明 416 时无法避开这两种结构，也要给出 415 时能同时避开它们的染色；据帖子介绍，Kullmann 在 2010 年猜测了这一数值。

**「复核入口与限制」** 希望复核结果的形式化验证研究者可通过公告链接获取证据包；其中给出的 \`shasum -a 256 -c SHA256SUMS\` 命令仅核对文件是否与所附摘要一致，不能替代对证明及检查流程的实际重放。

**标签**: `#formal-verification`, `#automated-theorem-proving`, `#Lean-4`, `#neuro-symbolic-AI`, `#combinatorics`

---