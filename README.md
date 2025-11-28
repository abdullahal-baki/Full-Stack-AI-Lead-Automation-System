# 🚀 Full-Stack AI Lead Automation System
### End-to-End Sales Outreach • AI Agents • Auto Meeting Booking • Instantly + Calendly + RAG

This project is a fully automated **AI Lead Automation System** built for a client company, designed to streamline and automate outbound sales workflows from start to finish.  
It takes bulk leads → enriches them → generates personalized emails → handles replies with an AI agent → and automatically books meetings via Calendly.

This system functions like a complete **AI SDR (Sales Development Representative)** capable of operating 24/7 with zero manual involvement.

---

## 🏢 Client / Company
This project was developed as a full production system for:

**➡️ _[RAY ADVERTISING]_**  

---

## 👥 Developers

| Name | Role |
|------|------|
| **MD Abdullah Al Baki** | System Architecture, Backend, AI Agent Pipeline, Integrations, Frontend Supervision |
| **Monirul Islam Akash** | Frontend Developer / Backend Support / UI Integration |

---

# ⭐ Features

## ✅ 1. Bulk Lead Import + Campaign Management
- Create, edit and manage campaigns  
- Import thousands of leads (CSV)  
- Automatic syncing with **Instantly.ai**  
- Real-time campaign status + analytics  

## ✅ 2. Lead Enrichment 
- Website data extraction  
- LinkedIn scraping (Bright Data)
- Industry + company + role intelligence  
- Clean structured dataset for personalization and RAG  

## ✅ 3. AI-Powered Email Outreach (OpenAI + LangChain)
Generates:
- Personalized cold outreach  
- Follow-up sequences  
- Dynamic email templates  
- Uses Instantly.ai to send real emails  

## ✅ 4. Autonomous AI Reply Agent (RAG + Tools + LangGraph)
The reply agent can:
- Read incoming emails  
- Understand intent  
- Extract information using RAG  
- Respond professionally  
- Handle objections  
- Push prospects toward booking  
- Store memory in Pinecone Vector DB  

## ✅ 5. Automatic Meeting Booking (Calendly API)
- Checks availability  
- Sends booking links  
- Auto-schedules meetings  
- Syncs event details  

## ✅ 6. Modern Next.js Frontend (SaaS UI)
- **Dashboard** – KPIs, stats & quick controls  
- **Leads Page** – full CRM-like table  
- **Campaigns Page** – build complete email campaigns  
- **Prompts Page** – manage system & agent prompts  
- **Agent Playground** – test reply agent in real-time  
- **API Config** – manage all integrations from UI  

## ✅ 7. Secure Backend Architecture
- Python + Flask  
- SQLAlchemy ORM  
- Alembic migrations  
- JWT Authentication  
- Modular service-based design  
- Async workers for background tasks  

## ✅ 8. Production Deployment (AWS)
- EC2 backend hosting  
- RDS PostgreSQL  
- Static asset hosting  
- Nginx reverse proxy  
- Fully Dockerized  

---

# 🧠 System Architecture
Bulk Leads → Enrichment → AI Email Generator → Instantly.ai Sending
→ Incoming Replies → RAG Reply Agent → Calendly Auto-Booking
→ Dashboard + Analytics


Frontend (Next.js)
↓
Backend API (Flask, SQLAlchemy, JWT)
↓
AI Layer (LangChain, LangGraph, Pinecone, OpenAI)
↓
3rd-Party Integrations (Instantly.ai, Calendly, Bright Data)
↓
Database (PostgreSQL)


---

# 🛠 Tech Stack

### **Frontend**
- Next.js  
- TailwindCSS  
- React Query  
- JWT Auth  

### **Backend**
- Python  
- Flask  
- SQLAlchemy  
- Alembic  
- Pydantic  
- Uvicorn  

### **AI / Agents**
- OpenAI Models  
- LangChain  
- LangGraph  
- LangSmith  
- Pinecone Vector DB  
- Custom RAG pipeline  
- Custom agent tools  

### **Integrations**
- Instantly.ai (Email Automation)  
- Calendly (Meeting Booking)  
- Bright Data (Scraping)  

### **Infrastructure**
- AWS EC2  
- AWS RDS  
- Docker  
- Nginx  

---

# 📁 Project Structure ( Backend )

