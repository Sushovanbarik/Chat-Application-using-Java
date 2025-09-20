# 💬 Java Chat Application (Socket + Swing)

A **simple client-server chat application** built using **Java Sockets** and **Swing GUI**.  
This project allows a server and a client to connect and exchange messages in real-time through a graphical interface.

---

## 📌 Features

✅ **Client-Server Communication**
- The **server** listens on a fixed port (`2802`) for incoming client connections.
- The **client** connects to the server using IP (`127.0.0.1` by default) and chosen username.

✅ **Username Handling**
- Both client and server provide usernames before starting chat.
- Client username is sent to server for approval (Accept/Reject popup).

✅ **Chat Functionality**
- Real-time **bi-directional messaging**.
- Messages are displayed in a scrollable chat area.
- Each message is prefixed with the sender's username.

✅ **Connection Control**
- Server can **accept/reject client requests**.
- Client and server both handle **graceful shutdown** on quit or disconnection.
- Displays connection status (connected, disconnected, error).

✅ **User-Friendly GUI**
- Built with **Java Swing**:
  - Scrollable chat area
  - Input field + Send button
  - Buttons for Connect/Quit (Client) and Start Server/Quit (Server)

---

## 🛠️ Technologies Used

- **Java Sockets** – TCP connection between client and server  
- **Java Swing** – GUI (JFrame, JTextArea, JTextField, JScrollPane, JOptionPane)  
- **Multithreading** – Separate thread for reading messages (non-blocking UI)  
- **I/O Streams** – `BufferedReader`, `PrintWriter` for message exchange  

---

## 📂 Project Structure

```

ChatApplication/
│
├── Client.java   # Client-side code (connects to server, sends/receives messages)
├── Server.java   # Server-side code (listens for client, handles messages)
└── Readme.md

```

---

## ▶️ How to Run

### 1️⃣ Start the Server
1. Compile the server file:
   ```bash
   javac Server.java
   ```

2. Run the server:

   ```bash
   java Server
   ```
   
3. Enter a username in the GUI and click **Start Server**.

### 2️⃣ Start the Client

1. Compile the client file:

   ```bash
   javac Client.java
   ```

2. Run the client:

   ```bash
   java Client
   ```

3. Enter a username in the GUI and click **Connect**.

4. **Server gets a popup** asking to accept or reject the connection.

   * If accepted → chat begins.
   * If rejected → client will be disconnected.

---

## 🧾 Notes

* Default server port: **2802**
* Default server IP: **127.0.0.1** (localhost)
* Change IP in `Client.java` if connecting to a remote server.

---

## 🏗️ Future Improvements

* Add support for **multiple clients** (broadcast messages).
* Add **file sharing** support.
* Add **encryption** for secure communication.
* Add **sound notifications** for incoming messages.

---

## 👨‍💻 Author

* **Sushovan Barik**
* 📧 [sushovanbarik66@gmail.com](mailto:sushovanbarik66@gmail.com)
* 🌐 [LinkedIn](http://www.linkedin.com/in/sushovan-barik-8b41b6268)

---
