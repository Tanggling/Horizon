---
layout: default
title: "Horizon Summary: 2026-10-23 (EN)"
date: 2026-10-23
lang: en
---

> From 44 items, 12 important content pieces were selected

---

**Technology News**
1. [Quad9 Plans French Exit; CTO Says GeoIP Blocking Is Likely](#item-tech-news-1) ⭐️ 8.0/10
2. [Reported Switch 2 jailbreak highlights AI-assisted console testing](#item-tech-news-2) ⭐️ 8.0/10
3. [Smart TV Study Reports Content Traffic After ACR Is Disabled](#item-tech-news-3) ⭐️ 8.0/10
4. [333 Tor Exit Relays Reportedly Taken Offline After Ebury Backdoor Discovery](#item-tech-news-4) ⭐️ 8.0/10
5. [eMudhra announces exit from global SSL/TLS certificate business](#item-tech-news-5) ⭐️ 7.0/10
6. [Earstrip claims 3.7 million map polygon triangulations in 489 ms](#item-tech-news-6) ⭐️ 7.0/10
7. [Carbon-X offers open 14.8B-parameter modeling of DNA and text](#item-tech-news-7) ⭐️ 7.0/10
8. [miHoYo and Tsinghua Release GameScaling Game-Control Models](#item-tech-news-8) ⭐️ 7.0/10
9. [Oracle Java SE JSSE Security Alert Reports Patches for Critical Vulnerability](#item-tech-news-9) ⭐️ 7.0/10

**Technology Blog**
1. [Performance Gains Come From Redesign, Not Just Faster Languages](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [China’s CSI 300 reportedly falls 20% from June peak](#item-finance-news-1) ⭐️ 7.0/10
2. [Australian court orders Apple to allow alternative iPhone app stores](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Quad9 Plans French Exit; CTO Says GeoIP Blocking Is Likely](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

Quad9 has announced plans to exit France, according to the supplied headline, with discussion linking the withdrawal to DNS-blocking obligations. A commenter identifying himself as Quad9’s CTO says the resolver will probably use GeoIP filters to block French users after November 24. This is a prospective measure, not a confirmed shutdown; the full announcement is unavailable in the supplied material, leaving the precise scope and implementation uncertain.

hackernews · farrokhi · Oct 22, 14:32 · [Discussion](https://news.ycombinator.com/item?id=50195959)

**「DNS and geographic blocking」** A DNS resolver translates domain names into the IP addresses devices need to reach internet services; blocking resolution can therefore restrict access without removing the underlying content. In the supplied discussion, a commenter identifying himself as Quad9’s CTO acknowledges the tension between potentially blocking French users with GeoIP filters and Quad9’s position that such filters are insufficient for selectively denying resolution of particular domain names.

**「Potential service loss」** Users in France who rely on Quad9 may need to switch DNS resolvers if the proposed access block takes effect, since it would deny access to the service rather than merely prevent resolution of selected domain names.

**「Geographic enforcement dispute」** The self-identified CTO acknowledges tension between potentially using GeoIP to exclude French users and Quad9’s position that geographic filtering is insufficient for selectively blocking domain resolution. Another commenter cites an account of a contempt fine after a plaintiff bypassed GeoIP restrictions with a VPN, questioning whether such enforcement demands are practically achievable; that legal account is not independently verified in the supplied material.

**Tags**: `#DNS`, `#Internet Infrastructure`, `#Internet Regulation`, `#Geoblocking`

---

<a id="item-tech-news-2"></a>
### [Reported Switch 2 jailbreak highlights AI-assisted console testing](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 8.0/10

A linked blog post reports a Nintendo Switch 2 jailbreak, but the article itself is unavailable in the supplied material, leaving the exploit mechanism, supported firmware, access level, and reproducibility unverified. A supplied comment quotes a testing setup in which JetKVM devices let Codex send controller inputs over USB and receive console video over HDMI, while a mechanical actuator presses the power button to restart crashed consoles. These details describe an AI-assisted hardware-testing workflow, not proof of the jailbreak’s scope or availability.

hackernews · ledoge · Oct 22, 08:01 · [Discussion](https://news.ycombinator.com/item?id=50192536)

**「What access the jailbreak claims」** A console jailbreak bypasses restrictions on running unauthorized code, but its scope depends on the privileges obtained. The author&\#x27;s description calls ns2jb a software-only, tethered jailbreak and claims native-code execution as ordinary system modules and the built-in fs module; that description alone does not establish that Switch 2 games can run on other hardware.

**「Automation draws attention」** Commenters highlighted the combination of KVM access and physical power-button automation, while one argued that the tooling’s usefulness should be distinguished from AI’s contribution relative to an experienced security researcher. Another speculated about game dumps and portability, but explicitly conditioned that prediction on decrypted filesystem read/write access, which the supplied material does not establish.

<details><summary>References</summary>
<ul>
<li><a href="https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/">pepsipu.com</a></li>

</ul>
</details>

**Tags**: `#reverse engineering`, `#console security`, `#jailbreaking`, `#AI-assisted research`

---

<a id="item-tech-news-3"></a>
### [Smart TV Study Reports Content Traffic After ACR Is Disabled](https://watchingthewatchers.github.io/watchingthewatchers/index.html) ⭐️ 8.0/10

A study of 12 smart TVs from 10 manufacturers in the United States reports that some tested models continued sending content-related traffic after users disabled automatic content recognition \(ACR\), based on 5,943 controlled experiments. The researchers report that VIDAA OS sent non-resettable device IDs and audio fingerprints over unencrypted MQTT, while Vizio’s WatchFree+ exposed program names in unencrypted domain-name queries that users could not disable. The supplied account does not identify affected models or firmware versions or provide full methods, limiting assessment of the findings’ scope and independent verification.

telegram · zaihuapd · Oct 22, 09:50

**「How viewing recognition differs from transport security」** Automatic content recognition \(ACR\) identifies what a television is playing using signals such as audio fingerprints. An ACR opt-out and encrypted network transmission address different privacy concerns: the former controls recognition activity, while the latter protects transmitted data from being read in transit.

**「Privacy implications」** For users of the affected tested TVs, disabling ACR was not sufficient to stop all content-related reporting. The reported plaintext transmissions also leave device identifiers, audio fingerprints, or program names exposed to parties able to observe that network traffic.

**Tags**: `#智能电视`, `#自动内容识别`, `#隐私安全`, `#物联网安全`, `#网络流量分析`

---

<a id="item-tech-news-4"></a>
### [333 Tor Exit Relays Reportedly Taken Offline After Ebury Backdoor Discovery](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

A Tor operator reportedly scanned roughly 3,000 exit relays and identified 333—about 10%—infected with the Ebury backdoor; the account says they were marked BadExit on October 4 and all went offline the following day. The compromised relays could reportedly redirect SSH connections on port 22 to 12 interception servers to steal credentials. According to the account, attackers had compromised the servers in August and blocked some ports to focus on collecting unencrypted email traffic. The intrusion method remains undetermined, and the supplied report provides neither detection details nor primary evidence to independently verify the findings.

telegram · zaihuapd · Oct 22, 14:52

**「How exit relays became interception points」** Exit relays are the points where Tor traffic leaves the network for its destination, making compromised relays a potential interception point for outbound connections. The operator’s account says the infected relays began a coordinated campaign on October 2 to intercept SSH connections and collect unencrypted data; this describes abuse of relay servers, not a demonstrated break of Tor’s encryption.

<details><summary>References</summary>
<ul>
<li><a href="https://kaba.cx/posts/20261020_Tor/">How I got over 300 Tor exit nodes removed - KABA</a></li>

</ul>
</details>

**Tags**: `#Tor`, `#Ebury 后门`, `#SSH 劫持`, `#凭据窃取`, `#网络安全`

---

<a id="item-tech-news-5"></a>
### [eMudhra announces exit from global SSL/TLS certificate business](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 7.0/10

eMudhra has announced plans to exit the global SSL/TLS certificate business, affecting its role as a provider of certificates used to authenticate websites and secure connections. The supplied material does not establish an exit timetable, customer migration arrangements, or whether existing certificates will remain valid. The announcement comes amid community scrutiny of a certificate-authority security incident, but the underlying technical details and scope of exposure are not established by the available evidence.

hackernews · bo0tzz · Oct 22, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50195110)

**「Certificate-key compromise」** Intermediate certificate authorities use private keys to sign certificates; compromising those keys can allow attackers to issue certificates without authorization. Mozilla reported receiving notice on October 17 that private keys associated with eight eMudhra intermediate certificates had been compromised, providing concrete security context for the company’s announced withdrawal.

**「Questions about key security and accountability」** Hacker News commenters criticized what they viewed as inadequate accountability for the incident, with one linking to public questions attributed to the Chrome team. Another challenged a quoted assurance that the affected certificate authorities had issued no end-entity certificates, arguing that unauthorized issuance—not just the provider’s own issuance history—was the relevant concern; the supplied comments do not establish whether such issuance occurred.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.mozilla.org/security/2026/10/20/protecting-firefox-users-following-the-compromise-of-emudhra-intermediate-certificates/">Protecting Firefox users following the compromise of eMudhra ...</a></li>

</ul>
</details>

**Tags**: `#TLS`, `#public-key-infrastructure`, `#certificate-authorities`, `#security`

---

<a id="item-tech-news-6"></a>
### [Earstrip claims 3.7 million map polygon triangulations in 489 ms](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 7.0/10

A performance writeup presents Earstrip as a faster alternative to Earcut for polygon triangulation, claiming it processed 3.7 million map polygons in 489 ms. The supplied material does not include the article’s implementation details or benchmark methodology, so the reported timing and its applicability to other workloads remain unverified.

hackernews · molind · Oct 22, 09:31 · [Discussion](https://news.ycombinator.com/item?id=50193170)

**「Triangulation and runtime tradeoffs」** Polygon triangulation divides polygonal shapes into triangles; Earcut’s approach searches for removable triangle-shaped “ears.” The post’s comparison is runtime-dependent: it reports that native earcut.hpp is 14% slower than Earstrip, while compiling to WebAssembly and running in V8 imposes a larger performance penalty on earcut.hpp than on Earstrip.

**「Speed versus deployment cost」** A commenter identifying as Earcut’s author expressed interest in borrowing optimizations for its JavaScript version, but said some optimizations had deliberately been rejected to preserve its 4.1 kB minified-and-gzipped size; they asked how large Earstrip’s WebAssembly build is. Other commenters raised alternative triangulation algorithms, while the self-identified author of Delaunay32 noted that they had not benchmarked the shared corpus and that their polygon API requires simple rings with non-touching holes.

<details><summary>References</summary>
<ul>
<li><a href="https://globus.software/blog/2026/10/16/cutting-map-polygons/">Faster than earcut : triangulating 3.7M map polygons in 489 ms</a></li>

</ul>
</details>

**Tags**: `#computational-geometry`, `#polygon-triangulation`, `#performance-optimization`, `#geospatial`

---

<a id="item-tech-news-7"></a>
### [Carbon-X offers open 14.8B-parameter modeling of DNA and text](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 7.0/10

The post presents Carbon-X as an open 14.8B-parameter decoder-only model that accepts raw DNA in chat and answers in English, with Apache 2.0 weights reportedly fitting on one 80 GB GPU in bfloat16. It combines DNA and text in one token stream, uses 6-mer DNA tokens, and underwent mid-training on 302B tokens. The post cites Hugging Face reporting a 66.7% average across five DNA benchmarks with thinking disabled, versus 67.5% for GPT-6.1 Sol; this comparison is not independently verified in the supplied material. Carbon-X has not been clinically validated, and whether its benchmark results generalize to private variant datasets remains unresolved.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 22, 12:32

**「Connecting DNA sequences with language」** Carbon-X represents DNA using 6-mer tokens—chunks of six DNA bases—in the same token stream as natural-language text. This joint representation lets users supply raw sequences in a chat and receive English-language answers; the model card describes tasks such as classifying mutations and identifying regions that control gene activity.

**「Local use with limits」** For researchers with a suitable 80 GB GPU, the reported hardware requirement offers a path to analyzing sensitive DNA datasets locally rather than sending sequences to a hosted model. Workflows should still delegate exact sequence operations to code, as the model card advises.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/HuggingFaceBio/Carbon-X/blob/main/README.md">README.md · HuggingFaceBio/Carbon-X at main</a></li>

</ul>
</details>

**Tags**: `#DNA language models`, `#Genomics`, `#Open-weight models`, `#Local inference`

---

<a id="item-tech-news-8"></a>
### [miHoYo and Tsinghua Release GameScaling Game-Control Models](https://arxiv.org/abs/2610.28698v1) ⭐️ 7.0/10

miHoYo’s Honkai AI team, Tsinghua University, and collaborators have released GameScaling, with eight checkpoints and an inference client available under Apache-2.0, according to the supplied report. Built through continued pretraining of Qwen3.5 vision-language models for keyboard-and-mouse control, the models range from 0.8 billion to 27 billion parameters and output actions for the next 200 milliseconds at each step. Across 120 training configurations, the study reports that more data improves performance in the source domain, while greater data diversity helps transfer to similar games but offers limited gains in substantially different game worlds. The supplied account includes no benchmark scores or comparison results, so it does not establish the magnitude of any performance advantage.

telegram · zaihuapd · Oct 22, 11:32

**「From visual input to game control」** GameScaling adapts Qwen3.5 vision-language models through continued pretraining on keyboard-and-mouse gameplay. According to the project repository, each inference call uses the current game frame and a short history of frames and actions to produce the next 200 milliseconds of controls, making recent interaction history part of the model’s input.

**「Usable for inference, incomplete for reproduction」** Developers can experiment with the released checkpoints using the inference client, but the release excludes training code, limiting their ability to reproduce the reported training experiments directly from the published artifacts.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/THUSI-Lab/GameScaling">GitHub - THUSI-Lab/GameScaling: Scaling in Games: Continued ...</a></li>

</ul>
</details>

**Tags**: `#游戏智能体`, `#视觉语言模型`, `#模型扩展规律`, `#迁移学习`, `#开源模型`

---

<a id="item-tech-news-9"></a>
### [Oracle Java SE JSSE Security Alert Reports Patches for Critical Vulnerability](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 7.0/10

A Telegram report linking to an Oracle security alert says Oracle has released patches for CVE-2026-91403, a Java SE JSSE vulnerability with a reported CVSS score of 9.1. It describes remote exploitation without authentication, potentially compromising data confidentiality and integrity, and lists Java SE 8u511, 11.0.33, 17.0.21, 21.0.13, 25.0.5, and 27.0.1, plus unspecified GraalVM versions, as affected. The supplied material does not include the Oracle advisory text, so the vulnerability identifier, score, affected versions, exploitation conditions, and patch availability remain independently unverified.

telegram · zaihuapd · Oct 22, 12:30

**「Certificate-trust context」** Oracle’s linked advisory describes a more specific issue than the Telegram summary: the Java updates address CVE-2026-91403 by distrusting a set of affected intermediate certificate-authority certificates associated with eMudhra. This makes certificate trust the key context for the alert, rather than an unspecified remotely exploitable JSSE flaw; Oracle directs users to the latest Java version or its recommended mitigations.

**「Verify exposure before updating」** Maintainers using the listed Java SE releases or GraalVM should check the linked Oracle advisory against their deployed runtimes and confirm the applicable patched release. The report recommends prompt upgrades, but it does not identify fixed-version numbers or the affected GraalVM releases.

<details><summary>References</summary>
<ul>
<li><a href="https://www.oracle.com/security-alerts/alert-cve-2026-91403.html">Oracle Security Alert Advisory - CVE-2026-91403</a></li>

</ul>
</details>

**Tags**: `#Java SE`, `#JSSE`, `#漏洞预警`, `#补丁管理`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Performance Gains Come From Redesign, Not Just Faster Languages](https://seangoedecke.com/software-is-slow-because-of-bad-design-not-slow-languages/) ⭐️ 6.0/10

rss · Sean Goedecke · Oct 23, 00:00

**「Background」** Sean Goedecke challenges the expectation that AI-driven rewrites into C, Rust, or assembly will make software dramatically faster: he argues that waiting for databases, networks, and disks often dominates execution time. Even CPU-heavy applications written in slower languages may already delegate their expensive operations to optimized native libraries, leaving little for a wholesale rewrite to accelerate.

**「Solution」** His illustrative database-backed website spends half its request time querying the database, so Amdahl’s law—the limit imposed by work an optimization leaves unchanged—caps a language-only speedup at 2×, even if the remaining execution becomes instantaneous. Design changes can instead reduce or reorganize the expensive work itself: cache external calls, move operations outside the request lifecycle, parallelize independent work, or replace repeated SQL queries with one query. For a CPU-bound example, Goedecke cites Bryan Cantrill’s account of a Rust rewrite that ran 30% faster than carefully optimized C, attributing the improvement to a more cache-efficient B-tree rather than intrinsic language speed. He therefore advocates profiling and redesign before rewriting, while retaining faster-language implementations for genuinely CPU-bound hotspots that cannot be refactored to do less work.

**「Takeaway」** Goedecke’s thesis is that AI’s larger performance opportunity lies in changing what software does, not merely translating how it expresses the same work. Language speed matters where it addresses the actual bottleneck, not as a substitute for understanding it.

**Tags**: `#software performance`, `#Amdahl’s law`, `#software design`, `#profiling`, `#programming languages`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China’s CSI 300 reportedly falls 20% from June peak](https://www.bloomberg.com/news/articles/2026-10-22/china-stocks-set-for-bear-market-as-ai-trade-policy-hopes-fade) ⭐️ 7.0/10

China’s CSI 300 stock index was down 20% from its June high at one point on October 22, according to a Telegram post citing Bloomberg. That decline puts it at the commonly used threshold for a bear market—a fall of 20% from a recent peak.

telegram · zaihuapd · Oct 22, 05:05

**「Background」** A fall of 20% from a recent peak is commonly called a bear market; for China’s benchmark CSI 300 index, the comparison is with its June high.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/10/22/chinas-stock-market-csi-300-bear-market.html">China&#x27;s stock market: CSI 300, bear market - CNBC</a></li>

</ul>
</details>

**Tags**: `#A股`, `#沪深300`, `#科技股`, `#企业业绩`, `#财政政策`

---

<a id="item-finance-news-2"></a>
### [Australian court orders Apple to allow alternative iPhone app stores](https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/) ⭐️ 7.0/10

According to the supplied account of a 9to5Mac report, Australia’s Federal Court ordered Apple to allow third-party app stores, app installation from websites, alternative payments and external payment links on Australian iPhones from March 1, 2027. The ruling stems from Epic Games’ competition lawsuit; Apple says it will appeal and seek to pause enforcement.

telegram · zaihuapd · Oct 22, 06:54

**「Background」** The ruling stems from Epic Games’ competition lawsuit, in which the court found that Apple’s substantial power over iPhone app distribution and payments allowed it to restrict competition in breach of Australian law.

**「What changes」** If implemented, the order would let developers reach Australian iPhone users and accept payments through channels outside Apple’s App Store and payment system.

**Tags**: `#苹果`, `#澳大利亚反垄断`, `#应用分发`, `#应用内支付`

---