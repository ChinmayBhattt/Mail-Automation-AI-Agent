# AI Chat Automation with n8n (Google Gemini + Gmail Agent)

This repository contains an **n8n AI Agent workflow** that listens for incoming chat messages, uses the **Google Gemini Chat Model**, stores short-term **conversation memory**, and can automatically **send emails via Gmail**.  
Use this workflow to build intelligent chat → email automation.

---

## 📁 Files in This Repo
- **My workflow.json** – full exported n8n workflow  
  *(You uploaded it: `/mnt/data/My workflow.json`)*

---

## 🧠 Workflow Overview

### **Nodes Used**
- **When chat message received** – chat trigger node  
- **AI Agent** – orchestrates LLM, tools & memory  
- **Google Gemini Chat Model** – LLM used for reasoning  
- **Simple Memory** – buffer-based memory for chat history  
- **Send a message in Gmail** – sends email through Gmail OAuth2

---

## ⚙️ Requirements
- n8n (self-hosted or cloud)
- Google Gemini API key (PaLM/Gemini credentials)
- Gmail OAuth2 credentials
- Basic JSON import knowledge in n8n

---

## 🚀 How to Import in n8n

1. Open n8n  
2. Go to **Workflows → Import from File**  
3. Upload: **My workflow.json**  
4. Click **Save**

---

## 🔑 Required Credentials Setup

### **Google Gemini (PaLM) API**
- Create API credential in n8n  
- Attach it to the “Google Gemini Chat Model” node

### **Gmail OAuth2**
- Create Gmail OAuth2 credential  
- Connect it to the “Send a message in Gmail” node

---

## 🔄 Workflow Logic (Step-by-Step)

1. **Chat Trigger fires** → receives message  
2. Message goes into the **AI Agent**  
3. AI Agent uses:
   - Google Gemini model for reasoning  
   - Simple Memory to store history  
   - Gmail Tool if email needs to be sent  
4. AI agent generates a reply or sends an email automatically  

---

## 🧪 Testing

1. Activate the workflow (toggle **Active**)  
2. Send a chat message to the configured trigger  
3. Monitor **Executions** in n8n  
4. Check Gmail to confirm email actions  

---

## 📌 Notes
- JSON contains node IDs, positions, and credential references  
- You must manually re-select your own credentials after importing  

---

## 📜 License
Free to use, modify, and extend for personal or production automation.

