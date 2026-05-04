# 🚀 Email Reply AI – Backend Service

A production-grade Spring Boot backend powering an AI-based email reply system using **Google Gemini API**. This service handles AI generation, secure REST APIs, Docker deployment, and integration with frontend and Chrome Extension.

---

# 🌐 Live API

👉 https://replyai.cfd/api/

---

# ⚙️ Tech Stack

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google%20Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS%20EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![SSL HTTPS](https://img.shields.io/badge/SSL%20HTTPS-00C7B7?style=for-the-badge&logo=letsencrypt&logoColor=white)
![REST API](https://img.shields.io/badge/REST%20API-000000?style=for-the-badge&logo=api&logoColor=white)

---

# 🧠 Features

- AI-powered email reply generation using Gemini  
- REST API architecture  
- Fully containerized backend using Docker  
- AWS EC2 cloud deployment  
- Secure HTTPS communication  
- CORS enabled for frontend + Chrome Extension  
- Production-ready scalable backend system  

---

# 🔗 API Endpoint

### POST `/api/generate`

Request:
```json
{
  "prompt": "Write a professional reply to this email"
}
```
Response:
```json
{
  "reply": "Generated AI response from Gemini"
}
```
This API receives a prompt, sends it to Google Gemini API, processes the AI response, and returns structured JSON output.

---

# 🐳 Docker Setup & Run

Build Docker Image:

```bash
docker build -t email-reply-backend .
```

Run Container:

```bash
docker run -d -p 8080:8080 email-reply-backend
```

---

# ☁️ Deployment Architecture

```text
┌──────────────────────────────────────────────┐
│ Client (Frontend / Chrome Extension)        │
└──────────────────────────────────────────────┘
                     │
                     ▼
┌──────────────────────────────────────────────┐
│ Nginx Reverse Proxy (HTTPS Layer)           │
└──────────────────────────────────────────────┘
                     │
                     ▼
┌──────────────────────────────────────────────┐
│ Spring Boot Backend (Docker Container)      │
└──────────────────────────────────────────────┘
                     │
                     ▼
┌──────────────────────────────────────────────┐
│ Google Gemini API (AI Processing Layer)     │
└──────────────────────────────────────────────┘
                     │
                     ▼
┌──────────────────────────────────────────────┐
│ JSON Response Returned to Client            │
└──────────────────────────────────────────────┘

```

---

# 🚀 Deployment Details (AWS EC2)

- ☁️ **Ubuntu EC2 Instance** → Hosts the Spring Boot backend securely in the cloud  
- 🐳 **Docker Containerization** → Runs the backend as an isolated Spring Boot service  
- 🌐 **Nginx Reverse Proxy** → Handles `/api` routing and manages request forwarding  
- 🔐 **HTTPS Security Layer** → Enabled using Let’s Encrypt SSL certificates  
- 🌍 **Domain Mapping** → Custom domain mapped to EC2 public IP for production access

---

# 🔐 Security

- 🔒 **HTTPS Encryption (SSL/TLS)** → Secures all client-server communication  
- ⚙️ **Stateless REST API** → Ensures scalability and independent request handling  
- 🌍 **CORS Configuration** → Enables safe communication with frontend & Chrome Extension  
- 🛡️ **Nginx Reverse Proxy** → Adds an additional security and routing layer  

---

# 📌 Project Purpose

This backend is part of a full-stack AI SaaS platform designed to:

- 🤖 Generate AI-powered email replies using Google Gemini  
- 🧩 Enable Chrome Extension automation for Gmail  
- 🌐 Integrate with a modern frontend interface  
- ☁️ Support scalable cloud deployment on AWS  

---

# 🔗 Related Repositories

- 💻 **Frontend Repository** → https://github.com/vanshupreti04/email-reply-frontend  
- ⚙️ **Backend Repository** → https://github.com/vanshupreti04/email-reply-backend  
- 🔌 **Chrome Extension Repository** → https://github.com/vanshupreti04/email-reply-extension  
