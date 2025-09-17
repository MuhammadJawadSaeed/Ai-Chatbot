# 🤖 AI Chatbot (React + Node.js + Socket.io + Google Gemini)

This project is a **real-time AI-powered chatbot** built with:
- **Frontend:** React + Socket.io-client  
- **Backend:** Node.js + Express + Socket.io  
- **AI Integration:** Google Gemini API (via `@google/genai`)  

The chatbot allows users to send messages from the frontend, communicates with the backend over WebSockets, and returns **AI-generated responses** in real-time.

---

##  Features
- Real-time chat using **Socket.io**
- AI-powered responses with **Google Gemini API**
- Clean and responsive **chat UI**
- Auto-scroll for new messages
- User & bot message distinction
- Easy setup for local development

---

##  Tech Stack
- **Frontend:** React, Vite, Socket.io-client, CSS  
- **Backend:** Node.js, Express, Socket.io  
- **AI Service:** Google Gemini API (`@google/genai`)  
- **Testing:** Postman (for backend API/socket testing)  



---

##  Setup Instructions

### 1️⃣ Clone Repository
```bash
git clone https://github.com/MuhammadJawadSaeed/ai-chatbot.git
cd ai-chatbot
```

### 2️⃣ Setup Backend
```bash
cd backend
npm install
```

Create a `.env` file in `backend/` and add:
```env
GEMINI_API_KEY=your_gemini_api_key_here
```

Run backend:
```bash
node server.js
```
> Backend runs at: **http://localhost:3000**

---

### 3️⃣ Setup Frontend
```bash
cd frontend
npm install
npm run dev
```
> Frontend runs at: **http://localhost:5173**

---

##  Testing with Postman
You can also test your backend with **Postman**:
1. Open Postman and connect to `http://localhost:3000`
2. Use the **Socket.io Postman extension** or hit REST endpoints if you add them.  
3. Send test events like `ai-message` to verify AI responses without running the frontend.

This is useful for debugging your backend before integrating with React.

---

##  How It Works
1. User enters a message in React frontend.  
2. Message is sent via **Socket.io** to backend server.  
3. Backend sends the conversation history to **Google Gemini API**.  
4. Gemini returns an AI-generated response.  
5. Backend emits response back to frontend.  
6. Chat UI displays bot’s reply in real-time.  

---

##  Future Improvements
- Save chat history in **MongoDB**
- Add **authentication** for users
- Support **multiple chat rooms**
- Add **voice-to-text** & **text-to-speech**

---

##  Contributing
Pull requests are welcome! For major changes, open an issue first to discuss what you’d like to change.  

