# 🚀 Talksy-Django-AI-Chat 🤖  
### _AI Chatbot with Collapsible History — Powered by Django & Google Gemini ✨_

---

<p align="center">
  <img src="https://img.shields.io/badge/Built%20with-Django-0C4B33?style=for-the-badge&logo=django&logoColor=white"/>
  <img src="https://img.shields.io/badge/Powered%20by-Google%20Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white"/>
  <img src="https://img.shields.io/badge/UI-Bootstrap%205-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
</p>

---

## 🧠 Project Overview

**Talksy** is a modern, responsive **AI chatbot application** built to demonstrate **full-stack AI integration**.  
It features a sleek **dark theme UI**, robust backend logic, and seamless **session-based conversation history**.

---

## 🌟 Key Technical Highlights

| Category | Description |
|-----------|-------------|
| **Framework** | 🐍 Django (Python) – secure, scalable backend using MVC architecture |
| **Intelligence** | 🤖 Google Gemini API (`google-genai` SDK) for conversational power |
| **Interface** | 🎨 Bootstrap 5 for responsive components and custom dark theme |

---

## ⚙️ Core Features

We focused on combining **functionality** with a **polished user experience**:

- 🛡️ **Secure Secrets** — API keys managed via `.env` and `python-dotenv` (never exposed in code).  
- 💾 **Persistent History** — Uses **Django Sessions** to store conversations (no login required).  
- 📱 **Dynamic UI**
  - **Collapsible Sidebar** — Sliding sidebar to manage history, auto-hides for full view.  
  - **Auto-Expand Input** — Textarea grows with message length, no horizontal scroll.  
  - **Clean Messages** — Custom Bootstrap bubbles auto-resize using `w-auto`.  
- ⚡ **Async Flow** — AJAX-based message exchange for fast, non-blocking chat.

---

## 🚀 Quick Start — Setup & Installation

### 1️⃣ Prerequisites
- 🐍 Python 3.8 +
- 🔑 Google Gemini / Studio API Key

---

### 2️⃣ Clone and Setup Environment

```bash
# Clone the repository
git clone https://github.com/your-username/Talksy-Django-AI-Chat.git
cd Talksy-Django-AI-Chat

# Create & activate a virtual environment
python -m venv venv
source venv/bin/activate    # macOS / Linux
# .\venv\Scripts\activate    # Windows (PowerShell)

# Install dependencies
pip install django google-genai python-dotenv
```
## 3️⃣ Configure Secrets (.env file) 🔒

To keep your API keys secure and out of the codebase, create a .env file in your project’s root directory (next to manage.py):
```bash
# .env
GEMINI_API_KEY="YOUR_ACTUAL_GOOGLE_STUDIO_API_KEY_HERE"
```
Make sure to load this file in your Django settings:
```python
# chatapp/settings.py
from dotenv import load_dotenv
import os

load_dotenv()
GEMINI_API_KEY = os.getenv("GEMINI_API_KEY")
```
## 4️⃣ Database Setup

Apply migrations for conversation history:
```bash
python manage.py makemigrations chat
python manage.py migrate
```
## 5️⃣ Run the Application
```bash
python manage.py runserver
```
Then open your browser at 👉 http://127.0.0.1:8000/

## 🗂️ Project File Guide (Brief Overview)

| File / Folder                   | Purpose                                                                    |
| ------------------------------- | -------------------------------------------------------------------------- |
| `manage.py`                     | Command-line utility to run and manage your Django app.                    |
| `chatapp/settings.py`           | Contains project settings like database, middleware, and Gemini key setup. |
| `chatapp/urls.py`               | Routes URLs to corresponding app views.                                    |
| `chat/views.py`                 | Main logic — handles AI API requests and chat responses.                   |
| `chat/templates/chat/chat.html` | Main UI for chatbot.                                                       |
| `chat/static/chat/`             | Holds CSS, JS, and images.                                                 |
| `.env`                          | Stores your API key securely.                                              |
| `requirements.txt`              | Lists required Python libraries.                                           |

## 📜 License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for full details.

---

## 👨‍💻 Author

**Project by:** [Ankit Kumar](https://github.com/CodewithAnkitt)  

⭐ If you like this project, give it a **star** on GitHub! ⭐


