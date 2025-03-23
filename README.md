# Chatbot Consultant - Microservices Architecture

## Overview
This project is a chatbot consultant that works with both **Telegram** and **Instagram**, built using a **microservices architecture** with **Express.js**. The services communicate via **REST APIs**, and the system is containerized using **Docker**.

## Features
- **Multi-platform support:** Works with both Telegram and Instagram.
- **Microservices architecture:** Each feature runs as an independent service.
- **MongoDB Atlas:** Cloud-based database storage.
- **Docker-based deployment:** Easily deployable with Docker and Docker Compose.

---

## Project Structure
```
tgchat-bot-microservices/
│── api-gateway/                # Handles API requests and routes them to the appropriate services
│── services/
│   ├── telegram-bot/           # Telegram bot microservice
│   ├── instagram-bot/          # Instagram bot microservice
│   ├── dialog-service/         # Handles message processing and AI responses
│   ├── database-service/       # Connects to MongoDB and manages stored data
│── docker-compose.yml          # Docker Compose configuration
│── README.md                   # Project documentation
```

---

## Setup & Installation
### Prerequisites
- **Node.js** (v22.8.0 recommended)
- **Docker & Docker Compose**
- **MongoDB Atlas account**

### 1. Clone the repository
```sh
git clone https://github.com/Muxitdin/tgchat-bot-microservices
cd tgchat-bot-microservices
```

### 2. Setup environment variables
Create `.env` files inside each microservice directory:
#### Example: `services/telegram-bot/.env`
```
TELEGRAM_BOT_TOKEN=your-telegram-bot-token
```
#### Example: `services/database-service/.env`
```
MONGO_URI=mongodb+srv://your-username:your-password@your-cluster.mongodb.net/
```