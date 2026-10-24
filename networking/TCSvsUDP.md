tcp and udp both operate in the layer 4
i.e transport layer of the osi model

TCP is a connection oriented transport protocol that breaks the information into ordered bytes

tcp transmits http requests in the form of bytes 

tcp performs a three way handshake 


tcp is byte stream whereas udp is message oriented

tcp does not preserve message boundary as udp       

whereas in case of udp each message preserves its boundary 
some common exapmles where udp is used are multiplayer games and video calls 
where the most recent data information is needed rather that retrieving the lost data 
DNS also uses TCP 

TCP: "Give me a reliable, ordered stream of bytes, and handle loss recovery for me."

UDP: "Let me send individual datagrams without a built-in connection, ordering, or retransmission mechanism. My application will handle any additional guarantees it needs."

UDP allows the application to choose which messages need reliability rather than imposing the same reliable, ordered byte stream on everything.

modern applications often use different protocols for different features 

one important point tcp doesnt prevent packet loss instead it helps applications recover from it

udp just doesnt automatically recover lost datagrams 

One question to check your understanding: Suppose two users are viewing the same Trello board, and User A creates an issue. If the WebSocket connection between User B and the server gets disconnected at that exact moment, will TCP guarantee that User B sees the new issue when they reconnect?

The answer is no. TCP's reliability applies to a connection, not across disconnected sessions. That's why real collaborative systems also resynchronize state from the backend after reconnecting.