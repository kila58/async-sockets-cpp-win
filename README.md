# Asynchronous Sockets for Windows
Simple, multithread-based(not thread safe), non-blocking asynchronous Client-Server classes in C++ for TCP & UDP. 
Creates a thread for every connection. Use `mutex`es or `atomic` variables to provide thread-safe functions.

```cpp
// Initialize a tcp socket.
TCPSocket tcpSocket;

// Connect to the host.
tcpSocket.Connect("127.0.0.1", 8888, [&] {
    cout << "Connected to the server successfully." << endl;

    // Send String:
    tcpSocket.Send("Hello Server!");
});
```
Super Easy!

**CPU & RAM Usages (with single tcp connection & with single udp server + client):**
![Lightweight](https://github.com/eminfedar/async-sockets-cpp/raw/master/img/emptyRamUsages.png)

Lightweight!

## Examples:
![Examples](https://github.com/eminfedar/async-sockets-cpp/raw/master/img/programs.png)
You can compile all the examples by just going in the `examples/` directory and run `make` in terminal:
- [examples/tcp-client.cpp](https://github.com/eminfedar/async-sockets-cpp/blob/master/examples/tcp-client.cpp)
- [examples/tcp-server.cpp](https://github.com/eminfedar/async-sockets-cpp/blob/master/examples/tcp-server.cpp)
- [examples/udp-client.cpp](https://github.com/eminfedar/async-sockets-cpp/blob/master/examples/udp-client.cpp)
- [examples/udp-server.cpp](https://github.com/eminfedar/async-sockets-cpp/blob/master/examples/udp-server.cpp)
  
## Supported Platforms:
- Windows
