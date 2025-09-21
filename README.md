# 💬 Real-Time Chat Application

A real-time chat application built with **Spring Boot**, **Thymeleaf**, and **WebSocket**. This project demonstrates how to build a live, multi-user chat system using STOMP over WebSockets and a simple front-end rendered with Thymeleaf.

---

## 🚀 Features

- Real-time bi-directional messaging using **WebSocket + STOMP**
- Multiple users can join and chat in real time
- Live message broadcast without page refresh
- Simple and responsive UI with **Thymeleaf**
- Message timestamping and sender identification
- No database required (in-memory message handling)

---

## 📦 Tech Stack

| Layer         | Technology       |
|---------------|------------------|
| Backend       | Spring Boot      |
| WebSockets    | Spring WebSocket + STOMP |
| View Engine   | Thymeleaf        |
| Frontend      | HTML, CSS, JavaScript |
| Build Tool    | Maven |

---

## 📁 Project Structure

src/
├── main/
│ ├── java/
│ │ └── com.example.chat/
│ │ ├── controller/
│ │ ├── config/
│ │ ├── model/
│ │ └── ChatApplication.java
│ └── resources/
│ ├── static/
│ │ └── js/
│ ├── templates/
│ │ └── chat.html
│ └── application.properties

yaml
Copy code

---

## 🛠️ Setup Instructions

### 1. **Clone the Repository**
```bash
git clone https://github.com/your-username/springboot-realtime-chat.git
cd springboot-realtime-chat
2. Build the Project
Using Maven:
bash
Copy code
./mvnw clean install
Using Gradle:
bash
Copy code
./gradlew build
3. Run the Application
bash
Copy code
./mvnw spring-boot:run
# or
java -jar target/chat-application.jar
4. Open in Browser
Navigate to:

bash
Copy code
http://localhost:8080/chat
Open multiple browser tabs or devices to test real-time messaging.

🧠 How It Works
Users load the chat page (/chat)

JavaScript connects to WebSocket using SockJS and Stomp.js

Messages are sent to /app/chat.sendMessage and broadcast to /topic/public

All subscribed clients receive the new message instantly

🔐 Security (Optional Enhancements)
Authentication for users (e.g., with Spring Security)

Chat room separation

Persistent chat history (via database)

Private messaging
