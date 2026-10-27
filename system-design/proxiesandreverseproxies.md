the proxy basically acts as an intermediary between a client and a server 

the proxy can receive your request and then contact the destination server for you 

forward proxy primarily represents the client 
reverse proxy primarily represents the server 

suppose a university wants to apply rules to some outbound web traffic 

instead of allowing every browser to contact external websites directly,
it can use forward proxy that checks whether the required detination is allowed

whereas a reverse proxy acts on the behalf of the server 

The reverse proxy receives requests and forwards them to an appropriate backend instance.

The browser doesn't need to know which backend actually processed the request.

there will be two tcp connections from a browser to reverse proxy and then reverce proxy to server 

use of reverse proxy is in:
when there is heavy traffic and you have multiple backend servers running but you dont want the users/browsser to konw that so you introduce an intermediate 

the proxy takes the request and sends it to the appropriate sever also known as LOAD BALANCING 

## TLS termination 

##caching response : a reverse proxy can store a cacheable response temporarily and reuse it for subsequent requests 


forward proxies and reverse proxies can exist can exist in the same communication flow 