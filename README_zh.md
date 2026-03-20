# 🧠 Awesome GLM-5 — 智谱AI开源MoE巨作

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GLM-5](https://img.shields.io/badge/GLM--5-744B%20MoE-blue.svg)](https://github.com/THUDM)
[![Try on Atlas Cloud](https://img.shields.io/badge/Try-Atlas%20Cloud-green.svg)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**Language / 语言:** [English](README.md) | 中文 | [日本語](README_ja.md) | [한국어](README_ko.md)

---

> 🔥 **GLM-5 已发布！** 智谱AI推出的744B开源MoE模型。GLM-5-Turbo（Agent优化版）于2026年3月16日上线。

---

## 目录

- [什么是 GLM-5？](#什么是-glm-5)
- [GLM-5 vs GLM-5-Turbo](#glm-5-vs-glm-5-turbo)
- [核心特性](#核心特性)
- [性能基准](#性能基准)
- [架构](#架构)
- [在 Atlas Cloud 上使用 GLM-5](#-在-atlas-cloud-上使用-glm-5)
- [API 快速开始](#api-快速开始)
- [价格对比](#价格对比)
- [社区资源](#社区资源)
- [常见问题](#常见问题)

---

## 什么是 GLM-5？

**GLM-5** 是[智谱AI](https://www.zhipuai.cn/)于2026年2月发布的最新旗舰大语言模型。采用**7440亿参数混合专家（MoE）架构**，推理时仅激活**400亿参数**，以极低的计算成本实现前沿性能。

核心亮点：

- 🏗️ **744B总参/40B激活** — MoE架构实现高效推理
- 📖 **200K上下文窗口** — 处理超大文档和代码库
- 🔓 **MIT许可证** — 权重在HuggingFace和ModelScope完全开源
- 🇨🇳 **全国产芯片训练** — 基于华为昇腾芯片+MindSpore框架，零NVIDIA依赖
- 🧑‍💻 **SWE-bench 77.8%** — 接近最先进的编码能力
- 🧮 **AIME 2026: 92.7%** — 卓越的数学推理能力
- 🤖 **Agent就绪** — GLM-5-Turbo专为工具调用和智能体工作流优化

---

## GLM-5 vs GLM-5-Turbo

| 特性 | GLM-5 | GLM-5-Turbo |
|------|-------|-------------|
| **参数量** | 744B总/40B激活 | 优化版（闭源） |
| **上下文窗口** | 200K tokens | 200K输入/128K输出 |
| **许可证** | MIT（开源） | 闭源 |
| **优化方向** | 通用 | Agent和工具调用 |
| **推理速度** | 标准 | ~48 tokens/s |
| **适用场景** | 自部署、研究、微调 | 生产级Agent工作流 |
| **发布日期** | 2026年2月11日 | 2026年3月16日 |

---

## 核心特性

### 🧑‍💻 编程能力
- **SWE-bench Verified: 77.8%** — 超越DeepSeek V3.2和Kimi K2.5
- 前后端、长链任务等开发场景比GLM-4.7提升20%+

### 🧮 数学推理
- **AIME 2026: 92.7%** — 竞赛级数学问题求解

### 🤖 Agent能力（GLM-5-Turbo）
- 为**OpenClaw**生态和智能体工程设计
- 高级工具调用、指令遵循、长链执行

### 🔒 幻觉率降低56%
- 相比GLM-4.7大幅减少幻觉，更可靠

---

## 性能基准

| 基准测试 | GLM-5 | GLM-4.7 | DeepSeek V3.2 | Claude Opus 4.5 |
|---------|-------|---------|---------------|-----------------|
| **SWE-bench Verified** | 77.8% | — | ~75% | 80.9% |
| **AIME 2026** | 92.7% | — | — | — |
| **BrowseComp** | 62.0 | — | — | — |
| **AA Intelligence Index** | 50 | 42 | — | — |
| **幻觉率降低** | -56% vs GLM-4.7 | 基准 | — | — |

---

## 架构

```
GLM-5 架构概览
├── 总参数量：744B（GLM-4.7为355B）
├── 激活参数：40B（GLM-4.7为32B）
├── 架构：混合专家（MoE）
├── 预训练数据：28.5T tokens（GLM-4.7为23T）
├── 上下文窗口：200K tokens
├── 注意力机制：DeepSeek稀疏注意力（DSA）
├── 训练框架：华为昇腾 + MindSpore
├── 训练工具："Slime"异步智能体强化学习框架
└── MoE Flop利用率：>75%（行业平均40-50%）
```

---

## ⚡ 在 Atlas Cloud 上使用 GLM-5

[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5) 提供GLM-5的全托管**OpenAI兼容API**，无需管理基础设施。

### 为什么选择 Atlas Cloud？

- 🔌 **OpenAI兼容API** — 支持任何OpenAI SDK，即插即用
- 💰 **比其他方案便宜最高88%**
- 🔒 **SOC I & II认证** | **HIPAA合规**
- ⚡ **无服务器自动扩缩** — 无需管理GPU
- 🌐 **300+AI模型** — 一个API访问GLM-5、DeepSeek、Qwen等
- 🆓 **新用户免费额度**，无需信用卡

> 💡 **[注册Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)，获取免费额度立即使用GLM-5！**

---

## API 快速开始

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
        {"role": "system", "content": "你是一位专业的软件工程师。"},
        {"role": "user", "content": "用Python实现一个线程安全的LRU缓存，要求get和put操作都是O(1)。"}
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
      {"role": "user", "content": "设计一个电商平台的微服务架构"}
    ]
  }'
```

---

## 价格对比

| 模型 | 输入（每百万token） | 输出（每百万token） | 相对成本 |
|------|-------------------|-------------------|---------|
| **GLM-5-Turbo** | **$1.20** | **$4.00** | **1x（基准）** |
| GPT-5.4 | ~$10.00 | ~$30.00 | ~8倍 |
| Claude Opus 4.5 | ~$15.00 | ~$75.00 | ~12倍 |
| DeepSeek V3.2 | $0.26 | $0.38 | 更便宜但能力弱 |

---

## 社区资源

- 📄 [GLM-5技术报告 (arXiv: 2602.15763)](https://arxiv.org/html/2602.15763v1)
- 🤗 [GLM-5 HuggingFace](https://huggingface.co/zai-org/GLM-5)
- 📦 [GLM-5 ModelScope](https://modelscope.cn/models/ZhipuAI/GLM-5)
- 🔧 [GLM-5-Turbo API文档](https://docs.z.ai/guides/llm/glm-5-turbo)
- 📚 [大模型开放平台文档](https://docs.bigmodel.cn/cn/guide/models/text/glm-5)

---

## 常见问题

### 1. GLM-5和GLM-5-Turbo有什么区别？
**GLM-5**是开源基座模型（MIT许可证），适合自部署和研究。**GLM-5-Turbo**是闭源优化版，专为Agent工作流和生产环境设计。

### 2. 可以自己部署GLM-5吗？
可以！权重在HuggingFace和ModelScope开源。但744B参数需要大量GPU资源，大多数用户建议通过[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)使用。

### 3. GLM-5真的没有用NVIDIA GPU训练吗？
是的，完全基于华为昇腾芯片和MindSpore框架训练，是首个证明完全脱离NVIDIA硬件的前沿模型。

---

<div align="center">

### [👉 在Atlas Cloud上试用GLM-5 — 免费额度 👈](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)

**Made with ❤️ by the open-source community**

[⬆ 回到顶部](#-awesome-glm-5--智谱ai开源moe巨作)

</div>
