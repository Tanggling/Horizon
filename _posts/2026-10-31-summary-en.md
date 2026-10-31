---
layout: default
title: "Horizon Summary: 2026-10-31 (EN)"
date: 2026-10-31
lang: en
---

> From 43 items, 11 important content pieces were selected

---

**Technology News**
1. [Tampered Claude Code extension on Cursor’s marketplace adds SSH backdoor](#item-tech-news-1) ⭐️ 8.0/10
2. [Report claims five Azure cross-tenant compromises](#item-tech-news-2) ⭐️ 8.0/10
3. [Northflank Breach Reported; Customer Impact Unconfirmed](#item-tech-news-3) ⭐️ 7.0/10
4. [Nesformer: NES emulation in roughly 1 GB of Qwen weights](#item-tech-news-4) ⭐️ 7.0/10
5. [Tangled stabilizes AT Protocol lexicons and adds organization support](#item-tech-news-5) ⭐️ 7.0/10
6. [Bunny removes Armenia CDN node and reissues platform TLS certificates](#item-tech-news-6) ⭐️ 7.0/10
7. [Soft-MTP Proposes a One-Line Gradient Change for Multi-Token Prediction](#item-tech-news-7) ⭐️ 7.0/10
8. [Baidu Netdisk iOS ads reportedly bypass motion-sensor restrictions using magnetometer](#item-tech-news-8) ⭐️ 7.0/10
9. [Apple Intelligence China beta reportedly planned for November 4](#item-tech-news-9) ⭐️ 7.0/10

**Financial News**
1. [Report identifies Anthropic as major SpaceX customer](#item-finance-news-1) ⭐️ 7.0/10
2. [DeepSeek’s second funding round reportedly totals 105.5 billion yuan](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Tampered Claude Code extension on Cursor’s marketplace adds SSH backdoor](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 8.0/10

A tampered copy of the Claude Code extension on Cursor’s marketplace reportedly appended an attacker’s SSH public key to users’ \`~/.ssh/authorized\_keys\`. A commenter quoting Cursor’s security notice identified the key’s label as \`svc-telemetry\`, which potentially affected users can look for in that file. The supplied excerpts do not identify affected extension versions or explain how the attacker obtained marketplace access.

hackernews · \_chall · Oct 30, 07:09 · [Discussion](https://news.ycombinator.com/item?id=50300683)

**「How SSH key persistence works」** SSH’s \`authorized\_keys\` file lists public keys allowed to authenticate to a user account. This explains the persistence mechanism in Cursor’s security notice: adding an attacker’s public key can permit later logins using the matching private key, provided an SSH service is reachable and configured to accept it.

**「Check for persistent SSH access」** Potentially affected Cursor users should inspect their SSH authorized-keys file for an entry labeled \`svc-telemetry\` and treat any match as a compromise indicator. Because the reported backdoor establishes persistence outside the extension, updating or uninstalling the extension alone should not be assumed to remove the attacker’s access.

**「Community discussion」** A commenter identifying himself as Anthropic’s Felix Rieseberg said Anthropic neither built nor published the tampered copy, its systems and employee laptops were not compromised, and official-channel releases were unaffected. He said the incident affected only Cursor users and that Anthropic was working with Cursor.

<details><summary>References</summary>
<ul>
<li><a href="https://cursor.com/blog/claude-code-extension-security-notice">Security notice — malicious version of Anthropic. claude - code ...</a></li>
<li><a href="https://phorion.io/blog/offical-claude-code-vsx-compromise/">Official Claude Code Extension Compromise: Security Advisory</a></li>
<li><a href="https://opensourcemalware.com/blog/trojanized-claude-code-extension-plants-persistent-ssh-backdoor">Trojanized Claude Code Extension Plants an SSH Backdoor</a></li>

</ul>
</details>

**Tags**: `#supply-chain-security`, `#ide-extensions`, `#cursor`, `#claude-code`, `#ssh`

---

<a id="item-tech-news-2"></a>
### [Report claims five Azure cross-tenant compromises](https://www.binarysecurity.no/posts/2026/10/one-root-case) ⭐️ 8.0/10

A security research post linked on Hacker News claims five “full” cross-tenant compromises in Microsoft Azure, alleging failures of isolation between customer environments. The technical write-up is absent from the supplied material, leaving the affected services, attack prerequisites, extent of access gained, and remediation status unverified.

hackernews · swq115 · Oct 30, 10:06 · [Discussion](https://news.ycombinator.com/item?id=50301854)

**「Tenant isolation」** Tenant isolation is the security boundary meant to prevent one cloud customer from accessing another customer&\#x27;s data or resources without authorization. A cross-tenant compromise breaches that boundary, but the headline alone does not establish which Azure services were affected or what access an attacker gained.

**「Community discussion」** One commenter raised an unverified concern about Microsoft’s admin-consent flow at login.microsoftonline.com, alleging that its callback can be forged if an attacker knows another customer’s tenant ID. They argued that documentation warnings against using that ID for authentication or authorization are insufficient without a way to authenticate users.

**Tags**: `#Azure`, `#cloud security`, `#vulnerability research`, `#tenant isolation`

---

<a id="item-tech-news-3"></a>
### [Northflank Breach Reported; Customer Impact Unconfirmed](https://status.northflank.com/) ⭐️ 7.0/10

A Hacker News submission reports a breach at hosted infrastructure provider Northflank and links to its status page. The supplied material includes neither status-page content nor a provider incident statement, so it does not verify the breach claim or establish the attack vector, affected customers, or whether customer data or credentials were exposed.

hackernews · js4ever · Oct 30, 15:10 · [Discussion](https://news.ycombinator.com/item?id=50305025)

**「What Northflank provides」** Northflank is a managed application platform that connects to Git repositories and runs application services, databases and background jobs, handling the deployment infrastructure for developers.

**「Protecting environment-variable secrets」** One commenter described encrypting environment-variable secrets and embedding the decryption key in application code, arguing that this adds protection if attackers cannot also access the code or binary. Their suggestion that attackers lacked such access in the reported Northflank incident is not established by the supplied material.

<details><summary>References</summary>
<ul>
<li><a href="https://northflank.com/features/platform">Platform — Features — Northflank</a></li>

</ul>
</details>

**Tags**: `#security`, `#cloud-infrastructure`, `#data-breaches`, `#secrets-management`

---

<a id="item-tech-news-4"></a>
### [Nesformer: NES emulation in roughly 1 GB of Qwen weights](https://github.com/dbreunig/nesformer) ⭐️ 7.0/10

Nesformer is presented as a working Nintendo Entertainment System \(NES\) emulator implemented in roughly 1 GB of Qwen model weights. It reportedly runs 150–290 times slower than the original console, far short of real-time emulation. The supplied excerpts do not establish game compatibility, emulation accuracy, or the test conditions behind that performance figure.

hackernews · dbreunig · Oct 30, 16:40 · [Discussion](https://news.ycombinator.com/item?id=50306442)

**「Emulation and model weights」** Conventional NES emulators reproduce the console’s hardware behavior in software, including processor operations and changes to memory. Qwen is Alibaba Cloud’s family of predominantly open-weights language models; model weights are the numerical parameters used in a neural network’s calculations.

**「Memory implementation and efficiency」** Commenter cafebeen said the project models RAM inside the network using a gated DeltaNet architecture, rather than simulating only the CPU. Commenters jacquesm and pbohun praised the experiment but argued that its computational cost highlights the efficiency advantage of conventional deterministic programs.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#NES emulation`, `#Qwen`, `#Neural computation`, `#Computer architecture`

---

<a id="item-tech-news-5"></a>
### [Tangled stabilizes AT Protocol lexicons and adds organization support](https://tangled.org/blog/forge/) ⭐️ 7.0/10

Tangled’s co-founder says the federated code forge has stabilized its AT Protocol lexicons, overhauled its architecture and UI, and shipped support for organizations. The co-founder also claims easier self-hosting of the entire stack or selected components, but the supplied material contains no deployment details to assess that claim. Private repositories were announced for rollout in the following couple of weeks, not as available at launch.

hackernews · zlliang · Oct 30, 15:44 · [Discussion](https://news.ycombinator.com/item?id=50305573)

**「Federation beyond Git」** A code forge adds collaboration features, such as issues and pull requests, to Git repository hosting. Tangled’s AT Protocol lexicons are schemas defining its data records, giving other implementations a common format for interpreting collaboration data rather than merely exchanging Git repositories.

**「Interoperability and migration questions」** A developer building juju.bi asked whether issue, pull-request and comment records now fall under repository rather than user scope, a change they have been awaiting while planning Tangled interoperability; the supplied comments do not resolve the question. Another commenter considering a move from self-hosted Gitea said they need a git-bug bridge to keep issues synchronized.

**Tags**: `#Code Hosting`, `#AT Protocol`, `#Federation`, `#Self-Hosting`, `#Developer Tools`

---

<a id="item-tech-news-6"></a>
### [Bunny removes Armenia CDN node and reissues platform TLS certificates](https://status.bunny.net/incidents/p6gf1by9kr7m) ⭐️ 7.0/10

According to its incident notice quoted in the supplied comments, Bunny stopped routing traffic through a CDN node in Armenia within 20 minutes of receiving a provider alert about unauthorized access involving third-party server-management software. Bunny says it preserved relevant security logs, wiped the server, revoked its access to other systems, and permanently removed it from its infrastructure. Investigations found no indication of unauthorized access to Bunny’s server but could not rule it out; if access occurred, potentially exposed information would include temporarily cached CDN content, Pull Zone configurations, and TLS certificates stored there. As a precaution, Bunny revoked and reissued all TLS certificates for its b-cdn.net and bunny.run platform domains.

hackernews · SondreDag · Oct 30, 19:05 · [Discussion](https://news.ycombinator.com/item?id=50308697)

**「CDN nodes and TLS」** A CDN node serves cached content to users and can also hold the TLS certificates used for HTTPS delivery. HTTPS uses TLS to encrypt traffic between clients and servers, while trusted server certificates allow clients to verify the server’s identity.

**「Incident scope and forensic preservation」** One commenter argued that the incident should be framed as a provider compromise rather than a confirmed breach of Bunny. Others praised the fast containment or stressed the need to preserve forensic evidence before wiping a potentially compromised server.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/HTTPS">HTTPS - Wikipedia</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Glossary/HTTPS">HTTPS - Glossary | MDN - MDN Web Docs</a></li>

</ul>
</details>

**Tags**: `#security`, `#cdn`, `#tls`, `#incident-response`, `#third-party-risk`

---

<a id="item-tech-news-7"></a>
### [Soft-MTP Proposes a One-Line Gradient Change for Multi-Token Prediction](https://www.reddit.com/r/MachineLearning/comments/1xjnz40/multitoken_prediction_done_right_r/) ⭐️ 7.0/10

The authors of Soft Multi-Token Prediction \(Soft-MTP\) propose a language-model training change intended to improve speculative decoding while reducing interference with next-token prediction. They say standard multi-token prediction gradients mix a useful Kullback–Leibler \(KL\) self-distillation signal with a harmful noisy residual, and propose recovering the KL gradient with the one-line update \`h\_ntp += h\_mtp.detach\(\) - h\_mtp\`. The author-written post links a paper, GitHub code and a Hugging Face collection, but includes no benchmarks or ablations to substantiate its claims of improvements across tasks.

reddit · r/MachineLearning · /u/jayden\_teoh\_ · Oct 30, 18:53

**「How multi-token prediction supports decoding」** Next-token prediction trains a language model to predict the immediately following token, while multi-token prediction adds objectives for tokens further ahead. Those extra predictions can supply drafts for speculative decoding, in which the main model checks proposed tokens before accepting them. KL self-distillation encourages agreement between the draft predictions and the model’s own next-token probability distribution.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/papers/2610.38331">Paper page - Multi - Token Prediction Done Right</a></li>

</ul>
</details>

**Tags**: `#llm-training`, `#multi-token-prediction`, `#speculative-decoding`, `#self-distillation`

---

<a id="item-tech-news-8"></a>
### [Baidu Netdisk iOS ads reportedly bypass motion-sensor restrictions using magnetometer](https://www.landian.news/archives/127843.html) ⭐️ 7.0/10

A developer’s AI-assisted analysis of Baidu Netdisk 13.36.0 for iOS, released October 22, reportedly found a NoShake advertising-framework variant that can trigger shake-to-open ad redirects even when gyroscope and accelerometer access is disabled. According to the report, it uses Core Location’s CLHeading magnetometer readings rather than CoreMotion to detect phone movement. The report also describes an automatic ad click after roughly one second under certain parameters. The supplied secondary summary includes neither code nor full reproduction conditions, limiting independent verification and leaving the scope of the behavior unclear.

telegram · zaihuapd · Oct 30, 15:00

**「Compass heading versus motion sensing」** A magnetometer supplies compass-direction data, which can indicate changes in a phone’s orientation without an app directly reading its accelerometer or gyroscope. In the reported technique, that data is accessed through Core Location’s CLHeading interface rather than CoreMotion—a distinction that matters when assessing which sensor access a blocking measure actually covers.

**「Motion-only blocking may miss ad triggers」** The reported analysis suggests that blocking accelerometer and gyroscope access alone may not protect Baidu Netdisk iOS 13.36.0 users from unwanted ad redirects. Auditors should also test the Core Location/CLHeading trigger path rather than checking only CoreMotion; the supplied account lacks full reproduction conditions and does not establish whether other versions are affected.

**Tags**: `#iOS`, `#逆向工程`, `#磁力计`, `#移动广告`, `#权限控制`

---

<a id="item-tech-news-9"></a>
### [Apple Intelligence China beta reportedly planned for November 4](https://www.apple.com.cn/newsroom/2026/10/apple-intelligence-features-are-coming-to-users-in-china/) ⭐️ 7.0/10

A Telegram post linking to Apple Newsroom reports that Apple plans to open Apple Intelligence testing in China on November 4 through the latest iOS developer beta, followed by a public release with iOS 27.3 in December. The initial features would include Live Translation, Clean Up in Photos, and Writing Tools. The post also describes an Alibaba partnership to integrate Qwen into Siri, Writing Tools, and Visual Intelligence, but says next-generation Siri is excluded from this release. Support for other platforms would follow after the necessary approvals are obtained.

telegram · zaihuapd · Oct 30, 21:44

**「Apple Intelligence and Siri」** Apple Intelligence is an umbrella for AI features across Apple&\#x27;s software, rather than simply a new version of Siri. The supplied account distinguishes the reported Alibaba Qwen integration into Siri from the next-generation Siri upgrade, which it says is excluded from this rollout.

**「Qwen eligibility」** According to the post, Qwen access would be available to users with Apple Intelligence-compatible iPhones purchased in China, or users whose device location and Apple Account country/region are both set to China.

**Tags**: `#Apple Intelligence`, `#iOS`, `#千问`, `#生成式 AI`, `#中国市场`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Report identifies Anthropic as major SpaceX customer](https://www.cls.cn/detail/2519914) ⭐️ 7.0/10

Unnamed sources cited in the report identified Anthropic as the computing-services customer that SpaceX said accounted for about 34.5% of its total revenue last quarter.

telegram · zaihuapd · Oct 30, 06:20

**「Background」** Anthropic, which develops the Claude AI models, signed an agreement earlier in 2026 to use computing capacity at SpaceX’s Memphis, Tennessee, data center, according to the report.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#SpaceX`, `#AI算力采购`, `#营收集中度`

---

<a id="item-finance-news-2"></a>
### [DeepSeek’s second funding round reportedly totals 105.5 billion yuan](https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players) ⭐️ 7.0/10

A Telegram post citing The Information says DeepSeek’s second funding round totals 105.5 billion yuan, compared with about 51 billion yuan raised in its first round in June 2026.

telegram · zaihuapd · Oct 30, 12:37

**「Background」** DeepSeek is a Chinese AI developer backed by investment firm High-Flyer; the Telegram post says state-linked investors supplied 2% of its first funding round, completed in June 2026.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#企业融资`, `#企业估值`, `#国资投资`

---