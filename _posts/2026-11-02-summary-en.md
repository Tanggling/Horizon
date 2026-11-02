---
layout: default
title: "Horizon Summary: 2026-11-02 (EN)"
date: 2026-11-02
lang: en
---

> From 29 items, 2 important content pieces were selected

---

**Technology News**
1. [OmniDiff v0.3.0 offers content-aware Git diffs across code and binary formats](#item-tech-news-1) ⭐️ 7.0/10
2. [Lenovo fingerprint USB reportedly stores data on unencrypted SD card](#item-tech-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OmniDiff v0.3.0 offers content-aware Git diffs across code and binary formats](https://github.com/ivankovic/omnidiff) ⭐️ 7.0/10

OmniDiff v0.3.0 is an AGPLv3-licensed Git difftool written in Rust, offering developers content-aware comparisons for 25 programming languages plus configuration files, images, PDFs, archives, cursors, and fonts. The author reports diffing C++ files tens of thousands of lines long in under 100 milliseconds on a 2023 ThinkPad T14s; no independent benchmark is supplied. According to the author, 2,000 manually analyzed diffs sampled from 7,400 repositories listed in Gentoo packages informed the content-specific pipelines and form the basis of its CI tests. The project remains under development, although the author reports using it daily as their Git difftool for months.

hackernews · FabCH · Nov 1, 13:02 · [Discussion](https://news.ycombinator.com/item?id=50325253)

**「Beyond line-by-line diffs」** Content-aware diffing uses format-specific comparison logic rather than relying solely on changed lines of text. Git supports external comparison tools through \`git difftool\`, which OmniDiff’s documentation specifies—not \`git diff\`—for opening its interactive viewer.

**「Workflow and integration questions」** Commenters compared OmniDiff with Delta, asking about piped \`git diff\` input without global configuration changes and reporting difficulty finding Delta-style character-level highlighting in OmniDiff&\#x27;s README or web version. The self-identified creator of \`git difftool\` also asked about three-way merge comparisons and offered help upstreaming OmniDiff integration into Git to simplify setup; these remain questions and proposals rather than confirmed capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ivankovic/omnidiff/tree/main">GitHub - ivankovic/omnidiff: Fast, robust, accurate diffing</a></li>

</ul>
</details>

**Tags**: `#Git`, `#diffing`, `#Rust`, `#developer-tools`, `#open-source`

---

<a id="item-tech-news-2"></a>
### [Lenovo fingerprint USB reportedly stores data on unencrypted SD card](https://www.reddit.com/r/technology/comments/1xl2pr3/lenovos_encrypted_fingerprint_usb_drive_is_just/) ⭐️ 7.0/10

A Lenovo fingerprint USB drive reportedly contains an unencrypted SD card that can be removed and read directly, bypassing the drive’s advertised protection. The supplied headline and discussion provide neither a device model nor primary testing evidence, so the claim remains unverified and the affected scope is unknown.

hackernews · entryleveljobsc · Nov 1, 14:34 · [Discussion](https://news.ycombinator.com/item?id=50326099)

**「Authentication versus encryption」** The linked Tom’s Hardware report describes a Lenovo ThinkPlus-branded fingerprint USB stick with a microSD card in an internal socket. Fingerprint authentication can restrict access through the USB interface, but encryption at rest is a separate safeguard: it should keep stored data unreadable without a decryption key even when the storage medium is removed.

**「Trusting hardware encryption」** One commenter recommends adding free-software encryption rather than relying on the drive’s advertised security. Another argues that opaque hardware-encryption implementations can introduce both security weaknesses and additional failure points that complicate data recovery.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/cyber-security/lenovo-fingerprint-usb-stick-sold-as-aes-256-encrypted-had-a-plain-sd-card-inside-ai-assisted-follow-up-finds-a-backdoor-and-hardcoded-keys-in-other-secure-usb-products">Lenovo &#x27;s &#x27;encrypted&#x27; fingerprint USB drive is just... | Tom &#x27; s ...</a></li>

</ul>
</details>

**Tags**: `#hardware-security`, `#usb-storage`, `#encryption`, `#biometric-authentication`

---