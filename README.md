# 🌐 **Multi-Threaded File Server** 🚀

This project is part of my university course on **Distributed Systems**. The goal of this project was to implement a **multi-threaded file server** capable of handling **multiple client requests** simultaneously. The server and clients communicate using **shared memory**, **semaphores**, and **pthreads**, ensuring efficient file access and parallel processing.

## 📝 **Project Overview**

The **Multi-Threaded File Server** is designed to handle multiple clients requesting specific lines from text files stored on the server. Each client makes multiple requests, and the server processes these requests concurrently using threads. The communication between the clients and the server is facilitated using:

- **Shared memory** for data exchange.
- **Semaphores** to synchronize the process and ensure data consistency.
- **Pthreads** to handle multiple client requests in parallel.

### 🖥️ **How It Works**
1. The **server** creates multiple threads, each handling a specific client request.
2. The **client** sends a request to the server for specific lines from a file stored in a directory.
3. The **server** reads the requested lines and sends them back to the client via shared memory.
4. The client and server communicate through semaphores, ensuring synchronization and proper handling of concurrent requests.

---

## 🧑‍💻 **How to Run**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/multi-threaded-file-server.git
   cd multi-threaded-file-server
2. **Compile the Code**:

The project comes with a Makefile, so simply run:
  ```bash
  make
  ```
3. **Run the Server**:

To start the server, use the following command:

  ```bash
  ./fileServer <num_clients> <num_requests> <lambda>
  ```
---

## ⚙️ **Features**

- **Multi-threading**: The server uses threads to process multiple client requests concurrently.
- **Semaphore Synchronization**: Ensures correct timing and data access.
- **Shared Memory**: Efficient communication between clients and the server.
- **Configurable Parameters**: Set the number of clients, requests, and file parameters through command-line arguments.

---

## 📄 **File Structure**

- `fileServer`: The main program for the server-side logic.
- `headFile.h`: Contains headers and shared structures used for communication.
- `my_functions.cpp`: Implements the server and client logic.
- `Makefile`: Automates the compilation process.
- `lines.txt`: Stores the results of each client's read operation.
- `stats.txt`: Contains performance statistics and time delays for each client.

---

## 🔧 **Technologies Used**

- **C++**: The programming language used for implementation.
- **Pthreads**: For handling parallelism and multi-threading.
- **Shared Memory**: For efficient data sharing between processes.
- **Semaphores**: For process synchronization and control.
- **Makefile**: For easy project compilation and management.

---

## 📈 **Project Purpose**

This project was developed to demonstrate concepts of parallelism, concurrent processing, and inter-process communication in a distributed environment. By simulating multiple clients making simultaneous requests to a file server, this project showcases how to handle synchronization, load distribution, and performance analysis.

---

## 🛠️ **Installation & Requirements**

- Linux (Ubuntu or similar distribution recommended)
- G++ (for compiling C++ code)
- Make (for building the project)
- POSIX Semaphores and Shared Memory (Linux-based IPC)

Make sure to have the required libraries and tools installed:
```bash
sudo apt update
sudo apt install build-essential
