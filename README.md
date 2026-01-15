# 🏠 AI-Powered Real Estate Deal Engine (Airbnb Sniper)

**[🌐 Live Dashboard](https://sona93303.softr.app) | [🎥 Video Demo](https://www.loom.com/share/36e9b83e3a004a40be72f37fadc70779)**

## 🖼️ Demo

* ([![AI Real Estate Engine](https://cdn.loom.com/sessions/thumbnails/36e9b83e3a004a40be72f37fadc70779-with-play.gif)](https://www.loom.com/share/36e9b83e3a004a40be72f37fadc70779))
[
](https://www.loom.com/share/36e9b83e3a004a40be72f37fadc70779)---

## 🎯 Project Overview
An enterprise-grade automation engine designed for Airbnb investors to eliminate manual property screening. This tool ingests raw property listing data via **Gmail triggers** or **Webhooks**, utilizes **LLMs** to perform financial feasibility analysis, and instantly publishes verdicts to a live dashboard.

## 📸 System Architecture (Under the Hood)
![n8n Workflow Graph](REPLACE_WITH_YOUR_N8N_SCREENSHOT_LINK)

## ✨ Key Features
- **🧠 Intelligence Engine:** Powered by **DeepSeek-V3 via OpenRouter** with a **Structured Output Parser** for 100% valid JSON extraction.
- **⚖️ Automated Verdict Logic:** 
    - **🟢 BUY:** Total cost < $400k AND Airbnb is legal.
    - **🔴 PASS:** Over budget OR rental restrictions found.
- **✉️ Gmail Automation:** Scans incoming property alerts automatically to identify deals before they hit the mainstream.
- **📊 Relational Storage:** Utilizes **Airtable** for centralized database tracking and persistence.

## 🚀 Technical Stack
| Layer | Technology |
| :--- | :--- |
| **Automation** | n8n Orchestration |
| **AI / LLM** | OpenRouter (DeepSeek-V3 / GPT-4o-mini) |
| **Frontend** | Softr |
| **Database** | Airtable |

## ⚙️ Advanced Implementation Details
I implemented a **Structured Output Parser** node in n8n. Unlike standard AI prompts that return conversational text, this implementation forces the LLM to adhere to a strict JSON schema, ensuring data integrity for the Airtable database.

## ✍️ Author
**Muneeb Ali Khan**

- **GitHub:** [@Muneeb20019](https://github.com/Muneeb20019)
- **LinkedIn:** [Muneeb Ali Khan](https://www.linkedin.com/in/muneeb-ali-khan-2a1675365)

---
*Built for the AI & Automation Engineering Internship Challenge.*




* (https://www.loom.com/share/941af541355f459a8f19f6c3e4cda597?sid=1307c447-a23c-45d0-88b9-dba260b51072)
