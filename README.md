# 🏠 AI-Powered Real Estate Dashboard

**[🌐 Live Dashboard](https://sona93303.preview.softr.app/?autoUser=true&show-toolbar=true) | [🎥 Video Demo](https://www.loom.com/share/36e9b83e3a004a40be72f37fadc70779)**

---

## 🖼️ Demo & Workflow Visualization

| n8n Automation (Backend) | Softr Investor Dashboard (Frontend) |
| :---: | :---: |
| <img src="https://github.com/Muneeb20019/Real-Estate-Dashboard-n8n-Softr/raw/main/real%20estate%20.png" width="400" /> | <img src="https://github.com/Muneeb20019/Real-Estate-Dashboard-n8n-Softr/raw/main/Softr%20n8n%20Dashboard.png" width="400" /> |

*Left: The n8n orchestration pipeline. Right: The real-time color-coded dashboard.*

---

## 🚀 Project Overview
An enterprise-grade automation engine designed for Airbnb investors to eliminate manual property screening. This tool ingests raw property listing data via **Gmail triggers**, utilizes **LLMs** to perform financial feasibility analysis, and instantly publishes "Buy" or "Pass" verdicts to a live, color-coded dashboard.

## 🎯 The Problem & The AI Solution
### The Problem
Airbnb investors waste hours reading messy listing descriptions. Identifying key "deal breakers"—like high renovation costs or HOA rental restrictions—requires intense manual focus and is prone to human error.

### The Solution
This system acts as a **24/7 Virtual Analyst**:
- **Automated Ingestion:** Captures data via Gmail triggers scanning for property alerts.
- **Financial Intelligence:** Calculates total investment (`Price + Reno Estimate`) against a $400k ceiling.
- **Regulatory Check:** Scans text for legal keywords to ensure Short-Term Rental (Airbnb) compliance.
- **Real-Time UI:** Streams analyzed data into a Softr-powered Deal Board for immediate viewing.

## ✨ Key Features
- **🧠 Advanced AI Logic:** Uses **OpenRouter (DeepSeek/GPT-4o)** with a **Structured Output Parser** to coerce raw text into valid JSON.
- **⚖️ Automated Verdict Logic:** 
    - **🟢 BUY:** Total cost < $400k AND Airbnb is legal.
    - **🔴 PASS:** Over budget OR rental restrictions found.
    - **🟡 HUMAN REVIEW:** Triggered for missing price data or ambiguous text.
- **✉️ Gmail Integration:** Scans incoming property alerts automatically to identify deals before they hit the mainstream.
- **📊 Relational Storage:** Utilizes **Airtable** as a centralized database for deal tracking and persistence.
- **📱 Responsive Frontend:** A public **Softr** dashboard with color-coded cards and search/filter functionality.

## 🚀 Technical Stack
| Layer | Technology |
| :--- | :--- |
| **Automation** | n8n Orchestration |
| **AI Brain** | OpenRouter (DeepSeek-V3 / GPT-4o-mini) |
| **Frontend** | Softr |
| **Database** | Airtable |
| **Language** | JavaScript (for n8n Logic) |
| **Triggers** | Gmail IMAP |

---

## 🛠️ How to Use & Setup

### 1. Database Setup (Airtable)
Create a new Airtable Base named `Real Estate Deal Engine` and a table named `Deals`. Define the following columns with precise data types:
*   `Property Title`: `Single line text`
*   `Asking Price`: `Currency`
*   `Renovation Estimate`: `Currency`
*   `Is Airbnb Legal?`: `Checkbox`
*   `AI Verdict`: `Single Select` (Options: `🟢 BUY`, `🔴 PASS`, `🟡 HUMAN REVIEW`)
*   `AI Summary`: `Long text`
*   `Listing Text`: `Long text`

### 2. Automation Setup (n8n)
1.  **Import Workflow:** Download the `workflow.json` from this repo and import it into your n8n instance.
2.  **Configure Credentials:**
    *   Connect your **OpenRouter/OpenAI** API key in the AI Agent node.
    *   Connect your **Airtable Personal Access Token** in the Airtable node.
    *   Authenticate your **Gmail** account in the Gmail Trigger node.
3.  **Activate:** Flip the toggle in the top-right corner to **Active**. The system is now live.

### 3. Trigger the Analysis
- **Via Gmail:** Simply send an email containing a property listing or description to your connected Gmail account. n8n will detect the new email and begin processing instantly.

### 4. Monitor the Dashboard
1.  Open your **Softr Live Dashboard**.
2.  The AI will process the listing in < 30 seconds.
3.  New deals will appear automatically at the top of the board with their respective **AI Verdict** tags and financial summaries.

---

## ✍️ Author
**Muneeb Ali Khan**

- **GitHub:** [@Muneeb20019](https://github.com/Muneeb20019)
- **LinkedIn:** [Muneeb Ali Khan](https://www.linkedin.com/in/muneeb-ali-khan-2a1675365)
- **Project Link:** [Airbnb Deal Board](https://sona93303.preview.softr.app/?autoUser=true&show-toolbar=true)