```bash
email-automation-ai/
|-- alembic/
|   |-- versions/
|   |   |-- 5690db239152_msg.py
|   |   |-- b59efe3b9c1f_msg.py
|   |   `-- cca5e655cb4c_init.py
|   |-- env.py
|   |-- README
|   `-- script.py.mako
|-- logs/
|   |-- leads/
|       |-- a383fe57-ff43-4052-8b35-1f3a75729ecc.log
|       `-- aeb5c0fb-442e-444b-9e28-b05585df71a3.log
|   |-- campaigns/
|       `-- cb0992b2-a123-4715-824e-cc350b42855a.log
|-- src/
|   |-- ai/
|   |   |-- edges/
|   |   |   |-- __init__.py
|   |   |   `-- edges.py
|   |   |-- embeddings/
|   |   |   |-- __init__.py
|   |   |   `-- embeddings.py
|   |   |-- graph/
|   |   |   |-- __init__.py
|   |   |   `-- reply_agent_graph.py
|   |   |-- LLMs/
|   |   |   |-- __init__.py
|   |   |   `-- openai_llm.py
|   |   |-- nodes/
|   |   |   |-- __init__.py
|   |   |   |-- response_nodes.py
|   |   |   `-- route_nodes.py
|   |   |-- prompts/
|   |   |   |-- __init__.py
|   |   |   |-- agent_prompts.py
|   |   |   |-- instruction.docx
|   |   |   |-- reply_instruction.docx
|   |   |   `-- user_prompts.py
|   |   |-- state/
|   |   |   |-- __init__.py
|   |   |   `-- states.py
|   |   |-- tools/
|   |   |   |-- __init__.py
|   |   |   |-- calendly_tools.py
|   |   |   `-- vector_retrievers.py
|   |   |-- __init__.py
|   |   |-- content_generator_agent.py
|   |   `-- reply_agent.py
|   |-- config/
|   |   |-- __init__.py
|   |   `-- configer.py
|   |-- database/
|   |   |-- models/
|   |   |   |-- __init__.py
|   |   |   |-- campaigns.py
|   |   |   |-- credentials.py
|   |   |   |-- leads.py
|   |   |   |-- notificatoins.py
|   |   |   |-- prompts.py
|   |   |   `-- users.py
|   |   |-- services/
|   |   |   |-- __init__.py
|   |   |   |-- campaign_services.py
|   |   |   |-- credential_services.py
|   |   |   |-- lead_services.py
|   |   |   |-- notification_services.py
|   |   |   |-- prompt_services.py
|   |   |   `-- user_services.py
|   |   |-- __init__.py
|   |   |-- base.py
|   |   |-- calendly_events_data.pkl
|   |   |-- database.db
|   |   |-- email_agent_memory.db
|   |   `-- session.py
|   |-- docs/
|   |   |-- front-end.txt
|   |   |-- leads_dummy.csv
|   |   |-- main-program-setup.txt
|   |   |-- project-structure.txt
|   |   `-- server-setup.txt
|   |-- email/
|   |   |-- __init__.py
|   |   |-- accounts_manager.py
|   |   |-- campaign_manager.py
|   |   |-- emails_manager.py
|   |   `-- lead_manager.py
|   |-- scrapers/
|   |   |-- __init__.py
|   |   |-- linkedin_scraper.py
|   |   `-- website_scraper.py
|   |-- site/
|   |   |-- routers/
|   |   |   |-- __init__.py
|   |   |   |-- api_key.py
|   |   |   |-- auth.py
|   |   |   |-- campaign.py
|   |   |   |-- lead.py
|   |   |   |-- prompt.py
|   |   |   `-- webhook.py
|   |   |-- __init__.py
|   |   `-- socket.py
|   |-- utils/
|   |   |-- __init__.py
|   |   `-- logger.py
|   `-- __init__.py
|-- tests/
|   `-- __init__.py
|-- .env
|-- .gitignore
|-- alembic.ini
|-- app.py
|-- main.py
|-- pyproject.toml
|-- README.md
|-- requirements.txt
|-- setup.cfg
`-- wsgi.py

```

---

# 🚀 How It Works (Flow)

1. User creates a campaign  
2. Uploads bulk leads  
3. System enriches using Bright Data  
4. AI generates personalized outreach  
5. Instantly.ai sends emails + follow-ups  
6. AI Reply Agent handles responses automatically  
7. If prospect is warm → Calendly auto-books meeting  
8. Dashboard updates with real-time metrics  

---

# 📊 Screenshots (Add your images)


---

# 🧪 Monitoring (LangSmith)

The system includes full observability:
- Agent traces  
- Prompt debugging  
- Error tracking  
- RAG performance visualization  

---

# 🏁 Final Result

A complete, autonomous **AI Sales Machine** capable of:
- Handling thousands of leads  
- Sending personalized outreach  
- Replying automatically  
- Booking meetings  
- And fully managing sales pipelines  

Designed to operate like a **24/7 AI SDR Team**.

---

# 📬 Contact / Credits

If you want to extend or customize this system:  
**Developer:** _Md Abdullah Al Baki_  
**Email:** _abdullahalbaki009@gmail.com_  
**Company Delivered For:** _Ray Advertising_  

---





