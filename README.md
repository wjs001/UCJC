**Improving Judicial Faithfulness in Uyghur–Chinese Machine Translation via Multi-Granularity Supervision and Verifiable Rewards**


## 🌟 Overview

Uyghur--Chinese judicial machine translation is a low-resource and high-stakes translation scenario.  
A fluent translation may still be legally unreliable if it changes judicial terminology, party roles, claims, judgment results, dates, amounts, or event relations.

This repository highlights the following contributions:
| Component | Description |
|---|---|
| 🧾 **UCJC** | A multi-granularity Uyghur--Chinese judicial MT resource |
| 🧠 **THE-RLVR** | A verifiable reward-based reinforcement learning framework |
| 🔍 **JFS** | A diagnostic metric for judicial factual faithfulness |

---

## 📦 Data Sources

UCJC is constructed from publicly available corpora and judicial text resources.  
The data is processed through cleaning, normalization, language filtering, judicial relevance filtering, sentence segmentation, duplicate removal, privacy filtering, and anonymization.

| Resource | Link | Usage |
|---|---|---|
| 🌐 **CC-100** | [data.statmt.org/cc-100](https://data.statmt.org/cc-100/) | Uyghur sentences selected for judicial relevance |
| 🌍 **MC2** | [Hugging Face: pkupie/mc2_corpus](https://huggingface.co/datasets/pkupie/mc2_corpus) | General-domain Uyghur sentences for improving language coverage |
| ⚖️ **China Judgments Online** | Public judicial document resource | Judicial documents and sentence-level legal text samples |
| 🏷️ **Extracted judicial terminology** | Constructed from the processed judicial corpus | Standardized Uyghur--Chinese legal term constraints |

All released data has undergone privacy anonymization and is intended solely for research on low-resource judicial machine translation.
## 🛠️ Tools and Frameworks

This repository builds on the following public tools and frameworks:

| Tool / Framework | Link | Usage |
|---|---|---|
| 🦙 **LLaMA-Factory** | [GitHub: hiyouga/LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) | Supervised fine-tuning |
| 🚀 **Verl** | [GitHub: verl-project/verl](https://github.com/verl-project/verl) | Reinforcement learning with GRPO |
| 📏 **BLEU** | Standard MT metric | Surface-level machine translation evaluation |
| 📊 **COMET / COMETKiwi** | COMET-style MT evaluation resources | Neural semantic translation evaluation |
| ⚙️ **Custom reward scripts** | Included in this repository | Terminology consistency, hallucination penalty, and event-graph reward computation |

## 🤖 Models Used

We evaluate both external general models and trained backbone models.  
The links below point to the public model pages or official project pages used for reference.

| Model | Link | Usage |
|---|---|---|
| 🧠 **Qwen3-8B** | [Hugging Face: Qwen/Qwen3-8B](https://huggingface.co/Qwen/Qwen3-8B) | Backbone model for SFT and THE-RLVR |
| 🧠 **Qwen3.6-27B** | [Qwen Blog: Qwen3.6-27B](https://qwen.ai/blog?id=qwen3.6-27b) | Backbone model for SFT and THE-RLVR |
| 🧠 **Qwen3.5-4B** | [Qwen Blog: Qwen3.5](https://qwen.ai/blog?id=qwen3.5) | External comparison model |
| 🌐 **Gemini-3.1-Flash-Lite** | [Google Blog: Gemini 3.1 Flash-Lite](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-1-flash-lite/) | External comparison model |
| 🧩 **GLM-4-32B-0414** | [GitHub: zai-org/GLM-4](https://github.com/zai-org/GLM-4) | External comparison model |
| 🔍 **DeepSeek-V4-Flash** | [SiliconFlow: DeepSeek-V4-Flash](https://www.siliconflow.com/models/deepseek-v4-flash) | Fixed reward extractor for judicial facts and event graphs |
