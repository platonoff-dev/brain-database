#Web #Protocols #ClientServer 
[[HTTP Methods]]
WebSockets is advanced technology that provides ability two-directional connection between devices. It designed to work over HTTP and it is compatible with HTTP. To achieve compability protocol uses upgrade header to switch over protocols. 

To open connection client must send HTTP message with upgrade header.

```
GET /chat HTTP/1.1 
Host: server.example.com 
Upgrade: websocket 
Connection: Upgrade 
Sec-WebSocket-Key: x3JJHMbDL1EzLkh9GBhXDw== 
Sec-WebSocket-Protocol: chat, superchat 
Sec-WebSocket-Version: 13 
Origin: http://example.com
```

And server must return the handshake response. 
```
HTTP/1.1 101 Switching Protocols 
Upgrade: websocket 
Connection: Upgrade 
Sec-WebSocket-Accept: HSmrc0sMlYUkAGmm5OPpG2HaGWk= 
Sec-WebSocket-Protocol: chat
```