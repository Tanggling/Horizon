---
layout: default
title: "Horizon Summary: 2026-10-30 (EN)"
date: 2026-10-30
lang: en
---

> From 38 items, 3 important content pieces were selected

---

**Technology News**
1. [Mistral announces Large 4 weights release](#item-tech-news-1) ⭐️ 8.0/10
2. [Report claims PHP2Shell chain gained root on 25 servers](#item-tech-news-2) ⭐️ 7.0/10
3. [Reported Lean 4 proof establishes van der Waerden number w\(2;3,21\) = 416](#item-tech-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Mistral announces Large 4 weights release](https://mistral.ai/news/mistral-large-4-oss/) ⭐️ 8.0/10

Mistral has announced the release of Mistral Large 4’s weights, making the model available beyond API access, according to the announcement title. The supplied material does not include the announcement text, so deployment requirements, performance claims, and full licensing terms cannot be verified here. A license excerpt quoted by a commenter says that users whose company or affiliates operate a Model-as-a-Service business must obtain a separate commercial license from Mistral before using the model or its derivatives for any commercial purpose.

hackernews · kuberwastaken · Oct 29, 14:13 · [Discussion](https://news.ycombinator.com/item?id=50289418)

**「Weights and licensing」** Model weights are the learned parameters needed to run a trained model, so releasing them enables deployment outside a provider’s hosted API. Access to weights does not itself grant unrestricted commercial rights: a commenter quotes a license clause requiring businesses that operate a Model-as-a-Service offering to obtain a separate commercial license before any commercial use of the model or its derivatives.

**「Commercial hosting requires a license check」** Companies offering Model-as-a-Service should check the Large 4 license before commercial use: a clause quoted in the supplied discussion requires a separate Mistral commercial license if the user or any affiliate operates such a business, including for commercial use of derivative works. The full license was not supplied, so this restriction should be verified rather than assuming that access to the weights permits unrestricted commercial deployment.

**「Pricing and licensing」** One commenter reports API pricing of $0.70 per million input tokens and $2.10 per million output tokens, down from preview prices of $1.36 and $4.18 respectively, and argues that the reduction warrants reevaluating the model’s competitiveness. Another argues that calling the release “open weight” is misleading given the quoted Model-as-a-Service restriction; the supplied material does not independently verify either the pricing or the complete license.

**Tags**: `#large-language-models`, `#model-weights`, `#AI-licensing`, `#inference-pricing`

---

<a id="item-tech-news-2"></a>
### [Report claims PHP2Shell chain gained root on 25 servers](https://dreamgroup.com/blog/chained-php2shell-exploit-roots-25-servers) ⭐️ 7.0/10

A Dream report claims that a chained PHP2Shell exploit gained root access on 25 servers, including US government systems. A quotation in the supplied discussion describes a second-stage Linux kernel vulnerability in the XFRM ESP-in-TCP subsystem, reportedly used for privilege escalation. The article body is unavailable, so the compromise count, government involvement, affected products, and remediation details cannot be verified from the supplied material.

hackernews · 882542F3884314B · Oct 29, 10:42 · [Discussion](https://news.ycombinator.com/item?id=50286987)

**「How the exploit chain fits together」** An exploit chain combines vulnerabilities so that an initial compromise can lead to greater access, such as escalating from an application’s privileges to root. Supplied comments describe a Linux kernel vulnerability in the XFRM ESP-in-TCP subsystem as the second stage in this case, but the missing article body prevents verification of the exact vulnerabilities and affected configurations.

**「Attack surface and vendor speculation」** One commenter questioned whether unused Linux networking features should be enabled by default and asked whether XFRM could be disabled; the supplied comments provide no validated mitigation. Another inferred that the unnamed firewall vendor was Palo Alto Networks from an alleged PAN-OS setting and SELinux configuration, but that identification remains community speculation.

**Tags**: `#exploit-chaining`, `#PHP`, `#Linux-kernel`, `#privilege-escalation`

---

<a id="item-tech-news-3"></a>
### [Reported Lean 4 proof establishes van der Waerden number w\(2;3,21\) = 416](https://www.reddit.com/r/MachineLearning/comments/1xivpue/w2321_416_a_van_der_waerden_number_conjectured_by/) ⭐️ 7.0/10

A Reddit announcement reports a formally checked proof that the van der Waerden number w\(2;3,21\) equals 416, resolving a value it says Kullmann conjectured in 2010. This means every red-blue colouring of \{1, …, 416\} contains a red three-term or blue 21-term arithmetic progression, while at least one colouring of \{1, …, 415\} contains neither. According to the announcement, Hupyy’s neuro-symbolic Large Proof Model produced a Lean 4 theorem covering 209 cases and 38,661,140 leaf formulas, with refutations checked by cake\_pr, an LRAT checker verified in CakeML, and linked by digest to Lean terms. The post links a preprint and a 13.6 GB evidence package, but the supplied material provides no independent verification of the result or assessment of the model’s contribution.

reddit · r/MachineLearning · /u/Rodriguez909 · Oct 29, 20:46

**「What the number means」** The van der Waerden number w\(2;3,21\) is the smallest N for which every red-blue colouring of the integers from 1 through N contains either a red three-term arithmetic progression or a blue 21-term arithmetic progression. Establishing an exact value therefore requires both an unavoidable-progression proof at N and a colouring that avoids both progressions at N−1. According to the announcement, Kullmann conjectured the value 416 in 2010.

**「Evidence available for scrutiny」** Researchers can obtain the linked evidence package, which the announcement says includes Lean sources, checker records and a replay kit, to scrutinize the claimed proof. The suggested command, \`shasum -a 256 -c SHA256SUMS\`, checks file integrity against the supplied checksums; it does not itself replay or validate the mathematical proof.

**Tags**: `#formal-verification`, `#automated-theorem-proving`, `#Lean-4`, `#neuro-symbolic-AI`, `#combinatorics`

---