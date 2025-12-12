AI Voice Sales Agent Demo (N8N + VAPI)
📌 Overview

This repository contains a simplified, safe-to-share version of an AI voice sales agent built with N8N and VAPI.
The agent receives a phone call, collects user requirements, and uses a chat model to recommend website types based on its own reasoning abilities — no external dataset is required.

All internal company systems and data have been completely removed.

🔧 Tech Stack

VAPI — Voice AI agent for handling calls

N8N — Workflow automation and orchestration

Chat Model — Used to analyze user needs and generate website recommendations

🧩 Features

AI receives a phone call from the user

Collects their business requirements

Sends the call data to N8N

N8N passes the information to a chat model

Chat model generates custom website recommendations using its internal knowledge

Sends response back through the workflow

📂 Included Files

workflow.json — Exportable N8N workflow (clean + safe)

screenshots/ — End-to-end workflow + VAPI test call screenshots

README.md — Project explanation

🚀 How to Use

Import the workflow.json into your N8N instance.

Replace the webhook URL with your own N8N webhook endpoint.

Connect the VAPI agent to the webhook.

Update your chat model node with your preferred LLM.

Make a test call → view the AI’s recommendations.

📞 Example Flow
User calls → VAPI agent listens → sends call data to N8N  
→ Chat model evaluates needs → generates recommendations  
→ N8N returns final answer → VAPI speaks it back to the user

⚠️ Disclaimer

This is a public demo version and does not include any internal data, company resources, or external spreadsheets.
All examples are for educational and portfolio purposes only.
