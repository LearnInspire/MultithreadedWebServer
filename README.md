# Multithreaded Web Server in Java

This project demonstrates different implementations of a web server and client in Java, showcasing single-threaded, multithreaded, and thread pool-based approaches. Each implementation is organized into separate directories for clarity.

## Project Structure
MultithreadedWebServer/ ├── Multithreaded/ │ ├── Client.java │ └── Server.java ├── SingleThreaded/ │ ├── Client.java │ └── Server.java ├── ThreadPool/ │ └── Server.java

### Implementations

1. **SingleThreaded**
   - A single-threaded server that handles one client at a time.
   - Client and server communicate using sockets.
   - Files:
     - `SingleThreaded/Server.java`: Implements the single-threaded server.
     - `SingleThreaded/Client.java`: Implements the client for the single-threaded server.

2. **Multithreaded**
   - A multithreaded server that creates a new thread for each client connection.
   - Files:
     - `Multithreaded/Server.java`: Implements the multithreaded server using threads.
     - `Multithreaded/Client.java`: Implements the client for the multithreaded server.

3. **ThreadPool**
   - A server that uses a thread pool to handle client connections efficiently.
   - Files:
     - `ThreadPool/Server.java`: Implements the server using a fixed thread pool.

## How to Run

### Prerequisites
- Java Development Kit (JDK) installed on your system.
- A terminal or IDE like Visual Studio Code to compile and run the code.

### Steps

1. **Compile the Code**
   Navigate to the directory containing the `.java` files and compile them using the `javac` command:
   ```sh
   javac *.java

2. Run the Server Start the server by running the main method in the desired server implementation:
   ```sh
   java Server

4. Run the Client Start the client by running the main method in the corresponding client implementation:
   ```sh
   java Client

Example
To test the multithreaded implementation:

1. Navigate to the Multithreaded directory.
2. Start the server:
   ```sh
   java Server

3. In a separate terminal, start the client:
   ```sh
   java Client

- Features
  - SingleThreaded Server: Handles one client at a time, blocking other connections until the one is completed.
  - Multithreaded Server: Spawns a new thread for each client, allowing concurrent handling of multiple clients.
  - ThreadPool Server: Uses a fixed thread pool to manage client connections efficiently, reducing the overhead of thread creation.
- Configuration
  - Port: The server listens on port 8010 by default. You can modify the port in the main method of the server files.
  - Thread Pool Size: The thread pool size in the ThreadPool/Server.java file is set to 10 by default. You can adjust it as needed.
- Notes
  - The SingleThreaded implementation is suitable for simple use cases but is not scalable for handling multiple clients.
  - The Multithreaded implementation improves scalability but may lead to high resource usage with many clients.
  - The ThreadPool implementation balances scalability and resource efficiency by reusing threads.
