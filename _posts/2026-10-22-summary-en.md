---
layout: default
title: "Horizon Summary: 2026-10-22 (EN)"
date: 2026-10-22
lang: en
---

> From 42 items, 15 important content pieces were selected

---

**Technology News**
1. [Report Alleges LiteLLM 1.107.0 PyPI Compromise Installs Credential Stealer and Backdoor](#item-tech-news-1) ⭐️ 8.0/10
2. [DuckDB 2.0.0 “Cinnamon Teal” Announced as LTS](#item-tech-news-2) ⭐️ 8.0/10
3. [Report alleges eMudhra CA keys cracked in milliseconds](#item-tech-news-3) ⭐️ 8.0/10
4. [PHP RCE fixes arrive early after coordinated disclosure breaks down](#item-tech-news-4) ⭐️ 8.0/10
5. [Node.js security updates reported for 26.x, 24.x and 22.x](#item-tech-news-5) ⭐️ 8.0/10
6. [Railway Publishes Security Disclosure; Comments Allege Stored Secret Misuse](#item-tech-news-6) ⭐️ 7.0/10
7. [GitLab Critical Patch Announcement Prompts Security Scrutiny](#item-tech-news-7) ⭐️ 7.0/10
8. [Meta reportedly ordered to pay $25 billion in New Mexico Cambridge Analytica case](#item-tech-news-8) ⭐️ 7.0/10
9. [OpenAI announces plans to bring its models to Google Cloud](#item-tech-news-9) ⭐️ 7.0/10
10. [Uber details AutoClean workflow for removing obsolete feature flags](#item-tech-news-10) ⭐️ 7.0/10
11. [Intel and AMD Plan Unified x86 PyTorch Optimizations Through oneDNN](#item-tech-news-11) ⭐️ 7.0/10
12. [Cloudflare Reports Automatic WAF Protection for php2shell](#item-tech-news-12) ⭐️ 7.0/10
13. [PHP Emergency Patch and Website Shutdowns Reported; Technical Details Unconfirmed](#item-tech-news-13) ⭐️ 7.0/10

**Financial News**
1. [Three Wall Street banks lead AI-driven equities revenue boom](#item-finance-news-1) ⭐️ 7.0/10
2. [Super Micro raises revenue outlook; Musk reports SpaceX–Tesla merger talks](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Report Alleges LiteLLM 1.107.0 PyPI Compromise Installs Credential Stealer and Backdoor](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) ⭐️ 8.0/10

A SafeDep report alleges that LiteLLM 1.107.0 distributed through PyPI was compromised to install a credential stealer and backdoor, potentially exposing users who installed that release. The supplied material identifies the package version but does not include the article body, technical indicators, verified scope, or remediation details. It therefore does not establish which installations were affected or identify a confirmed safe replacement version.

hackernews · abhisek · Oct 21, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50181114)

**「Package-level supply-chain risk」** A compromised package release can introduce malicious code through an otherwise routine dependency installation or upgrade. SafeDep’s report identifies LiteLLM 1.107.0 itself as carrying the malicious payload, while reporting that its pinned companion packages, litellm-proxy-extras 0.4.110 and litellm-enterprise 0.1.78, are clean—a distinction between the affected release and its dependencies.

**「Dependency trust and credentials」** One commenter argued that permission fatigue and routine acceptance of large dependency trees undermine developers’ security controls. Another recommended pinning LiteLLM to an earlier version while investigating alleged developer credential theft, but the supplied comments do not verify that account or establish that an earlier release is safe.

<details><summary>References</summary>
<ul>
<li><a href="https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/">Compromised LiteLLM 1 . 107 . 0 on PyPI Installs a Credential Stealer...</a></li>

</ul>
</details>

**Tags**: `#software-supply-chain`, `#PyPI`, `#LiteLLM`, `#credential-theft`, `#AI-infrastructure`

---

<a id="item-tech-news-2"></a>
### [DuckDB 2.0.0 “Cinnamon Teal” Announced as LTS](https://duckdb.org/2026/10/21/announcing-duckdb-200) ⭐️ 8.0/10

DuckDB 2.0.0 “Cinnamon Teal” has been announced as a long-term support \(LTS\) release of the analytical database. The announcement text is unavailable in the supplied material, so its support duration, availability, compatibility changes, and exact feature scope cannot be verified here. Comments describe improved high-core-count performance and discuss client-server access and triggers, but do not establish those as confirmed release capabilities.

hackernews · nnx · Oct 21, 14:01 · [Discussion](https://news.ycombinator.com/item?id=50181136)

**「Release context」** The official announcement identifies DuckDB 2.0.0 “Cinnamon Teal” as an LTS \(long-term support\) release. The available excerpt does not specify the support period or compatibility guarantees, so the LTS label alone does not establish those details.

**「Reported scaling gains and server use」** One commenter reports that their EC2 workloads now benefit from roughly 128–192 vCPUs, compared with scaling that previously topped out near 64 vCPUs, while noting little additional speedup beyond about 192 vCPUs; this is a workload-specific experience, not an independently verified benchmark. Another describes running an alpha as a centralized analytics server using a self-built extension for PostgreSQL wire-protocol or Arrow Flight connections, citing limited client support for DuckDB’s Quack protocol.

<details><summary>References</summary>
<ul>
<li><a href="https://duckdb.org/2026/10/21/announcing-duckdb-200">Announcing DuckDB 2 . 0 . 0 LTS “ Cinnamon Teal ” – DuckDB</a></li>

</ul>
</details>

**Tags**: `#DuckDB`, `#analytical databases`, `#parallel computing`, `#open source`

---

<a id="item-tech-news-3"></a>
### [Report alleges eMudhra CA keys cracked in milliseconds](https://scotthelme.co.uk/eight-bits-of-trust-emudhras-ca-keys-cracked-in-milliseconds/) ⭐️ 8.0/10

A report by Scott Helme alleges that eMudhra certificate-authority keys were cracked in milliseconds, raising concerns for systems that trust certificates issued through the affected CAs. The article body is unavailable in the supplied material, so the affected certificates, exploitability, timing claim, and remediation status cannot be verified. A Telegram account supplied alongside the discussion claims eight intermediate certificates were affected and browser vendors were taking blocking actions, but those details are not independently confirmed here.

hackernews · hkc · Oct 21, 09:08 · [Discussion](https://news.ycombinator.com/item?id=50177916)

**「Why CA private keys matter」** Certificate authorities use private keys to sign certificates that browsers and other software rely on to authenticate websites; recovering a CA’s private key can enable forged certificates within that authority’s permitted scope. The linked report says recovered eMudhra CA private keys included the integers 4, 56, and 115, illustrating a failure to generate unpredictable keys rather than a general defeat of modern cryptography.

**「Detection and update concerns」** One commenter quotes the original reporter as saying Google&\#x27;s paranoid\_crypto detected the weakness out of the box during a check of CCADB certificates, with a more thorough scan finding no additional hits. Another highlights the need to update software and container images that carry CA bundles, while emphasizing that devices without an accessible update path present a harder remediation problem; the supplied material does not establish which updates are already available.

<details><summary>References</summary>
<ul>
<li><a href="https://scotthelme.co.uk/eight-bits-of-trust-emudhras-ca-keys-cracked-in-milliseconds/">Eight Bits of Trust; eMudhra&#x27;s CA keys cracked in milliseconds</a></li>

</ul>
</details>

**Tags**: `#PKI`, `#Cryptographic Vulnerabilities`, `#Certificate Authorities`, `#IoT Security`

---

<a id="item-tech-news-4"></a>
### [PHP RCE fixes arrive early after coordinated disclosure breaks down](https://simonwillison.net/2026/Oct/21/php-security-release/) ⭐️ 8.0/10

PHP security updates released October 21 address two remote code execution vulnerabilities; the supplied release account lists PHP 8.5.12, 8.4.27, 8.3.36 and 8.2.35 as patched versions and urges operators to upgrade rather than rely solely on configuration mitigations. The vulnerabilities, CVE-2026-109618 and CVE-2026-109619, are reported to carry CVSS 4.0 scores of 9.2 and affect web-request deployments, with exploitation conditions varying by deployment. According to the PHP Foundation account quoted by Simon Willison, premature circulation of the CVE IDs prompted PHP to advance its release by one day, while a mistakenly published demonstration video subsequently accelerated public proof-of-concept development. That account supports the circulation of exploitation proofs of concept, but does not establish widespread successful attacks.

rss · Simon Willison · Oct 21, 18:41

**「Disclosure coordination」** Coordinated vulnerability disclosure gives maintainers time to prepare fixes before researchers publish details that could help attackers. According to the PHP Foundation account quoted in the report, premature circulation of the CVE IDs prompted PHP to advance its release from October 22 to October 21; the initial leak contained no technical details, but a subsequently published demonstration video helped accelerate development of exploitation proofs of concept.

**「Prioritize PHP runtime updates」** Operators of PHP-backed websites should prioritize deploying the patched PHP runtime, including through their distribution or hosting provider. AWS’s advisory says crafted web requests can allow unauthenticated attackers to execute code or read data accessible to affected PHP workers; the PHP Foundation’s account of circulating proof-of-concept exploits adds urgency, but does not establish widespread successful attacks.

**「Operator experience and disclosure concerns」** One commenter reported using an nginx rule blocking multipart uploads as a temporary mitigation while patching servers; this is an individual account, not evidence that the workaround covers all attack paths. Other commenters criticized the premature demonstration video and argued that disclosure agreements need consequences for breaches, though their interpretations of the firm&\#x27;s motives remain speculation.

<details><summary>References</summary>
<ul>
<li><a href="https://aws.amazon.com/security/security-bulletins/2026-143-aws/">PHP web runtimes (CVE-2026-109618 and CVE-2026-109619)</a></li>

</ul>
</details>

**Tags**: `#PHP`, `#Security Updates`, `#Remote Code Execution`, `#Vulnerability Disclosure`

---

<a id="item-tech-news-5"></a>
### [Node.js security updates reported for 26.x, 24.x and 22.x](https://nodejs.org/en/blog/vulnerability/october-2026-security-releases) ⭐️ 8.0/10

A Telegram report linking to a Node.js security advisory says updates for Node.js 26.x, 24.x and 22.x fix 10 vulnerabilities, with the highest severity rated high. It identifies a Brotli decoder out-of-bounds write \(CVE-2026-111497\) as potentially enabling remote code execution, alongside TLS noncanonical IP address handling flaws \(CVE-2026-106069 and CVE-2026-106072\), DNS null-byte validation \(CVE-2026-105482\), and a TLS IP normalization regression \(CVE-2026-105483\). The report also lists medium- and low-severity fixes involving HTTP proxies, cryptographic snapshots, zlib and permissions, but supplies neither exact patched versions nor exploitation conditions; the claims have not been independently verified here.

telegram · zaihuapd · Oct 21, 14:49

**「Security context」** The linked Node.js advisory classifies the Brotli decoder out-of-bounds write \(CVE-2026-111497\) as high severity, not critical, and states that it permits remote code execution. The supplied excerpt does not specify the conditions required to exploit it, so it does not establish that every application running an affected Node.js version is remotely exploitable.

**「Check patched versions before upgrading」** Maintainers running these Node.js branches should consult the linked official advisory to identify the patched release for their branch and assess exposure. The report says end-of-life versions are also affected, so users of unsupported branches should not assume they are outside the scope of these vulnerabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://nodejs.org/en/blog/vulnerability/october-2026-security-releases">Node . js — Wednesday, October 21, 2026 Security Releases</a></li>

</ul>
</details>

**Tags**: `#Node.js`, `#安全更新`, `#远程代码执行`, `#TLS`, `#Brotli`

---

<a id="item-tech-news-6"></a>
### [Railway Publishes Security Disclosure; Comments Allege Stored Secret Misuse](https://blog.railway.com/p/security-disclosure-wednesday-october-21st) ⭐️ 7.0/10

Railway has published a security disclosure, while community comments allege unauthorized use of secrets stored on its platform. The disclosure text is not included in the supplied material, so the incident’s technical cause, affected users, scope, and remediation status cannot be established here. Reports of compromised secrets and service disruption remain unverified in the available evidence.

hackernews · passenger · Oct 21, 21:58 · [Discussion](https://news.ycombinator.com/item?id=50188228)

**「Environment variables and secrets」** Deployment environment variables can hold credentials that applications use to access other services, so exposure can put those connected services at risk. The available excerpt of Railway’s disclosure says it detected anomalous activity involving systems that store customer environment variables, but does not establish whether credentials were exposed or how many customers were affected.

**「Postiz reports a customer-wide shutdown」** Postiz founder Nevo David said the service was shutting down for all customers after receiving notices from Anthropic and Stripe that its keys had been compromised. This is a reported service disruption, but his suspicion that Railway was compromised does not establish the cause or whether other Railway customers are affected.

**「Reports from the community」** One commenter reported seeing Railway Discord users say third parties had used their stored secrets, and inferred that attackers could read decrypted environment variables; that inference is not a confirmed technical finding. Another relayed an allegation from the Postiz founder that his keys had been used and his service was being disrupted, alongside criticism of Railway’s communication timing.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.railway.com/p/security-disclosure-wednesday-october-21st">Security Disclosure : Wednesday October 21st | Railway Blog</a></li>
<li><a href="https://x.com/wickedguro/status/2113015432974405658">Nevo David on X: &quot;We are currently shutting down Postiz for ...</a></li>

</ul>
</details>

**Tags**: `#Railway`, `#cloud-security`, `#secrets-management`, `#incident-response`

---

<a id="item-tech-news-7"></a>
### [GitLab Critical Patch Announcement Prompts Security Scrutiny](https://docs.gitlab.com/releases/patches/patch-release-gitlab-19-5-1-released/) ⭐️ 7.0/10

A GitLab critical patch announcement links to a release page for GitLab 19.5.1, warranting review by teams operating GitLab instances. The release text was not supplied, so the affected versions, precise vulnerability impact, patch availability, and upgrade instructions cannot be verified from this material.

hackernews · artooro · Oct 21, 19:01 · [Discussion](https://news.ycombinator.com/item?id=50185869)

**「GitLab’s patch release process」** GitLab distinguishes scheduled patch releases from ad-hoc critical patches for high-severity vulnerabilities. Its October 21 announcement lists fixes for both Community Edition \(CE\) and Enterprise Edition \(EE\) across seven release branches, so this is not limited to installations on the newest branch.

**「Reported exposure and log checks」** One commenter described a regex-related vulnerability involving an unauthenticated endpoint and welcomed reported guidance for checking logs for exploitation attempts; these details remain unverified without the release text. Another questioned whether the underlying bug was in GitLab or Ruby, highlighting uncertainty about its technical cause.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.gitlab.com/releases/patches/patch-release-gitlab-19-5-1-released/">GitLab Critical Patch Release... | GitLab Docs</a></li>

</ul>
</details>

**Tags**: `#GitLab`, `#security-patches`, `#vulnerabilities`, `#application-security`

---

<a id="item-tech-news-8"></a>
### [Meta reportedly ordered to pay $25 billion in New Mexico Cambridge Analytica case](https://www.cnbc.com/2026/10/21/meta-new-mexico-cambridge-analytica-penalty.html) ⭐️ 7.0/10

Meta has reportedly been ordered to pay a $25 billion penalty in New Mexico in a case related to Cambridge Analytica. The supplied item links to a New Mexico Department of Justice announcement describing a $25 billion penalty against Facebook, but includes neither the ruling nor substantive details of its legal basis. The available material does not establish whether the penalty is subject to further proceedings or how much Meta will ultimately pay.

hackernews · cbg0 · Oct 21, 17:45 · [Discussion](https://news.ycombinator.com/item?id=50184820)

**「Legal background」** The New Mexico case concerns allegations that Facebook deceived users about its data-privacy practices in connection with Cambridge Analytica. The monetary penalty follows a jury finding against Meta in a Santa Fe courthouse, with a state judge subsequently imposing the sanction.

**「Accountability and appeals」** One commenter argued that corporate fines alone are insufficient to deter misconduct and called for personal accountability for executives. Others focused on whether an appeal could reduce the penalty and whether New Mexico’s separate litigation would yield more than settlements elsewhere; their projected payouts and settlement comparisons are not verified by the supplied material.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/10/21/meta-new-mexico-cambridge-analytica-penalty.html">Meta ordered to pay $25B in New Mexico Cambridge Analytica case</a></li>
<li><a href="https://apnews.com/article/facebook-penalty-cambridge-analytica-new-mexico-b329f82c3d3db3758a159405acbd4d0e">Meta ordered to pay New Mexico $25 billion after Cambridge ...</a></li>

</ul>
</details>

**Tags**: `#Meta`, `#Cambridge Analytica`, `#data privacy`, `#regulatory enforcement`

---

<a id="item-tech-news-9"></a>
### [OpenAI announces plans to bring its models to Google Cloud](https://openai.com/index/openai-models-google-cloud/) ⭐️ 7.0/10

OpenAI has announced plans to bring its models to Google Cloud, adding an enterprise access channel. The supplied material does not include the announcement body, so the supported model lineup, availability dates, deployment architecture, and compatibility requirements cannot be confirmed. A secondary Telegram account describes Model Garden integration and Marketplace purchasing, but those details remain unverified here.

hackernews · armcat · Oct 21, 12:53 · [Discussion](https://news.ycombinator.com/item?id=50180079)

**「Distribution through Google Cloud」** The announcement connects two distinct parts of enterprise model access: Model Garden is the destination for OpenAI’s frontier models and Codex workflows, while Google Cloud Marketplace is the purchasing channel. That distribution arrangement alone does not establish which models are included or where inference will run.

**「Purchasing commitments draw attention」** A Hacker News commenter quoted a provision allowing enterprises to apply Google Cloud spending commitments toward these purchases, highlighting a potentially useful procurement benefit that cannot be verified from the missing announcement body. Another commenter framed the move as meeting customers’ preference to access inference through their existing cloud provider, rather than evidence that Google is losing confidence in Gemini.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/openai-models-google-cloud/">OpenAI models are coming to Google Cloud</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Google Cloud`, `#Enterprise AI`, `#Model Hosting`

---

<a id="item-tech-news-10"></a>
### [Uber details AutoClean workflow for removing obsolete feature flags](https://www.uber.com/us/en/blog/ai-code-cleanup/) ⭐️ 7.0/10

Uber described AutoClean, an AI-assisted system running across multiple internal monorepos to remove obsolete feature flags, and reported that it has removed more than 16,000 flags and over one million lines of code over the past few years. Its workflow combines AI agents with the deterministic code-transformation tool PolyglotPiranha, iteratively fixes CI failures, and then applies static checks and the multi-agent validation system CodeCourt before final human review. These are Uber-reported results; the supplied blog summary provides no accuracy, cost, or failure data and does not establish how much each component contributed to the cumulative cleanup.

telegram · zaihuapd · Oct 21, 06:45

**「Why feature flags need cleanup」** Feature flags let developers control whether a code path is enabled without removing it from the codebase. Once a flag is obsolete, its conditional branches can remain as technical debt; Uber’s AutoClean approach combines AI agents with deterministic code rewrites and validation to remove that stale logic.

**「Human review remains」** For Uber engineers, AutoClean automates code rewriting and validation while retaining final approval by a human reviewer. Uber says this lets reviewers focus on whether a flag should be removed rather than checking mechanical correctness, although the supplied account does not independently demonstrate that those checks eliminate correctness risks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.uber.com/us/en/blog/ai-code-cleanup/">Using AI to Delete Code : Agentic Tech Debt Cleanup at Uber</a></li>

</ul>
</details>

**Tags**: `#AI 编程`, `#技术债治理`, `#功能开关`, `#代码自动化`, `#软件工程`

---

<a id="item-tech-news-11"></a>
### [Intel and AMD Plan Unified x86 PyTorch Optimizations Through oneDNN](https://mp.weixin.qq.com/s/JcEFssHmhyL0drohofQNkg) ⭐️ 7.0/10

Intel and AMD announced plans to consolidate their x86 CPU optimizations for PyTorch in the open-source deep-learning library oneDNN, aiming to give developers a common software path across both vendors. According to the report, AMD is integrating ZenDNN optimizations into oneDNN and joining the UXL Foundation as a steering committee member. The companies are also collaborating on next-generation x86 AI instruction-set extensions, with future PyTorch integration planned through oneDNN. The brief report provides no release versions, delivery schedule, instruction-set details, or performance measurements, so it does not establish when developers can use the combined capabilities or what gains they will deliver.

telegram · zaihuapd · Oct 21, 08:55

**「A shared optimization layer」** oneDNN is an open-source deep-learning library that provides a shared destination for Intel’s and AMD’s x86 CPU optimizations used by PyTorch. According to the companies’ announcements, their alignment on oneDNN followed a recommendation from the x86 Ecosystem Advisory Group; AMD’s ZenDNN optimization work is being integrated into that common library rather than remaining a separate path.

<details><summary>References</summary>
<ul>
<li><a href="https://www.intel.com/content/www/us/en/newsroom/news/data-center/amd-intel-simplify-x86-ai-development-with-pytorch.html">AMD and Intel Collaborate to Simplify AI Development on x86 ...</a></li>
<li><a href="https://newsroom.amd.com/news/amd-intel-collaborate-simplify-ai-development-on-x86-cpus-pytorch/">Simplifying AI Development on x86 CPUs with PyTorch - AMD ...</a></li>

</ul>
</details>

**Tags**: `#x86`, `#PyTorch`, `#oneDNN`, `#AI计算`, `#开源生态`

---

<a id="item-tech-news-12"></a>
### [Cloudflare Reports Automatic WAF Protection for php2shell](https://blog.cloudflare.com/php-vulnerabilities-waf-protection/) ⭐️ 7.0/10

According to the supplied Telegram summary of Cloudflare’s announcement, Cloudflare has deployed automatic php2shell protection for all plans with WAF enabled, including the free plan. The report describes php2shell as involving two PHP flaws affecting PHP 5.4 and later, with potential denial-of-service, remote-code-execution, and data-disclosure consequences. Cloudflare says protection went live approximately nine hours before public disclosure and that it observed attack traffic targeting customers. The supplied account does not identify vulnerability IDs, exploitation conditions, or fixed PHP versions, so the precise exposure and protection coverage remain unverified.

telegram · zaihuapd · Oct 21, 14:43

**「WAF protection versus patching」** A web application firewall \(WAF\) filters web requests rather than fixing the underlying PHP software. Cloudflare describes its php2shell protections as an additional layer of defense and says customers should still patch PHP; the supplied account does not identify vulnerability numbers, exploitation prerequisites, or fixed versions.

**「Administrator action」** Cloudflare advises administrators to update PHP promptly and keep WAF protection enabled; the reported automatic coverage is conditional on WAF being enabled and should not be treated as a substitute for patching.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.cloudflare.com/php-vulnerabilities-waf-protection/">Cloudflare deploys protections against php 2 shell ... | Cloudflare Blog</a></li>

</ul>
</details>

**Tags**: `#PHP`, `#漏洞防护`, `#WAF`, `#远程代码执行`, `#Cloudflare`

---

<a id="item-tech-news-13"></a>
### [PHP Emergency Patch and Website Shutdowns Reported; Technical Details Unconfirmed](https://www.reuters.com/world/asia-pacific/eu-agency-warns-websites-may-need-be-taken-offline-php-prepares-patches-2026-10-21/) ⭐️ 7.0/10

A Telegram post linking to Reuters reports that PHP released an emergency security patch on October 21 and that government websites in the Netherlands, Denmark, Finland and France went offline as a precaution. It also reports partial shutdowns at Wikipedia and other websites, and says cybersecurity agencies in Europe, Australia, Japan and the UK urged operators to update or temporarily take sites offline. These claims are not independently verified in the supplied material, which contains no Reuters article text, CVE identifier, affected PHP versions, vulnerability mechanism or fixed release numbers.

telegram · zaihuapd · Oct 21, 17:22

**「PHP’s security advisories」** PHP’s advance advisory scheduled a security release for October 21, 2026, at 14:00 UTC to address two vulnerabilities, each rated Critical with a CVSS v4.0 score of 9.2. Its PHP 8.3.36 release announcement identifies them as CVE-2026-109618 and CVE-2026-109619 and says they can allow unauthenticated remote code execution. These official notices support the report’s claim of an urgent security fix, but do not establish the reported website shutdowns or the claim that the flaws had existed for more than a decade.

**「Operational uncertainty」** PHP website operators cannot determine from this post whether their deployments are affected or which release would resolve the reported vulnerability; those decisions require a primary security advisory specifying affected and fixed versions. The post’s additional references to risks in Node.js, Nginx, Go, Rust and LiteLLM provide no concrete advisories establishing a connection to the reported PHP issue.

<details><summary>References</summary>
<ul>
<li><a href="https://news-web.php.net/php.announce/509">php.announce: [ANNOUNCE] Upcoming Critical PHP Security Release</a></li>
<li><a href="https://news-web.php.net/php.announce/511">php.announce: [ANNOUNCE] PHP 8.3.36 Released</a></li>

</ul>
</details>

**Tags**: `#PHP`, `#漏洞修复`, `#网络安全`, `#网站运维`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Three Wall Street banks lead AI-driven equities revenue boom](https://www.cnbc.com/2026/10/21/goldman-sachs-jpmorgan-morgan-stanley-ai-trading.html) ⭐️ 7.0/10

Goldman Sachs, JPMorgan Chase and Morgan Stanley generated a combined $52 billion in equities revenue in the first nine months of 2026, nearly 80% of the five largest investment banks’ total, according to company filings cited by CNBC.

rss · CNBC Finance · Oct 21, 15:30

**「Background」** Their global trading networks and capacity to lend to large hedge funds help them capture demand for borrowed money to trade AI-related stocks, executives and analysts told CNBC. Revenue comparisons are imperfect because banks differ in which services and transaction taxes they include.

**Tags**: `#Investment banking`, `#Equities trading`, `#Prime brokerage`, `#AI stocks`, `#Hedge fund leverage`

---

<a id="item-finance-news-2"></a>
### [Super Micro raises revenue outlook; Musk reports SpaceX–Tesla merger talks](https://www.cnbc.com/2026/10/21/stocks-making-the-biggest-moves-premarket-spcx-smci-nflx-more.html) ⭐️ 7.0/10

Super Micro Computer raised its fiscal first-quarter revenue forecast to $18.5 billion–$19.5 billion from $14.5 billion–$15.5 billion, CNBC reported. Separately, Elon Musk said SpaceX and Tesla had formed special committees to discuss a merger; the report does not establish an agreed transaction.

rss · CNBC Finance · Oct 21, 11:49

**「Background」** Super Micro’s revenue outlook is a forecast rather than reported sales, while the SpaceX–Tesla merger discussions described by Musk are exploratory, not an announced deal.

**Tags**: `#Corporate earnings`, `#Revenue guidance`, `#Merger discussions`, `#Premarket trading`, `#Data center servers`

---