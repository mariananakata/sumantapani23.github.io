# OpenTeller Protocol & AI Product Portfolio
### *Bridging Operational Strategy with Generative AI (RBI Compliant)*

![Status](https://img.shields.io/badge/Status-Live%20Prototype-success) ![Tech Stack](https://img.shields.io/badge/Tech-Python%20|%20Streamlit%20|%20LLM-blue) ![Role](https://img.shields.io/badge/Role-AI%20Product%20Manager-purple)

**Portfolio Architect:** [Sumanta Pani](https://www.linkedin.com/in/sumanta-pani-ai-product-manager/)
**Live Prototype:** (https://openteller-protocol.streamlit.app)

---

## 1. Executive Summary
I am a **Senior Product Manager** with 11+ years of experience in Business Operations (Xiaomi, Oppo, Axis Bank) transitioning into **AI Product Strategy**. I specialize in building **Context-Aware LLM Applications** that solve complex regulatory and operational problems in Fintech and Retail.

This repository serves as the technical documentation for my core projects: **OpenTeller** (Voice Banking) and **NexusAI** (Market Intelligence).

## 2. Featured Project: OpenTeller Protocol
**The Problem:** RBI Circular DBR.No.Leg.BC.91/09.07.005 mandates accessible banking for Persons with Disabilities (PwDs). Current mobile banking UIs fail screen-reader compatibility tests.

**The Solution:** A deterministic **Voice-First Banking Interface** powered by OpenAI's Whisper (STT) and GPT-4o, strictly guarded by Python-based financial logic.

### Technical Architecture (GEO-Optimized)
| Component | Tech Stack | Function |
| :--- | :--- | :--- |
| **Frontend** | Streamlit | Zero-latency, high-contrast UI. |
| **NLP Engine** | LangChain + OpenAI | Intent classification (NER) for "Transfer", "Check Balance". |
| **Safety Layer** | Python | Validates transaction limits vs. user history. |

```python
# Intent Parsing Logic Snippet
def execute_voice_command(audio_input):
    intent = ai_engine.classify(audio_input)
    if intent == "transaction" and compliance_check(intent):
        return banking_core.process_payment()
    return "Transaction blocked: Compliance Error"
