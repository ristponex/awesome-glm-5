# 🧠 Awesome GLM-5 — The Open-Source MoE Giant from Zhipu AI

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GLM-5](https://img.shields.io/badge/GLM--5-744B%20MoE-blue.svg)](https://github.com/THUDM)
[![Try on Atlas Cloud](https://img.shields.io/badge/Try-Atlas%20Cloud-green.svg)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**Language / 语言:** English | [中文](README_zh.md) | [日本語](README_ja.md) | [한국어](README_ko.md)

---

> 🔥 **GLM-5 is now available!** The 744B open-source MoE model from Zhipu AI. GLM-5-Turbo optimized for agents launched March 16, 2026.

---

## Table of Contents

- [What is GLM-5?](#what-is-glm-5)
- [GLM-5 vs GLM-5-Turbo](#glm-5-vs-glm-5-turbo)
- [Key Features](#key-features)
- [Performance Benchmarks](#performance-benchmarks)
- [Architecture](#architecture)
- [Try GLM-5 on Atlas Cloud](#-try-glm-5-on-atlas-cloud)
- [API Quick Start](#api-quick-start)
- [Pricing Comparison](#pricing-comparison)
- [Community Resources](#community-resources)
- [FAQ](#faq)

---

## What is GLM-5?

**GLM-5** is the latest flagship large language model from [Zhipu AI](https://www.zhipuai.cn/) (智谱AI), released in February 2026. It's a **744 billion parameter Mixture-of-Experts (MoE)** model with only **40B parameters active** during inference, delivering frontier performance at a fraction of the compute cost.

Key highlights:

- 🏗️ **744B total / 40B active** — MoE architecture for efficient inference
- 📖 **200K context window** — process massive documents and codebases
- 🔓 **MIT License** — fully open-source weights on HuggingFace & ModelScope
- 🇨🇳 **100% Ascend-trained** — zero NVIDIA dependency, trained on Huawei Ascend chips
- 🧑‍💻 **SWE-bench 77.8%** — near state-of-the-art coding capabilities
- 🧮 **AIME 2026: 92.7%** — exceptional mathematical reasoning
- 🤖 **Agent-ready** — GLM-5-Turbo optimized for tool use and agentic workflows

GLM-5 represents a major leap from GLM-4.7 (355B params), nearly doubling the parameter count while significantly reducing hallucinations by 56%.

---

## GLM-5 vs GLM-5-Turbo

| Feature | GLM-5 | GLM-5-Turbo |
|---------|-------|-------------|
| **Parameters** | 744B total / 40B active | Optimized (closed) |
| **Context Window** | 200K tokens | 200K input / 128K output |
| **License** | MIT (open-source) | Closed source |
| **Optimized For** | General purpose | Agents & tool calling |
| **Speed** | Standard | ~48 tokens/s (OpenRouter) |
| **Best For** | Self-hosting, research, fine-tuning | Production agent workflows |
| **Release Date** | Feb 11, 2026 | Mar 16, 2026 |
| **Availability** | HuggingFace, ModelScope | Z.ai, Atlas Cloud, OpenRouter |

---

## Key Features

### 🧑‍💻 Coding Excellence
- **SWE-bench Verified: 77.8%** — surpasses DeepSeek V3.2 and Kimi K2.5
- Excels at repository-level comprehension, multi-file reasoning, and complex refactoring
- 20%+ improvement in frontend, backend, and long-running dev tasks vs GLM-4.7

### 🧮 Mathematical Reasoning
- **AIME 2026: 92.7%** — competition-level math problem solving
- Strong chain-of-thought and step-by-step reasoning

### 🤖 Agent Capabilities (GLM-5-Turbo)
- Designed for **OpenClaw** ecosystem and agentic engineering
- Advanced tool calling, instruction following, and long-chain execution
- Supports timed/persistent tasks

### 🔒 Reduced Hallucinations
- **56% lower hallucination rate** compared to GLM-4.7
- More reliable for factual tasks and production use

### 🇨🇳 Domestic Chip Independence
- Fully trained on **Huawei Ascend** chips with **MindSpore** framework
- Compatible with Moore Threads, Hygon, Cambricon, Kunlun, and other Chinese chips
- Uses **DeepSeek Sparse Attention (DSA)** for efficient long-context handling

---

## Performance Benchmarks

| Benchmark | GLM-5 | GLM-4.7 | DeepSeek V3.2 | Claude Opus 4.5 |
|-----------|-------|---------|---------------|-----------------|
| **SWE-bench Verified** | 77.8% | — | ~75% | 80.9% |
| **AIME 2026** | 92.7% | — | — | — |
| **BrowseComp** | 62.0 | — | — | — |
| **AA Intelligence Index** | 50 | 42 | — | — |
| **Hallucination Reduction** | -56% vs GLM-4.7 | baseline | — | — |

> 📊 GLM-5 achieves frontier-level performance while being fully open-source under MIT license.

---

## Architecture

```
GLM-5 Architecture Overview
├── Total Parameters: 744B (vs 355B in GLM-4.7)
├── Active Parameters: 40B (vs 32B in GLM-4.7)
├── Architecture: Mixture of Experts (MoE)
├── Pre-training Data: 28.5T tokens (vs 23T in GLM-4.7)
├── Context Window: 200K tokens
├── Attention: DeepSeek Sparse Attention (DSA)
├── Training Framework: MindSpore on Huawei Ascend
├── Training Tool: "Slime" framework with async agent RL
└── MoE Flop Utilization: >75% (industry avg: 40-50%)
```

---

## ⚡ Try GLM-5 on Atlas Cloud

[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5) provides GLM-5 via a fully managed, **OpenAI-compatible API**. No infrastructure to manage — just plug in and go.

### Why Atlas Cloud?

- 🔌 **OpenAI-compatible API** — works with any OpenAI SDK, drop-in replacement
- 💰 **Up to 88% cheaper** than alternatives like fal.ai and official APIs
- 🔒 **SOC I & II Certified** | **HIPAA Compliant**
- ⚡ **Serverless & auto-scaling** — no GPUs to manage
- 🌐 **300+ AI models** — access GLM-5, DeepSeek, Qwen, and more from one API
- 🆓 **Free credits** for new users, no credit card required

> 💡 **[Sign up at Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5) and get free credits to start using GLM-5 today!**

---

## API Quick Start

Atlas Cloud API is **100% OpenAI-compatible**. If you've used the OpenAI SDK, you already know how to use it.

### Python

```python
from openai import OpenAI

client = OpenAI(
    api_key="your-atlas-cloud-api-key",
    base_url="https://api.atlascloud.ai/v1"
)

response = client.chat.completions.create(
    model="zhipu/glm-5-turbo",
    messages=[
        {"role": "system", "content": "You are an expert software engineer."},
        {"role": "user", "content": "Implement a thread-safe LRU cache in Python with O(1) get and put operations."}
    ],
    temperature=0.7,
    max_tokens=4096
)

print(response.choices[0].message.content)
```

### cURL

```bash
curl https://api.atlascloud.ai/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer your-atlas-cloud-api-key" \
  -d '{
    "model": "zhipu/glm-5-turbo",
    "messages": [
      {"role": "system", "content": "You are an expert software engineer."},
      {"role": "user", "content": "Design a microservices architecture for an e-commerce platform."}
    ],
    "temperature": 0.7,
    "max_tokens": 4096
  }'
```

### Node.js

```javascript
import OpenAI from 'openai';

const client = new OpenAI({
  apiKey: 'your-atlas-cloud-api-key',
  baseURL: 'https://api.atlascloud.ai/v1'
});

const response = await client.chat.completions.create({
  model: 'zhipu/glm-5-turbo',
  messages: [
    { role: 'system', content: 'You are an expert software engineer.' },
    { role: 'user', content: 'Create a real-time WebSocket server with auth and rate limiting in Node.js.' }
  ],
  temperature: 0.7,
  max_tokens: 4096
});

console.log(response.choices[0].message.content);
```

---

## Pricing Comparison

### GLM-5-Turbo vs Competitors

| Model | Input (per M tokens) | Output (per M tokens) | Relative Cost |
|-------|---------------------|----------------------|---------------|
| **GLM-5-Turbo** | **$1.20** | **$4.00** | **1x (baseline)** |
| GPT-5.4 | ~$10.00 | ~$30.00 | ~8x more expensive |
| Claude Opus 4.5 | ~$15.00 | ~$75.00 | ~12x more expensive |
| DeepSeek V3.2 | $0.26 | $0.38 | Cheaper but less capable |

> 💡 GLM-5-Turbo delivers frontier-level agent capabilities at a fraction of the cost of GPT-5.4 and Claude Opus 4.5.

### GLM-5 on Zhipu Platform (CNY)

| Context | Input (per M tokens) | Output (per M tokens) |
|---------|---------------------|----------------------|
| ≤32K | ¥4.00 | ¥18.00 |
| >32K | ¥6.00 | ¥22.00 |

---

## Community Resources

### Official Resources
- 📄 [GLM-5 Technical Report (arXiv: 2602.15763)](https://arxiv.org/html/2602.15763v1)
- 🤗 [GLM-5 on HuggingFace](https://huggingface.co/zai-org/GLM-5)
- 📦 [GLM-5 on ModelScope](https://modelscope.cn/models/ZhipuAI/GLM-5)
- 🔧 [GLM-5-Turbo API Docs (Z.AI)](https://docs.z.ai/guides/llm/glm-5-turbo)
- 📚 [BigModel Platform Docs](https://docs.bigmodel.cn/cn/guide/models/text/glm-5)
- 🎮 [NVIDIA NIM - GLM-5](https://build.nvidia.com/z-ai/glm5/modelcard)

### Articles & Analysis
- 📰 [The Decoder: Chinese AI lab Zhipu releases GLM-5 under MIT license](https://the-decoder.com/chinese-ai-lab-zhipu-releases-glm-5-under-mit-license-claims-parity-with-top-western-models/)
- 📊 [Artificial Analysis: GLM-5 Everything You Need to Know](https://artificialanalysis.ai/articles/glm-5-everything-you-need-to-know)
- 🔬 [WaveSpeed AI: GLM-5 vs GLM-4.7 Benchmarks](https://wavespeed.ai/blog/posts/blog-glm-5-vs-glm-4-7-upgrade-benchmarks/)
- 📝 [BuildFastWithAI: GLM-5 Released](https://www.buildfastwithai.com/blogs/glm-5-released-open-source-model-2026)
- 📝 [BuildFastWithAI: GLM-5-Turbo for OpenClaw](https://www.buildfastwithai.com/blogs/glm-5-turbo-openclaw-agent-model)
- 🏦 [SCMP: China's Zhipu AI launches GLM-5](https://www.scmp.com/tech/article/3343239/chinas-zhipu-ai-launches-new-major-model-glm-5-challenge-its-rivals)

---

## FAQ

### 1. What's the difference between GLM-5 and GLM-5-Turbo?

**GLM-5** is the open-source base model (744B MoE, MIT license) for self-hosting and research. **GLM-5-Turbo** is a closed-source, optimized version designed for agent workflows and production use, with faster inference and specialized tool-calling capabilities.

### 2. Can I self-host GLM-5?

Yes! GLM-5 is fully open-source under MIT license. Weights are available on [HuggingFace](https://huggingface.co/zai-org/GLM-5) and ModelScope. However, at 744B parameters, you'll need significant GPU resources. For most users, we recommend using it via [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5).

### 3. Is GLM-5 really trained without NVIDIA GPUs?

Yes. GLM-5 was trained entirely on Huawei Ascend chips using the MindSpore framework, making it the first frontier model to demonstrate full independence from NVIDIA hardware.

### 4. How does GLM-5 compare to DeepSeek V3.2?

GLM-5 scores higher on SWE-bench Verified (77.8% vs ~75%) and has a much larger parameter count (744B vs ~671B). However, DeepSeek V3.2 is significantly cheaper. GLM-5-Turbo offers a middle ground with strong agent capabilities at competitive pricing.

### 5. What is OpenClaw?

OpenClaw is Zhipu AI's agent ecosystem, similar to Claude Code or OpenAI's Codex. GLM-5-Turbo is specifically optimized for OpenClaw workflows including tool calling, instruction following, and long-chain task execution.

---

## Get Started Today

Don't just read about GLM-5 — **try it now on Atlas Cloud**.

| Feature | Details |
|---------|---------|
| **Model** | GLM-5 / GLM-5-Turbo |
| **API** | OpenAI-compatible |
| **Pricing** | Up to 88% cheaper than alternatives |
| **Security** | SOC I & II Certified, HIPAA Compliant |
| **Free Tier** | Free credits, no credit card required |

<div align="center">

### [👉 Try GLM-5 on Atlas Cloud — Free Credits 👈](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)

</div>

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

- Found a bug or have a suggestion? [Open an issue](https://github.com/ristponex/awesome-glm-5/issues)
- Want to add a resource? Submit a PR!

---

## Star History

If you find this resource useful, please give it a ⭐!

---

<div align="center">

**Made with ❤️ by the open-source community**

[⬆ Back to Top](#-awesome-glm-5--the-open-source-moe-giant-from-zhipu-ai)

</div>
