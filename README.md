# AI Voice Sales Agent Demo (N8N + VAPI)

## 📌 Overview
This repository contains a simplified, safe-to-share version of an **AI voice sales agent** built using **N8N** and **VAPI**.  
The agent receives a phone call, gathers user requirements, and uses a **chat model** to recommend website types based on its own reasoning — **no external dataset is required**.

All internal company data and systems have been removed.

---

## 🔧 Tech Stack
- **VAPI** — Voice AI call handling  
- **N8N** — Workflow automation  
- **Chat Model** — Reasoning + website recommendations  

---

## 🧩 Features
- Accepts voice calls through VAPI  
- Collects business requirements  
- Sends structured data to N8N  
- Chat model generates recommendations from general knowledge  
- Sends the final answer back through VAPI  

---

## 📂 Included Files
- `workflow.json` — Exportable N8N workflow (safe version)  
- `screenshots/` — Workflow screenshots + VAPI test call  
- `README.md` — Documentation  

---

## 🚀 How to Use
1. Import the `workflow.json` into N8N  
2. Update the webhook URL with your own  
3. Connect the VAPI agent to the webhook endpoint  
4. Configure the chat model node (your own LLM)  
5. Make a test call and observe recommendations  

---

## 📞 Example Flow
User calls → VAPI agent listens → sends call data to N8N
→ Chat model evaluates → produces recommendations
→ N8N returns answer → VAPI speaks it back to the user

---

## ⚠️ Disclaimer
This is a **public demo** and does **not** use any internal company systems, spreadsheets, or sensitive data.  
It exists purely for educational and portfolio purposes.

