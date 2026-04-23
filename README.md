# 🤖 AI Operations Copilot – ServiceNow + AI Project

## 🚀 Overview
AI Operations Copilot is an intelligent assistant built on ServiceNow that:
- Understands user issues in natural language
- Automatically creates incidents
- Classifies category, priority, and urgency
- Provides AI-driven recommendations
- Maintains chat history
- Displays analytics via a dashboard

This project demonstrates how AI can be integrated into ITSM workflows to improve efficiency and automation.

---

## 🧠 Key Features

### 💬 AI Chat Interface
- ChatGPT-style UI
- Real-time interaction using GlideAjax
- Typing indicator and chat bubbles

### ⚙️ Incident Automation
- Auto-creates incidents from user input
- Maps AI output to:
  - Category
  - Impact
  - Urgency
- Generates Incident Number dynamically

### 🧾 Chat History (Memory)
- Stores conversations in `u_ai_chat_history`
- Supports session-based tracking
- Reloads previous conversations on UI load

### 📊 Dashboard Analytics
- Total AI-generated incidents
- Category distribution (Network, Software, Inquiry)
- Recent activity tracking
- Bar chart visualization
- Date-based filtering
- AI-generated insights (Top issue detection)

---

## 🏗️ Architecture

User → UI Page (Chat UI) → GlideAjax → Script Include  
→ AI Processing → Incident Creation → Response  
→ Stored in Chat History → Dashboard Analytics

---

## 🧩 Components

### 1️⃣ UI Pages
- `ai_copilot` → Chat interface
- `ai_copilot_dashboard` → Analytics dashboard

### 2️⃣ Script Includes

#### AICopilotAjax
Handles:
- User input
- AI processing
- Incident creation
- Chat history storage

#### AICopilotDashboard
Handles:
- Aggregation of data
- Category counts
- Chart data
- AI summary generation

---

## 🗃️ Custom Table

### `u_ai_chat_history`

| Field       | Description |
|------------|------------|
| message     | User input |
| response    | AI response (JSON) |
| session_id  | Chat session |
| incident    | Linked incident |
| role        | User/AI |

---

## 🔧 Technologies Used

- ServiceNow (UI Pages, GlideAjax, Script Includes)
- JavaScript
- GlideRecord
- Chart.js (for visualization)
- REST (optional AI integration)

---

## 🤖 AI Integration

Two modes supported:

### 1. Mock AI (No Cost)
- Rule-based response simulation
- Works offline
- Used for demo and development

### 2. Real AI (Optional)
- OpenAI API integration
- Requires API key and billing
- Handles real NLP understanding

---

## 📊 Dashboard Features

- 📈 Bar chart for incident distribution
- 📅 Date filter (dynamic query)
- 🔍 Recent activity tracking
- 🤖 AI-generated insights

---

## 🧪 Sample Use Cases

| Input | Output |
|------|--------|
| Internet not working | Network Incident |
| Password reset | Inquiry |
| Application crash | Software Incident |

---

## 📌 Challenges Solved

- XML/Jelly UI Page errors
- GlideAjax response parsing
- JSON cleanup from AI responses
- Date filtering issues
- Incident linking and navigation

---

## 🎯 Business Value

- Reduces manual ticket creation
- Improves classification accuracy
- Enables proactive monitoring
- Enhances user experience
- Demonstrates AI-driven ITSM

---

## 🚀 Future Enhancements

- Real-time AI (OpenAI / LLM integration)
- Predictive incident analysis
- SLA breach prediction
- ServiceNow Now Assist integration
- Mobile UI / Service Portal version

---

## 👤 Author

**Srikanth Madabhushi**  
Portfolio: https://srikanthmadabhushi.github.io  

---

## ⭐ If you like this project
Give it a star ⭐ and connect with me on LinkedIn!
