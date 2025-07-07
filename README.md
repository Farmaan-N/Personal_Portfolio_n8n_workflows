# Personal Portfolio Feedback & Chatbot Automation (n8n + Render)

This project consists of two workflow automations built using n8n and deployed for free on Render.com.
Both workflows are designed to enhance interaction on a personal portfolio website — by collecting visitor feedback and offering a chatbot for project info and FAQs.

### 🚀 Stack & Methodology
Tool / Service	Purpose
n8n (Render.com)	Open-source workflow automation platform
OpenRouter API	To access DeepSeek Chat (a free AI model)
LangChain AI Agent (n8n LangChain Node)	To generate AI-powered responses based on form/chat inputs
Gmail OAuth2 (n8n)	To send personalized thank-you emails
n8n Form Trigger	To capture form submissions
n8n Chat Trigger	To receive messages via webhook

### AI Methodology:
I integrated OpenRouter’s free DeepSeek LLM model through n8n’s LangChain nodes for AI-powered message generation and reply formatting, without relying on paid services like OpenAI.

#### 📄 Workflow 1: Personal_Portfolio_Forms
📑 Purpose: Collects visitor feedback on a personal portfolio via a hosted form

📝 Process:

User submits feedback via n8n Form Trigger

Data is sent to a LangChain AI Agent powered by DeepSeek Chat via OpenRouter

AI generates a personalized thank-you message based on form inputs

n8n sends an automated email to the visitor using Gmail OAuth2

🎨 Use case: Real-time, personalized engagement with portfolio visitors

#### 💬 Workflow 2: Personal_Portfolio_Chatbot
📑 Purpose: A chatbot accessible via a public webhook that answers visitor queries

📝 Process:

Message received via Chat Trigger (webhook)

Forwarded to a LangChain AI Agent using DeepSeek Chat (OpenRouter)

AI crafts a custom reply based on your predefined system message (can include skills, projects, experience)

Response sent back via webhook reply

🎨 Use case: 24/7 automated chatbot assistant for your personal portfolio

📦 Deployment
Both workflows are deployed free on Render.com, making them publicly accessible via secure HTTPS URLs, without needing ngrok, Cloudflare Tunnel, or external webhook hosting.

### 📑 Required Credentials
Credential	Purpose	Where to Get
OpenRouter API Key	Connect to DeepSeek AI models via OpenRouter	openrouter.ai
Gmail OAuth2 Credentials	Send emails from your Gmail account via n8n	Google Cloud Console

### 📌 Summary
🚀 Hosted fully on Render.com (free)

📬 Personalized feedback form & auto-email system

🤖 AI-powered chatbot via OpenRouter’s DeepSeek Chat

🎛️ Built using n8n’s no-code automation platform
