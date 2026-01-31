***Lead Generation AI Agent (n8n + OpenAI + Google Sheets)***

<img width="1910" height="744" alt="Lead-generation-AI-Agent" src="https://github.com/user-attachments/assets/7fab2e77-c4fd-435a-ac0f-bc70ef7aa3be" />

Workflow overview in n8n

Successful lead capture logs

Google Sheets integration results
<img width="1024" height="370" alt="unnamed (12)" src="https://github.com/user-attachments/assets/535936a1-dd32-4846-a0ad-c03d8c569fe6" />




Problem
Sales teams waste countless hours manually qualifying leads, searching for enrichment data, and updating spreadsheets or CRMs. This slows down response times, creates bottlenecks, and leaves gaps in the sales pipeline.

Solution
This AI-powered Lead Generation Agent automates the entire process of capturing, enriching, and storing leads using n8n, OpenAI, and Google Sheets.

Instead of manual entry, conversational AI extracts lead details, enriches them with external data, and stores them in a CRM-ready format.

🔄 Workflow Steps
Chat Trigger → Captures incoming user messages as potential leads.

AI Agent (OpenAI) → Extracts and structures lead details (name, email, company, intent).

HTTP Request Node → Performs live enrichment (e.g., company/domain lookup).

Code Node → Cleans and formats the extracted lead data.

Google Sheets Integration → Appends each qualified lead into a sheet for sales follow-up.

✨ Features
Conversational lead intake via chat

AI-powered entity extraction (name, email, company, intent)

External data enrichment (via HTTP API calls)

Automatic storage in Google Sheets (CRM-ready)

Extendable to HubSpot, Airtable, or Salesforce

🛠️ Tech Stack
n8n → workflow automation

OpenAI → natural language understanding

Google Sheets → lead database

HTTP APIs → data enrichment

(Optional) Simple Memory → keeps short context across conversations

▶️ How to Run (Demo)
Import workflow.json into n8n (export is sanitized; set your own credentials).

Create the required credentials in n8n (WhatsApp/Telegram/OpenAI/etc.).

Create a Google Sheet / Notion DB / Airtable base as needed.

Update node IDs/URLs in the workflow to match your resources.

Trigger the entry node (Cron/Webhook/Gmail) with sample data from /sample-data.


⚠️ Notes on Credentials & Safety
This repo does not include secrets. Configure credentials inside n8n.

Replace any test tokens/IDs with your own before running.

Keep sensitive data out of version control.
