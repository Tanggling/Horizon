---
layout: default
title: "Horizon Summary: 2026-11-03 (EN)"
date: 2026-11-03
lang: en
---

> From 47 items, 11 important content pieces were selected

---

**Technology News**
1. [vLLM v0.33.0rc3 drops CUDA 12.9 artifacts and upgrades PyTorch](#item-tech-news-1) ⭐️ 7.0/10
2. [Ubuntu kernel RCE patch delay alleged on Hacker News](#item-tech-news-2) ⭐️ 7.0/10
3. [LightMIS targets edge medical segmentation with 131K parameters](#item-tech-news-3) ⭐️ 7.0/10
4. [OpenAI reportedly patches ChatGPT shared-link flaw that could expose private chats](#item-tech-news-4) ⭐️ 7.0/10
5. [WIRED reports hidden sexual deepfake features across 400-plus AI apps and sites](#item-tech-news-5) ⭐️ 7.0/10

**Technology Blog**
1. [Reassessing Claims of Superhuman Neural Network Weight Editing](#item-tech-blog-1) ⭐️ 6.0/10
2. [Audience Capture and Proxy Metrics](#item-tech-blog-2) ⭐️ 5.0/10

**Financial News**
1. [Oracle plans AI financing; Marvell agrees to buy Lumentum](#item-finance-news-1) ⭐️ 7.0/10
2. [Marvell agrees to $115 billion Lumentum deal](#item-finance-news-2) ⭐️ 7.0/10
3. [Anthropic IPO filing reportedly shows wider losses](#item-finance-news-3) ⭐️ 7.0/10
4. [UK proposes longer wait for permanent residency](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [vLLM v0.33.0rc3 drops CUDA 12.9 artifacts and upgrades PyTorch](https://github.com/vllm-project/vllm/releases/tag/v0.33.0rc3) ⭐️ 7.0/10

The vLLM inference engine has published v0.33.0rc3, a release candidate whose notes specify upgrades to PyTorch 2.14.0, torchvision 0.29.0 and Triton 3.8.0. NVIDIA release wheels and images move to CUDA 13.0 only, ending publication of CUDA 12.9 variants; the project also describes its CUDA wheel as libtorch ABI-stable. New model support includes Reflection Beam-1.0 with its DFlash2 drafter, Yandex AliceAI-Foundation-80B-A3B and Recursive Flint, while AMD builds default to ROCm 10.0 with ROCm 7.2 variants retained. The supplied notes are truncated and list final v0.33.0 artifact tags still marked for verification, so they do not establish that those stable-release downloads are available.

github · khluu · Nov 2, 10:10

**「Deployment compatibility」** vLLM distributes its model-serving software as prebuilt Python wheels and container images for specific compute backends, including CUDA. A stable libtorch application binary interface \(ABI\) is intended to keep compiled components compatible across supported versions of PyTorch’s C++ library without recompilation; it does not remove separate CUDA compatibility requirements.

**「CUDA deployment migration」** Deployment scripts selecting CUDA 12.9 wheels or \`-cu129\`/\`-cu129-ubuntu2404\` images need to switch to the default CUDA 13.0 artifacts to adopt this release candidate. Validate host compatibility and confirm artifact availability before rollout: the rc3 notes list final-version \`v0.33.0\` tags and still mark artifact URLs and tags for verification.

**Tags**: `#vLLM`, `#LLM inference`, `#CUDA`, `#PyTorch`, `#ABI compatibility`

---

<a id="item-tech-news-2"></a>
### [Ubuntu kernel RCE patch delay alleged on Hacker News](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 7.0/10

A Hacker News submission alleges that Ubuntu LTS kernels have remained unpatched for nearly three weeks against a Linux kernel remote-code-execution vulnerability, identified in the linked URL as CVE-2026-98432. No article text or official advisory content is supplied, so the affected releases, exploit conditions, current patch availability, and claimed delay remain unverified.

hackernews · majorchord · Nov 2, 18:39 · [Discussion](https://news.ycombinator.com/item?id=50341462)

**「Vulnerability context」** AlmaLinux describes CVE-2026-98432 as a use-after-free in the Linux kernel code that establishes incoming IPv4 TCP connections, with a critical CVSS score of 9.8. The supplied Ubuntu security-tracker excerpt lists Ubuntu 26.10 as vulnerable with work in progress, but does not establish Ubuntu LTS patch status or verify the alleged three-week delay.

**「Verify mitigations before relying on them」** Ubuntu administrators should not treat the firewall command posted in the comments as a confirmed fix: the supplied evidence does not establish its effectiveness or identify affected Ubuntu kernel builds. Red Hat documents a mitigation for CVE-2026-98432 and instructs users to remove it after installing a fixed kernel, but that does not establish the commenter’s rule as suitable protection for Ubuntu.

**「Mitigation discussion」** Commenter debinguy claims an iptables u32 drop rule in raw PREROUTING can block exploitation, while majorchord reports that Red Hat describes a separate mitigation as reducing exposure rather than fully preventing exploitation. The supplied discussion does not establish either mitigation’s effectiveness for Ubuntu systems.

<details><summary>References</summary>
<ul>
<li><a href="https://ubuntu.com/security/CVE-2026-98432">CVE - 2026 - 98432 | Ubuntu</a></li>
<li><a href="https://almalinux.org/blog/2026-10-30-cve-2026-98432/">CVE - 2026 - 98432 : Patched kernels available in testing | AlmaLinux OS</a></li>
<li><a href="https://access.redhat.com/security/vulnerabilities/RHSB-2026-016">RHSB-2026-016 Use-after-free - kernel IPv4 (CVE-2026-98432)</a></li>

</ul>
</details>

**Tags**: `#linux-kernel`, `#ubuntu`, `#remote-code-execution`, `#patch-management`, `#network-security`

---

<a id="item-tech-news-3"></a>
### [LightMIS targets edge medical segmentation with 131K parameters](https://www.reddit.com/r/MachineLearning/comments/1xm8dbo/lightmis_ultralightweight_medical_image/) ⭐️ 7.0/10

The LightMIS authors have released a 131K-parameter model for 2D binary medical image segmentation on edge devices that aggregates multiscale encoder features directly, without a learned stage-wise decoder. Across six datasets and five imaging modalities, they report modality-macro Dice and IoU averages close to nnWNet, with 98.14% fewer parameters and 94.58% fewer GFLOPs under the same nnU-Net v2.3.1 training and evaluation protocol. On an Arm Mali-G52 MC2 GPU, the authors report roughly 10.5× faster inference than nnWNet for the full model; all LightMIS variants achieved 100% GPU operator coverage without CPU fallback. The post does not provide exact accuracy scores, per-dataset results, or absolute inference times.

reddit · r/MachineLearning · /u/OkLion2068 · Nov 2, 20:22

**「Task and evaluation context」** Binary medical image segmentation labels each pixel as belonging to a target region or the background; Dice and IoU measure overlap between predicted and reference masks. The authors’ paper specifies five-fold cross-validation under a common nnU-Net v2.3.1 protocol on six datasets: DRIVE, Kvasir-SEG, DSB18, BUSI, ISIC-2017 and ISIC-2018.

**「Deployment considerations」** Public code, checkpoints, and reproduction details allow developers to evaluate LightMIS on their own 2D binary segmentation tasks. Developers targeting other hardware still need to verify operator support and performance, because the Mali-G52 MC2 benchmark does not establish the same speedup or GPU-only execution elsewhere.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.28327">[ 2609 . 28327 ] LightMIS : Ultra-Lightweight Medical Image Segmentation...</a></li>

</ul>
</details>

**Tags**: `#medical-image-segmentation`, `#edge-ai`, `#efficient-neural-networks`, `#gpu-inference`

---

<a id="item-tech-news-4"></a>
### [OpenAI reportedly patches ChatGPT shared-link flaw that could expose private chats](https://www.parameter.ai/labs/we-found-a-gap-at-openai) ⭐️ 7.0/10

OpenAI reportedly fixed a ChatGPT vulnerability on October 26 that Parameter researchers said could be triggered when a signed-in user opened a malicious shared-chat link. The flaw involved message handling between the preview feature and a chart component, reportedly allowing attackers to execute code within the user&\#x27;s ChatGPT session, read private conversations and send them to an external server without any app installation. The report says OpenAI classified the issue as P1 and paid the researchers a $5,000 bounty. The brief account does not provide enough detail to establish the source headline&\#x27;s broader claim of full account takeover.

telegram · zaihuapd · Nov 2, 10:24

**「Sharing and session boundaries」** ChatGPT’s standard sharing feature lets users publish a conversation and send others a link to view it. The relevant security boundary is between displaying that shared content and executing code as chatgpt.com with access to the viewer’s authenticated web session, as Parameter describes.

<details><summary>References</summary>
<ul>
<li><a href="https://www.parameter.ai/labs/we-found-a-gap-at-openai">Do the Math: How We Took Over ChatGPT Accounts - Parameter</a></li>

</ul>
</details>

**Tags**: `#ChatGPT`, `#漏洞研究`, `#会话安全`, `#数据泄露`

---

<a id="item-tech-news-5"></a>
### [WIRED reports hidden sexual deepfake features across 400-plus AI apps and sites](https://www.wired.com/story/hundreds-of-mundane-ai-apps-are-hiding-abusive-deepfake-features/) ⭐️ 7.0/10

According to the supplied recap of a WIRED investigation, a network of more than 400 linked AI apps and websites allegedly concealed sexually explicit deepfake features behind ordinary pet-portrait and language-learning tools. The hidden interfaces loaded under certain conditions and let users generate explicit images or videos from other people&\#x27;s photos; researchers traced connections through code, domains, and advertising. In September, 27 of the apps were still listed on Google Play with more than 350,000 combined downloads, and many were rated suitable for all ages. Apple said developers had replaced remotely hosted web content after their apps passed review.

telegram · zaihuapd · Nov 2, 12:45

**「Remote content and app review」** Apps can display remotely hosted web pages, allowing their visible content to change without replacing the installed app—a potential gap between what store reviewers inspect and what users later see. According to the supplied account, Apple said developers exploited this gap by replacing remote web content after approval.

**「App removals and advertising restrictions」** Apple removed 19 apps after receiving WIRED&\#x27;s findings, while Google had already removed most of the relevant apps before WIRED contacted it. Meta said it had blocked 209 related apps from advertising—a restriction on their promotion, not evidence that the apps or websites themselves were taken offline.

**Tags**: `#AI安全`, `#色情深度伪造`, `#应用商店审核`, `#平台治理`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Reassessing Claims of Superhuman Neural Network Weight Editing](https://seangoedecke.com/llms-are-not-superhuman-at-reading-and-writing-neural-network-weights/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 3, 00:00

**「Background」** A paper presents GPT-6 Astra’s ability to identify and edit neural networks directly through their weights as beyond normal human capability. Sean Goedecke scrutinizes that interpretation because genuinely superhuman model improvement could enable recursive self-improvement.

**「Solution」** For the roughly 17,000-weight game networks, plotting the magnitude of each labeled grid input’s first-layer weights produces heatmaps with recognizable spatial patterns, such as Pac-Man’s maze. Goedecke calls Astra’s unaided calculation of these magnitudes impressive mental arithmetic, not superhuman research. The 0.8B-parameter Qwen model’s mathematics failure was similarly specific: it solved all tested problems requiring fewer than 32,000 tokens, but longer reasoning became trapped in loops. With Python available, Astra used what Goedecke describes as a familiar steering approach: it generated four pairs of looping and non-looping texts, compared their internal activations, and tested reductions to weights implicated in looping until a patch stopped the repetition, enabling longer mathematical reasoning.

**「Takeaway」** Goedecke argues that a competent human researcher could reproduce these methods, making the results evidence of capable engineering rather than a radically new research capability. He likens direct weight edits to patching compiled binaries and expects AI’s larger contribution to model development to come through improving conventional training.

**Tags**: `#LLM capabilities`, `#Neural network interpretability`, `#Weight editing`, `#Activation steering`

---

<a id="item-tech-blog-2"></a>
### [Audience Capture and Proxy Metrics](https://seangoedecke.com/audience-capture/) ⭐️ 5.0/10

rss · Sean Goedecke · Nov 3, 00:00

**「Background」** Sean Goedecke worries that his engineering instinct to make numbers rise can undermine his reasons for writing online, where analytics, rankings, and financial incentives reward engagement. He actually wants thoughtful readers, feedback grounded in experience, and a reputation for careful thinking—not simply clicks.

**「Solution」** He illustrates the danger with a hypothetical loop: popular anti-microservices posts encourage more of the same, while careful readers quietly leave and rising traffic conceals their replacement by people who barely read. He reports little attention for some technical explainers and philosophical pieces he enjoys, while attributing some industry laments’ popularity to their role as outlets for readers’ anxieties. Because reach helps him find thoughtful readers but says little about whether he satisfies them, he relies on his taste and the sparse signal of substantive replies. He extends the distinction to engineering: clearing Jira tickets can displace work that earns promotion, while promotion itself may be either a genuine goal or a means to doing technical work one values.

**「Takeaway」** Goedecke argues for conscious tradeoffs, not rejection of measurable success: compromising one aim to secure something genuinely valued can be worthwhile. The failure is letting an easily optimized proxy replace the real goal by habit, without gaining anything one actually wants.

**Tags**: `#audience capture`, `#proxy metrics`, `#incentive design`, `#engineering culture`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Oracle plans AI financing; Marvell agrees to buy Lumentum](https://www.cnbc.com/2026/11/02/stocks-making-the-biggest-moves-midday-orcl-spcx-tem-rivn.html) ⭐️ 7.0/10

Oracle plans to sell $10 billion in shares and issue $10 billion in debt to fund its artificial intelligence expansion, according to regulatory filings cited by CNBC. Separately, Marvell agreed to buy laser maker Lumentum in a deal valued at $115 billion and paid entirely in shares, with completion expected in the first half of 2028.

rss · CNBC Finance · Nov 2, 20:00

**「Background」** Marvell and Lumentum said the offer valued Lumentum shares about 23.9% above their market price before deal speculation, based on both companies’ October 28, 2026 closing prices.

<details><summary>References</summary>
<ul>
<li><a href="https://investor.marvell.com/news-events/press-releases/detail/1040/marvell-and-lumentum-to-combine-creating-a-category-leader-in-ai-connectivity">Marvell and Lumentum to Combine, Creating a Category Leader ...</a></li>

</ul>
</details>

**Tags**: `#Corporate financing`, `#Mergers and acquisitions`, `#Corporate earnings`, `#AI infrastructure`, `#Equity markets`

---

<a id="item-finance-news-2"></a>
### [Marvell agrees to $115 billion Lumentum deal](https://www.cnbc.com/2026/11/02/stocks-making-the-biggest-moves-premarket-crwd-rivn-mu.html) ⭐️ 7.0/10

Marvell Technology agreed to acquire Lumentum in a deal paid entirely in shares that values Lumentum at $115 billion, CNBC reported. Separately, Estée Lauder reported fiscal first-quarter earnings excluding certain items of $0.72 per share, above the $0.51 expected by analysts polled by FactSet, and raised its full-year earnings outlook.

rss · CNBC Finance · Nov 2, 12:49

**「Background」** Marvell’s planned acquisition is a bet that optical networking—technology that moves data using light—will be central to expanding artificial-intelligence data centers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/02/technology/marvell-lumentum-115-billion-merger-ai.html">Driven by A.I. Boom, Marvell and Lumentum Announce $ 115 Billion ...</a></li>

</ul>
</details>

**Tags**: `#Mergers and acquisitions`, `#Corporate earnings`, `#Premarket trading`, `#Analyst upgrades`, `#Memory stocks`

---

<a id="item-finance-news-3"></a>
### [Anthropic IPO filing reportedly shows wider losses](https://www.cnbc.com/2026/11/02/anthropic-ant-s-1-quarter-financials.html) ⭐️ 7.0/10

A Telegram post citing CNBC says Anthropic updated its filing to go public, reporting a $104 billion net loss for the first nine months of 2026, versus $25.1 billion a year earlier. The post says Anthropic attributed its first-half loss mainly to changes in the recorded value of debt and other financial obligations, rather than money spent running the business.

telegram · zaihuapd · Nov 2, 15:12

**「Background」** Anthropic’s initial filing for a stock-market listing, released last week, covered only the first half of 2026. The company said its first-half loss mainly reflected changes in the recorded value of debt and other financial contracts, so it was not a direct measure of cash spent running the business.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/02/anthropic-ant-s-1-quarter-financials.html">Anthropic releases amended IPO prospectus with Q3 financials</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#IPO`, `#企业财报`, `#AI基础设施`, `#公允价值变动`

---

<a id="item-finance-news-4"></a>
### [UK proposes longer wait for permanent residency](https://www.gov.uk/government/news/home-secretary-unveils-new-rules-for-migrants-settling-in-the-uk) ⭐️ 7.0/10

The UK government has proposed extending the standard residence requirement for most migrants applying for permanent residency from five to 10 years. The plan includes shorter routes for some high earners and public-service workers.

telegram · zaihuapd · Nov 2, 23:50

**「Background」** The Home Office’s proposed “earned settlement” system would link permanent residence to applicants’ contributions and conduct, with requirements covering English skills, unpaid taxes and criminal records.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gov.uk/government/news/home-secretary-unveils-new-rules-for-migrants-settling-in-the-uk">Home Secretary unveils new rules for migrants settling in the UK - GOV.UK</a></li>

</ul>
</details>

**Tags**: `#英国移民政策`, `#永久居留`, `#劳动力市场`, `#公共服务`

---