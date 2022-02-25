# Simple WebsocketServer
This is a very simple Websocket server class. 
You can us it like a TcpListener and client.
## Usage
```bash
  WebSocketServer server = new WebSocketServer(IPAddress.Parse("192.168.1.69"), 8080);//Use your own local ip (ipv4)
  server.Start();
  WebSocketClient client = server.AcceptWebsocketClient();
```

```bash
    client.Write("Hello");

    client.Read();//The program stop if there is no data to receive.
```
## Installation

 - Copy the Websocket.cs file in the same folder as the main program. Then call the library (using Websockets)in the main program.
 - Host the .html website in the same network as the server. For more help (https://www.youtube.com/results?search_query=visual+studio+code+html+hosting)

## Features
 - It can be multithreaded
 - It is easy to use
 - It uses Utf-8 codec
 - It uses [RFC 6455] protoclo 

## Limitations 
 - It can send max 65 535 bytes of data 
 - It can recieve 100 000 bytes
 - The receiving can be slow

## Sources
 - https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API/Writing_WebSocket_server
 - https://datatracker.ietf.org/doc/html/rfc6455
