# GPT-Teaching-Assistant

## Overview
This is a **GPT-powered chat application** designed to help users understand **Data Structures & Algorithms (DSA) problems** on LeetCode. Users can submit a **LeetCode problem URL** along with their **doubt**, and the chatbot provides **guidance and hints** to help them solve the problem without revealing direct solutions.

## Features
✅ **Chat-based UI** for submitting doubts on LeetCode problems  
✅ **GPT-powered responses** with hints and explanations  
✅ **No direct answers** – only guidance for better learning  
✅ **FastAPI backend** to handle GPT interactions  
✅ **React + TailwindCSS frontend** for a smooth UI experience  
✅ **CORS support** for seamless frontend-backend communication  

---

## 📌 Setup Instructions

### **1️⃣ Backend (FastAPI + OpenAI GPT)**
#### **Prerequisites:**
- Python 3.8+
- OpenAI API key

#### **Installation Steps:**
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-repo.git
   cd your-repo
   ```
2. **Create a virtual environment and activate it**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
4. **Set up OpenAI API Key**
   - Create a `.env` file in the root directory and add:
     ```
     OPENAI_API_KEY=your-api-key
     ```
   - OR set it in your terminal:
     ```bash
     export OPENAI_API_KEY="your-api-key"
     ```
5. **Run the FastAPI backend**
   ```bash
   uvicorn main:app --reload
   ```

### **2️⃣ Frontend (React + TailwindCSS)**
#### **Prerequisites:**
- Node.js 16+

#### **Installation Steps:**
1. **Navigate to the frontend directory**
   ```bash
   cd frontend
   ```
2. **Install dependencies**
   ```bash
   npm install
   ```
3. **Run the frontend**
   ```bash
   npm run dev
   ```
4. Open **http://localhost:3000** in your browser

---

## 📌 Application Architecture

The project follows a **client-server architecture**, where:
- **Frontend (React + TailwindCSS)** sends user inputs to the backend.
- **Backend (FastAPI + OpenAI GPT)** processes user queries and generates helpful hints.
- **OpenAI GPT API** provides intelligent responses without revealing direct solutions.

### **System Flow:**
1. User enters a **LeetCode URL** and **their doubt**.
2. React frontend sends the request to FastAPI backend.
3. FastAPI formats a **structured prompt** and sends it to OpenAI’s GPT API.
4. GPT returns a **hint-based response**.
5. The frontend **displays the response** in a chat interface.

---

## 📌 Using the Application
1. **Enter a LeetCode problem URL**
2. **Ask a question about the problem**
3. **Receive helpful hints** instead of direct solutions
4. **Refine your approach based on the guidance**

---

## 📌 GPT Integration Explained

This project uses **OpenAI's GPT model** to assist users in solving DSA problems. The bot does NOT provide direct solutions but instead:
- **Asks guiding questions** to help users think critically.
- **Suggests related problems** for a better understanding.
- **Explains constraints and edge cases** to refine problem-solving skills.

### **Prompt Engineering Approach:**
We craft structured prompts for GPT, such as:
```
A student is struggling with a problem on LeetCode: {LeetCode URL}.
They asked: {User's Question}.
Provide hints and guidance without giving the full solution.
Encourage them to think about problem constraints, edge cases, and similar examples.
```
This ensures that GPT acts as a **teaching assistant** rather than a direct answer provider.

---

## 🚀 Future Enhancements
- **User Authentication** to save previous chats
- **Support for multiple GPT models**
- **Advanced hint-generation algorithms**
- **Improved UI with markdown support for better explanations**

---

## 📌 Contributions
Feel free to contribute! Submit a pull request or report issues.

---

## 📌 License
This project is **open-source** and free to use.


