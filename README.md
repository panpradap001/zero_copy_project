# File Transfer with Normal Copy and Zero Copy

## Overview
This project demonstrates a simple client-server file transfer application using Java Sockets. It supports two modes of file transfer:
1. **Normal Copy**: Transfers data using traditional byte stream methods.
2. **Zero Copy**: Uses `transferTo` and `transferFrom` for efficient file transfer, reducing CPU usage and improving performance.

## Features
- Transfer files from the server to the client.
- Select between normal copy and zero copy modes.
- Measure and display transfer time for performance comparison.

## Technology Stack
- **Language**: Java
- **Networking**: Java Sockets
- **File I/O**: File Streams, NIO Channels

## Installation and Usage

### 1. Compile the code
```bash
javac Server.java Client.java
```

### 2. Run the server
```bash
java Server
```
The server will listen on port **5000** and wait for client connections.

### 3. Run the client
```bash
java Client
```
The client will connect to the server and receive the file.

## Configuration
- Modify the **mode** variable in `Server.java` and `Client.java` to switch between modes:
  - `"1"` → Normal Copy
  - `"0"` → Zero Copy
- Change the file names (`test.deb`, `test_downloaded.deb`) as needed.

## Performance Comparison
The execution time for each method is displayed in milliseconds after the file transfer is completed. Zero copy is generally faster for large files due to reduced memory copies and CPU overhead.

## License
This project is open-source and can be modified or distributed freely.

