# 📨 Messenger - A Simple Chat App Using Socket Programming

Messenger is a basic command-line chat application built using **Python socket programming**. It enables multiple clients to connect to a server and exchange messages in real-time — just like a group chat!

## 🚀 Features

- Multi-client support via threading
- Real-time message broadcast to all connected users
- Simple communication protocol using TCP
- Command-line interface
- Username-based message identification

## ⚙️ How It Works

### 🔌 Socket Programming Basics

- **Sockets** allow two computers to communicate.
- This app uses the **TCP (SOCK_STREAM)** protocol for reliable connection.
- The server listens on a fixed IP & port. Clients connect to it using those details.
- Each client sends messages to the server, which then broadcasts them to all connected clients.

### 🧠 Flow:

#### Server
1. Creates a socket and binds it to a host and port.
2. Listens for incoming connections.
3. When a client connects, the server accepts it and starts a thread to handle messages from that client.
4. Broadcasts received messages to all connected clients.

#### Client
1. Connects to the server using the host and port.
2. Sends a username to register.
3. Starts two threads:
   - One for sending messages.
   - One for receiving and displaying incoming messages.

---
