# 🧠 Awesome GLM-5 — Zhipu AI의 오픈소스 MoE 대규모 모델

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GLM-5](https://img.shields.io/badge/GLM--5-744B%20MoE-blue.svg)](https://github.com/THUDM)
[![Try on Atlas Cloud](https://img.shields.io/badge/Try-Atlas%20Cloud-green.svg)](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**Language / 언어:** [English](README.md) | [中文](README_zh.md) | [日本語](README_ja.md) | 한국어

---

> 🔥 **GLM-5 출시!** Zhipu AI의 744B 오픈소스 MoE 모델. 에이전트 최적화 버전 GLM-5-Turbo는 2026년 3월 16일 출시.

---

## 목차

- [GLM-5란?](#glm-5란)
- [GLM-5 vs GLM-5-Turbo](#glm-5-vs-glm-5-turbo)
- [주요 특징](#주요-특징)
- [벤치마크](#벤치마크)
- [Atlas Cloud에서 사용하기](#-atlas-cloud에서-glm-5-사용하기)
- [API 빠른 시작](#api-빠른-시작)
- [가격 비교](#가격-비교)
- [커뮤니티 리소스](#커뮤니티-리소스)
- [FAQ](#faq)

---

## GLM-5란?

**GLM-5**는 [Zhipu AI](https://www.zhipuai.cn/)(智谱AI)가 2026년 2월에 출시한 최신 플래그십 LLM입니다. **7440억 파라미터의 Mixture-of-Experts(MoE) 아키텍처**를 채택하여 추론 시 **400억 파라미터만** 활성화합니다.

- 🏗️ **744B 총 파라미터 / 40B 활성화** — 효율적인 MoE 아키텍처
- 📖 **200K 컨텍스트 윈도우**
- 🔓 **MIT 라이선스** — HuggingFace, ModelScope에서 완전 오픈소스
- 🇨🇳 **Huawei Ascend 칩으로 완전 학습** — NVIDIA 제로 의존
- 🧑‍💻 **SWE-bench 77.8%** — 최첨단에 근접한 코딩 능력
- 🧮 **AIME 2026: 92.7%** — 뛰어난 수학 추론
- 🤖 **에이전트 지원** — GLM-5-Turbo는 도구 호출과 에이전트 워크플로에 최적화

---

## GLM-5 vs GLM-5-Turbo

| 특성 | GLM-5 | GLM-5-Turbo |
|------|-------|-------------|
| **파라미터** | 744B 총 / 40B 활성 | 최적화 버전 (비공개) |
| **컨텍스트** | 200K 토큰 | 200K 입력 / 128K 출력 |
| **라이선스** | MIT (오픈소스) | 비공개 |
| **최적화** | 범용 | 에이전트 및 도구 호출 |
| **추론 속도** | 표준 | ~48 tokens/s |
| **출시일** | 2026년 2월 11일 | 2026년 3월 16일 |

---

## 주요 특징

### 🧑‍💻 코딩 능력
- **SWE-bench Verified: 77.8%** — DeepSeek V3.2와 Kimi K2.5 능가
- GLM-4.7 대비 개발 작업 20%+ 향상

### 🧮 수학 추론
- **AIME 2026: 92.7%** — 경시대회 수준 수학 문제 해결

### 🤖 에이전트 능력 (GLM-5-Turbo)
- **OpenClaw** 에코시스템 최적화
- 도구 호출, 명령 준수, 장기 체인 실행

### 🔒 환각률 56% 감소
- GLM-4.7 대비 대폭 신뢰성 향상

---

## 벤치마크

| 벤치마크 | GLM-5 | GLM-4.7 | DeepSeek V3.2 | Claude Opus 4.5 |
|---------|-------|---------|---------------|-----------------|
| **SWE-bench Verified** | 77.8% | — | ~75% | 80.9% |
| **AIME 2026** | 92.7% | — | — | — |
| **BrowseComp** | 62.0 | — | — | — |
| **AA Intelligence Index** | 50 | 42 | — | — |

---

## ⚡ Atlas Cloud에서 GLM-5 사용하기

[Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)에서 GLM-5를 **OpenAI 호환 API**로 이용할 수 있습니다.

- 🔌 **OpenAI 호환** — 기존 OpenAI SDK 그대로 사용 가능
- 💰 **대안 대비 최대 88% 저렴**
- 🔒 **SOC I & II 인증** | **HIPAA 준수**
- 🌐 **300+ AI 모델** — 하나의 API로 GLM-5, DeepSeek, Qwen 등 이용
- 🆓 **무료 크레딧** 제공, 신용카드 불필요

> 💡 **[Atlas Cloud 가입](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)하고 무료 크레딧으로 GLM-5를 시작하세요!**

---

## API 빠른 시작

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
        {"role": "user", "content": "Python으로 스레드 안전한 LRU 캐시를 구현해주세요."}
    ]
)

print(response.choices[0].message.content)
```

---

## 가격 비교

| 모델 | 입력 (백만 토큰당) | 출력 (백만 토큰당) | 상대 비용 |
|------|-------------------|-------------------|----------|
| **GLM-5-Turbo** | **$1.20** | **$4.00** | **1x** |
| GPT-5.4 | ~$10.00 | ~$30.00 | ~8배 |
| Claude Opus 4.5 | ~$15.00 | ~$75.00 | ~12배 |

---

## 커뮤니티 리소스

- 📄 [GLM-5 기술 보고서](https://arxiv.org/html/2602.15763v1)
- 🤗 [GLM-5 HuggingFace](https://huggingface.co/zai-org/GLM-5)
- 🔧 [GLM-5-Turbo API 문서](https://docs.z.ai/guides/llm/glm-5-turbo)

---

## FAQ

### 1. GLM-5와 GLM-5-Turbo의 차이는?
**GLM-5**는 오픈소스 기반 모델 (MIT 라이선스). **GLM-5-Turbo**는 에이전트에 최적화된 비공개 버전입니다.

### 2. GLM-5를 직접 배포할 수 있나요?
네! HuggingFace에서 가중치가 공개되어 있습니다. 다만 744B 파라미터에는 상당한 GPU 리소스가 필요합니다. 대부분의 사용자에게는 [Atlas Cloud](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5) 사용을 권장합니다.

---

<div align="center">

### [👉 Atlas Cloud에서 GLM-5 사용하기 — 무료 크레딧 👈](https://www.atlascloud.ai?utm_source=github&utm_campaign=awesome-glm-5)

[⬆ 맨 위로](#-awesome-glm-5--zhipu-ai의-오픈소스-moe-대규모-모델)

</div>
