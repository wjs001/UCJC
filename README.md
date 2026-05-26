Improving Judicial Faithfulness in Uyghur–Chinese Machine Translation via Multi-Granularity Supervision and Verifiable Rewards


> 🧾 **UCJC** provides multi-granularity judicial translation supervision.  
> 🧠 **THE-RLVR** optimizes legal faithfulness with verifiable rewards.  
> 🔍 **JFS** evaluates whether critical judicial facts are faithfully preserved.

---

## 🌟 Overview

Uyghur--Chinese judicial machine translation is a low-resource and high-stakes translation scenario.  
A fluent translation may still be legally unreliable if it changes judicial terminology, party roles, claims, judgment results, dates, amounts, or event relations.

This repository provides the anonymized implementation for:

**Improving Judicial Faithfulness in Uyghur--Chinese Machine Translation via Multi-Granularity Supervision and Verifiable Rewards**

We introduce:

| Component | Description |
|---|---|
| 🧾 **UCJC** | A multi-granularity Uyghur--Chinese judicial MT resource |
| 🧠 **THE-RLVR** | A verifiable reward-based reinforcement learning framework |
| 🔍 **JFS** | A diagnostic metric for judicial factual faithfulness |

---

## 🧩 Framework

```text
🧾 UCJC Corpus Construction
        ↓
🛠️ Supervised Fine-Tuning
        ↓
🧠 THE-RLVR Optimization
        ↓
⚖️ Faithful Uyghur--Chinese Judicial MT
