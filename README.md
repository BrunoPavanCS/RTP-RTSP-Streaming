# RTP Video Streaming  

## Overview  
This project consists of a **Server** and a **Client** for streaming video over **RTP (Real-time Transport Protocol)**.  

## How to Run  

### Start the Server  
To start the server, run the following command:  
```bash
python Server.py <server_port>
```
- **server_port**: Choose a port number greater than **1024**.  

#### Example:  
```bash
python Server.py 5555
```

### Start the Client  
To start the client, run:  
```bash
python ClientLauncher.py <server_host> <server_port> <RTP_port> <video_file>
```
- **server_host**: The address of the server (e.g., `localhost` or an IP address).  
- **server_port**: The same port used to start the server.  
- **RTP_port**: The port to receive RTP packets.  
- **video_file**: Use the provided video file (`movie.Mjpeg`).  

#### Example:  
```bash
python ClientLauncher.py 127.0.0.1 5555 6000 movie.Mjpeg
```

## Notes  
- Ensure that both the server and client are running on the same network.  
- The client should use the **same server port** specified when launching the server.  
- The video file must be available in the directory where the client is executed.  
