# HTTP Client and Server in C

**httpclient.c:** a simple HTTP client  
*USAGE: ./httpclient \<hostname> \<port> \<request path>*

**httpserver.c:**  simple blocking HTTP server (TCP only)  
*USAGE: ./httpserver \<port>*

**httpserver_fork.c:** a simple non-blocking HTTP server (TCP only)  
*USAGE: ./httpserver_fork \<port>*

**multi_service_server.c:** a non-blocking server that uses TCP to serve HTTP requests and UDP to serve ping requests  
*USAGE: ./multi_service_server \<tcp port> \<udp port>*  
The format of the UDP ping request is a 32 bit random integer followed by up to 64 bytes of information.
The ping response will send back the 32 random integer in the request + 1 followed by the same 64 bytes of information.

HOW 2 RUN THIS (IT WORKS ) 
*server
sudo ./+x/httpserver 99

*client = 
 sudo ./+x/httpclient 127.0.0.1 99 ./

*result
HTTP/1.0 200 OK


*not ./ = 
 127.0.0.1 99 /
HTTP/1.0 404 Not Found
