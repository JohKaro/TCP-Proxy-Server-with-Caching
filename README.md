# TCP Proxy Server with Caching 🌐

##  Overview
This project implements a functional **TCP Proxy Server** that acts as an intermediary between a client and a destination server. The primary goal is to demonstrate network communication principles, socket programming, and data flow optimization through a caching layer.

##  Key Technical Features
* **Socket Programming:** Low-level TCP socket implementation for reliable data transfer.
* **Caching Mechanism:** Implements a local cache to store frequently requested data, reducing redundant server requests and improving response times (Cache Hit/Miss logic).
* **Protocol Analysis:** Handles packet packing and unpacking (Struct Packing) to ensure data integrity across the network.
* **Error Handling:** Robust management of connection timeouts and server-side errors.

##  Architecture & Flow
The system follows a classic three-tier architecture:
1. **Client:** Initiates requests to the proxy.
2. **Proxy Server:** Checks the local cache. If data exists (Cache Hit), it returns it immediately. If not (Cache Miss), it fetches data from the server, updates the cache, and forwards it to the client.
3. **Destination Server:** Processes requests forwarded by the proxy.

##  How to Run
1. Start the Destination Server:
   ```bash
   python Server.py
