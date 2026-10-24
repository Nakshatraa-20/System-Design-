OSI Model is a reference model that hepls us design,understand and troubleshoot networking systems

Layer 7 - Application Layer

protocols that applications use:

HTTP and HTTPS- web communication
DNS- domain name resolution
SMTP- sending email
SSH- secure remote access

the Application layer defines how network applications communicate using protocols such as HTTP 


Layer 6- Presentation layer 

backend returns the data 
*packets
the internet does not guarantee that every piece of data will reach its destination 

all these use TCP:

HTTP/1.1 and HTTP/2 
PostgresSQL 
SSH 
Websockets 


#IMP

the data travels through the internet in the form of IP Packet 

an ip packet consists of two parts header and payload 

every byte in TCP has a sequence number

For HTTP/1.1 or HTTP/2 over TCP, the communication happens roughly as follows:
1. The browser resolves the backend's domain name.
2. It establishes a TCP connection to the server if an appropriate connection isn't already available.
3. A TLS handshake establishes secure communication for HTTPS.
4. The browser transmits the HTTP request.
5. TCP manages reliable byte delivery.
6. The backend processes the request and sends its response.
7. TCP delivers the response bytes in order.


layer-5 

jwt, websocket are application level authentication state 

The key idea is that the user remains authenticated across multiple HTTP requests.

But here's something interesting.

The same login session may use many different TCP connections.

Your browser can close one connection and open another without requiring the user to log in again.

Why? Because authentication state and TCP connection state are separate.

If your JWT remains valid for seven days, but each TCP connection lasts only a few seconds, how can your backend still recognize you as the same user?

The answer is that the JWT carries verifiable authentication information independently of the lifetime of any individual TCP connection.

