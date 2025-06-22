# **SocialeX – Project Documentation**  
**A Real-Time MERN Stack Social Media Web Application**  

## **1. Introduction**  
**SocialeX** is a full-stack social media platform built using the **MERN stack** (MongoDB, Express.js, React, Node.js). It includes features like user authentication, post creation, 24-hour stories, real-time interactions (using **Socket.io**), and media uploads (via **Firebase Storage**).  

### **Key Features**  
✅ **User Authentication** (JWT-based login/register)  
✅ **Create & View Posts** (Text & Images)  
✅ **24-Hour Expiring Stories** (Similar to Instagram)  
✅ **Real-Time Notifications & Chat** (Socket.io)  
✅ **Responsive UI** (React + Bootstrap)  
✅ **Secure Backend** (Node.js + Express + MongoDB)  

---

## **2. Technologies Used**  

| **Layer**       | **Technologies**                          |
|----------------|-----------------------------------------|
| **Frontend**   | React.js, CSS, Bootstrap, Axios         |
| **Backend**    | Node.js, Express.js, JWT, Bcrypt        |
| **Database**   | MongoDB (via Mongoose ODM)              |
| **Media Storage** | Firebase Storage                      |
| **Real-Time**  | Socket.io                               |
| **Deployment** | GitHub (Code), Firebase/Drive (Demo)    |

---

## **3. Project Structure**  

### **GitHub Repository Layout**  
```
SocialeX/  
├── client/               # React Frontend  
│   ├── public/           # Static files  
│   ├── src/              # React components, hooks, context  
│   │   ├── components/   # Reusable UI components  
│   │   ├── context/      # Auth & Socket context  
│   │   ├── pages/        # Main views (Home, Profile, etc.)  
│   │   └── App.js        # Main App Router  
│   └── package.json      # Frontend dependencies  
│  
├── server/               # Node.js Backend  
│   ├── controllers/      # Logic for routes  
│   ├── models/           # MongoDB Schemas  
│   ├── routes/           # API endpoints  
│   ├── middleware/       # Auth middleware  
│   ├── utils/            # Helper functions  
│   └── server.js         # Express server setup  
│  
├── docs/                 # Documentation  
│   └── API.md            # API Endpoint Reference  
│  
├── screenshots/          # App Screenshots  
├── README.md             # Project Setup Guide  
└── .gitignore            # Excluded files (env, node_modules)  
```

---

## **4. Setup & Installation**  

### **Prerequisites**  
- Node.js (v16+)  
- MongoDB Atlas (or local DB)  
- Firebase Project (for storage)  

### **Steps to Run Locally**  
1. **Clone the Repository**  
   ```bash
   git clone https://github.com/HariN999/SocialeX.git
   cd SocialeX
   ```

2. **Install Dependencies**  
   ```bash
   cd client && npm install
   cd ../server && npm install
   ```

3. **Configure Environment Variables**  
   - **Backend (`.env` in `/server`)**  
     ```env
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret_key
     FIREBASE_API_KEY=your_firebase_config
     ```
   - **Frontend (`.env` in `/client`)**  
     ```env
     REACT_APP_API_URL=http://localhost:5000
     REACT_APP_FIREBASE_CONFIG=your_firebase_config
     ```

4. **Run the Application**  
   - **Start Backend**  
     ```bash
     cd server && npm start
     ```
   - **Start Frontend**  
     ```bash
     cd client && npm start
     ```
   - Access at: `http://localhost:3000`  

---

## **5. API Documentation**  
See **[API.md](https://github.com/HariN999/SocialeX/blob/main/docs/API.md)** for detailed endpoints:  

| **Endpoint**            | **Method** | **Description**                |
|------------------------|----------|-------------------------------|
| `/api/auth/register`   | POST     | Register a new user           |
| `/api/auth/login`      | POST     | Login user (returns JWT)      |
| `/api/posts`           | GET      | Fetch all posts               |
| `/api/posts`           | POST     | Create a new post             |
| `/api/stories`         | POST     | Upload a story (24h expiry)   |
| `/api/chat`            | GET      | Fetch messages (Socket.io)    |

---

## **6. Screenshots & Demo**  
📸 Screenshots: View in /screenshots
🎥 Demo Video: Watch on Drive (Link in README.md) 

---

## **7. Security Measures**  
- **JWT Authentication** (Secure token-based sessions)  
- **Bcrypt Password Hashing** (No plaintext passwords)  
- **Firebase Rules** (Restricted media access)  
- **`.env` Protection** (Sensitive keys excluded via `.gitignore`)  

---

## **8. Future Enhancements**  
🔹 **Comments & Reactions** on posts  
🔹 **Direct Messaging** (1-on-1 chats)  
🔹 **Deploy on Vercel/Heroku**  

---

## **9. Conclusion**  
SocialeX successfully implements core social media features with a **secure MERN stack architecture**. The project is **ready for mentor review** and further scaling.  

📌 **GitHub Repo:** [https://github.com/HariN999/SocialeX](https://github.com/HariN999/SocialeX)  
📩 **Contact:** [narlakantihariharan@gmail.com]  

