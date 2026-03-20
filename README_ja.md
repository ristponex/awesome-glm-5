# 🧠 Awesome GLM-5 — Zhipu AIのオープンソースMoE大規模モデル

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GLM-5](https://img.shields.io/badge/GLM--5-744B%20MoE-blue.svg)](https://github.com/THUDM)
[![Try on Atlas Cloud](https://img.shields.io/badge/Try-Atlas%20Cloud-green.svg)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**Language / 言語:** [English](README.md) | [中文](README_zh.md) | 日本語 | [한국어](README_ko.md)

---

> 🔥 **GLM-5が公開されました！** Zhipu AIの744Bオープンソース MoEモデル。エージェント最適化版GLM-5-Turboは2026年3月16日リリース。

---

## 目次

- [GLM-5とは？](#glm-5とは)
- [GLM-5 vs GLM-5-Turbo](#glm-5-vs-glm-5-turbo)
- [主な特徴](#主な特徴)
- [ベンチマーク](#ベンチマーク)
- [Atlas Cloudで試す](#-atlas-cloudでglm-5を試す)
- [APIクイックスタート](#apiクイックスタート)
- [料金比較](#料金比較)
- [コミュニティリソース](#コミュニティリソース)
- [FAQ](#faq)

---

## GLM-5とは？

**GLM-5**は[Zhipu AI](https://www.zhipuai.cn/)（智谱AI）が2026年2月にリリースした最新フラッグシップLLMです。**7440億パラメータのMixture-of-Experts（MoE）アーキテクチャ**を採用し、推論時は**400億パラメータのみ**を活性化します。

- 🏗️ **744B総パラメータ / 40B活性化** — 効率的なMoEアーキテクチャ
- 📖 **200Kコンテキストウィンドウ**
- 🔓 **MITライセンス** — HuggingFace・ModelScopeで完全オープンソース
- 🇨🇳 **Huawei Ascendチップで完全訓練** — NVIDIAゼロ依存
- 🧑‍💻 **SWE-bench 77.8%** — 最先端に近いコーディング能力
- 🧮 **AIME 2026: 92.7%** — 卓越した数学推論
- 🤖 **エージェント対応** — GLM-5-Turboはツール呼び出しとエージェントワークフローに最適化

---

## GLM-5 vs GLM-5-Turbo

| 特徴 | GLM-5 | GLM-5-Turbo |
|------|-------|-------------|
| **パラメータ** | 744B総 / 40B活性 | 最適化版（クローズド） |
| **コンテキスト** | 200K tokens | 200K入力 / 128K出力 |
| **ライセンス** | MIT（オープンソース） | クローズドソース |
| **最適化** | 汎用 | エージェント・ツール呼び出し |
| **推論速度** | 標準 | ~48 tokens/s |
| **リリース日** | 2026年2月11日 | 2026年3月16日 |

---

## 主な特徴

### 🧑‍💻 コーディング
- **SWE-bench Verified: 77.8%** — DeepSeek V3.2やKimi K2.5を上回る
- GLM-4.7比で開発タスク20%+向上

### 🧮 数学推論
- **AIME 2026: 92.7%** — コンペティションレベル

### 🤖 エージェント能力（GLM-5-Turbo）
- **OpenClaw**エコシステム向けに最適化
- ツール呼び出し、長鎖実行、タイマータスク対応

### 🔒 ハルシネーション56%削減
- GLM-4.7比で大幅に信頼性向上

---

## ベンチマーク

| ベンチマーク | GLM-5 | GLM-4.7 | DeepSeek V3.2 | Claude Opus 4.5 |
|------------|-------|---------|---------------|-----------------|
| **SWE-bench Verified** | 77.8% | — | ~75% | 80.9% |
| **AIME 2026** | 92.7% | — | — | — |
| **BrowseComp** | 62.0 | — | — | — |
| **AA Intelligence Index** | 50 | 42 | — | — |

---

## ⚡ Atlas CloudでGLM-5を試す

[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)はGLM-5を**OpenAI互換API**で提供します。

- 🔌 **OpenAI互換** — 既存のOpenAI SDKがそのまま使える
- 💰 **代替サービスより最大88%安い**
- 🔒 **SOC I & II認証** | **HIPAA準拠**
- 🌐 **300以上のAIモデル** — 1つのAPIでGLM-5、DeepSeek、Qwenなどにアクセス
- 🆓 **無料クレジット**付き、クレジットカード不要

> 💡 **[Atlas Cloudに登録](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)して、無料でGLM-5を試しましょう！**

---

## APIクイックスタート

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
        {"role": "user", "content": "Pythonでスレッドセーフなキャッシュを実装してください。"}
    ]
)

print(response.choices[0].message.content)
```

---

## 料金比較

| モデル | 入力（100万トークン） | 出力（100万トークン） | 相対コスト |
|-------|--------------------|--------------------|-----------|
| **GLM-5-Turbo** | **$1.20** | **$4.00** | **1x** |
| GPT-5.4 | ~$10.00 | ~$30.00 | ~8倍 |
| Claude Opus 4.5 | ~$15.00 | ~$75.00 | ~12倍 |

---

## コミュニティリソース

- 📄 [GLM-5技術レポート](https://arxiv.org/html/2602.15763v1)
- 🤗 [GLM-5 HuggingFace](https://huggingface.co/zai-org/GLM-5)
- 🔧 [GLM-5-Turbo APIドキュメント](https://docs.z.ai/guides/llm/glm-5-turbo)

---

## FAQ

### 1. GLM-5とGLM-5-Turboの違いは？
**GLM-5**はオープンソース基盤モデル（MITライセンス）。**GLM-5-Turbo**はエージェント向けに最適化されたクローズドソース版です。

### 2. GLM-5をセルフホストできますか？
はい！HuggingFaceで重みが公開されています。ただし744Bパラメータには大規模なGPUリソースが必要です。ほとんどのユーザーには[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)をお勧めします。

---

<div align="center">

### [👉 Atlas CloudでGLM-5を試す — 無料クレジット 👈](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)

[⬆ トップに戻る](#-awesome-glm-5--zhipu-aiのオープンソースmoe大規模モデル)

</div>
