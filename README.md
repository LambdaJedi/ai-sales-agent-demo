# **AI Voice Sales Agent Demo (N8N + VAPI)**

## **📌 Overview**  
This repository contains a simplified, safe-to-share version of an **AI-powered voice sales agent**, built using **N8N** and **VAPI**.  
The agent receives a phone call, collects user requirements, and uses a **chat model** to recommend the best type of website based on its own reasoning.  

This demo does **not** use any internal datasets or company-specific infrastructure.  
All sensitive information has been removed.

---

## **🔧 Tech Stack**
- **VAPI** — Voice AI agent for phone calls  
- **N8N** — Workflow automation engine  
- **Groq Llama 3.3 70B** — High-speed LLM for reasoning  
- **Conversation memory** — To maintain short-term context  

---

## **🧩 Features**
- Handles voice calls through VAPI  
- Extracts the user's business needs  
- Sends user input to N8N through a webhook  
- LLM evaluates requirements and recommends website solutions  
- Sends structured JSON back to VAPI (which turns it to audio)  
- Clean, simple end-to-end pipeline  

---

## **📂 Included Files**
- `workflow.json` — Sanitized N8N workflow (no credentials)  
- `/screenshots` — Workflow and VAPI preview screenshots  
- `README.md` — Documentation for setup and usage  

---

## **🚀 How the Workflow Works**

### **1. VAPI → Webhook**  
The voice agent receives a call and sends input to an N8N webhook.

### **2. AI Agent Node**  
The workflow uses a LangChain Agent with a custom prompt to:
- interpret the user’s request  
- extract key website requirements  
- generate a short, spoken-friendly recommendation  

### **3. Groq LLM**  
Powered by `llama-3.3-70b-versatile`, providing:
- fast reasoning  
- accurate website suggestions  
- conversational phrasing  

### **4. Memory Node**  
Maintains short-term conversation history to improve responses.

### **5. Return Node**  
Sends structured JSON back to VAPI so the AI can speak the results.

---

## **📞 End-to-End Flow**  
```text
User call → VAPI agent → N8N Webhook → AI Agent → Groq LLM  
→ Generate Recommendation → Return JSON → VAPI speaks back

---

flowchart LR
    A[VAPI Voice Call] --> B[Webhook Input]
    B --> C[AI Agent Node]
    C --> D[Groq LLM Reasoning]
    C --> E[Conversation Memory]
    D --> F[Return Response to VAPI]

---

## **⚙️ How to Use**

Import workflow.json into N8N

Add your own Groq API key in N8N credentials

Replace webhook URL in VAPI with your own

Make a call to the agent

N8N responds with the LLM-generated website recommendation

---

## ⚠️ Disclaimer
This is a **public demo** and does **not** use any internal company systems, spreadsheets, or sensitive data.  
It exists purely for educational and portfolio purposes.

