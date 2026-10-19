---
layout: default
title: "Horizon Summary: 2026-10-19 (ZH)"
date: 2026-10-19
lang: zh
---

> 从 34 条内容中筛选出 2 条重要资讯。

---

**科技新闻**
1. [vLLM v0.32.0 新增结构化决策接口，扩展低精度 KV 缓存](#item-tech-news-1) ⭐️ 7.0/10
2. [消息称 Linux 校验和漏洞可致 KVM 访客逃逸](#item-tech-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [vLLM v0.32.0 新增结构化决策接口，扩展低精度 KV 缓存](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) ⭐️ 7.0/10

vLLM v0.32.0 已发布，为模型推理服务新增默认启用的 \`POST /v1/systemone\` 接口，可针对结构化状态回答 \`choice\`、\`noul\` 和 \`score\` 问题。新的 \`hf\` 工具调用与推理解析器通过 \`--tool-call-parser hf\` 和 \`--reasoning-parser hf\` 启用，读取模型检查点中的 \`response\_template\`；提供该模板的模型无需专用解析器，Python 与 Rust 前端均支持。低精度 KV 缓存支持进一步扩展：NVFP4 覆盖更多 NVIDIA GPU 架构，ROCm 新增四位 \`ultraquant\_4bit\`，GLM-5.x 在 SM100 上默认使用 FP8 KV 缓存。发布说明引用的 PR 基准显示，后一配置每个 rank 的 KV 内存减半、吞吐量提高 2.3%–5.5%，但首 token 延迟增加 7%–11%；这些是特定配置的项目方测试结果，并非整个版本的普遍收益。

github · khluu · 10月18日 06:50

**「技术背景」** KV 缓存用于保存模型生成过程中可复用的注意力键值数据；降低缓存精度可以减少其内存占用，但实际收益取决于模型、GPU 架构和注意力实现，不能等同于整个模型的内存用量同比下降。工具调用与推理解析器则负责识别模型输出中的对应结构，因此，从检查点的 response\_template 读取解析规则这一机制，以模型检查点提供该模板为前提。

**「升级兼容性」** 现有部署升级前需要检查运行环境和客户端兼容性：本版不再支持 Python 3.10，依赖要求变为 \`transformers&gt;=5.16.1,&lt;5.20.0\` 和 \`tokenizers&gt;=0.23.2\`。默认 CORS 不再允许所有来源，依赖跨域访问的应用应检查来源配置；消费 Responses API 推理流事件的客户端也需适配重命名后的事件。

**标签**: `#vLLM`, `#LLM inference`, `#KV-cache quantization`, `#AI infrastructure`, `#Open source`

---

<a id="item-tech-news-2"></a>
### [消息称 Linux 校验和漏洞可致 KVM 访客逃逸](http://pwn.ai/) ⭐️ 7.0/10

一则 Telegram 消息称，PWN.AI 披露了编号为 CVE-2026-99999 的 Linux 内核漏洞，并在自有 KVM 环境中演示了从访客到宿主机的逃逸。按该消息描述，漏洞涉及网络校验和元数据，可在内核完成校验后改写 IPv4 头，造成 32 字节宿主机内存信息泄露。消息还称修复补丁已于 2026 年 10 月 14 日合入主线，但所附链接仅指向站点首页，未提供研究原文、补丁、受影响版本或利用前提，因此漏洞编号、修复状态及逃逸适用范围均无法据此核实。

telegram · zaihuapd · 10月18日 09:47

**「漏洞所在的信任边界」** PWN.AI 的研究说明称，问题位于 Linux 网络栈，而非虚拟机监控器本身，涉及 CHECKSUM\_PARTIAL 校验和处理中的信任边界：网络包通过校验后，后续校验和写入仍可能改动 IPv4 头。AlmaLinux 的补丁说明指出，修复是在内核完成校验和计算前检查校验和写入位置是否合法，这解释了为何虚拟机逃逸问题需要在 Linux 网络栈中修补。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pwn.ai/blog/pwnescape">PwnEscape: Guest-to-Host KVM Escape (CVE-2026-99999)</a></li>
<li><a href="https://www.pwn.ai/">pwn.ai — Autonomous Penetration Testing | AI-Powered Security ...</a></li>
<li><a href="https://almalinux.org/blog/2026-10-16-pwnescape-cve-2026-99999/">PwnEscape ( CVE - 2026 - 99999 ): Patched kernels ... | AlmaLinux OS</a></li>

</ul>
</details>

**标签**: `#Linux 内核`, `#KVM`, `#虚拟机逃逸`, `#漏洞研究`, `#内存信息泄露`

---