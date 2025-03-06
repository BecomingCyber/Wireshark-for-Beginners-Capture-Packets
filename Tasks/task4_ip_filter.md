Task 4: Visit a Web Page and Detect Its IP Address Using a Display Filter

4.1 Detect a Website Visit via TLS Handshake

A TLS handshake occurs when a client and server establish a secure connection for HTTPS. To filter and detect the TLS handshake in the packet list, use the following filter:

tls.handshake.type == 1
This filter will show packets that are part of the initial TLS handshake (type 1 corresponds to the ClientHello message).

4.2 Detect the IP Address of a Website
Once the TLS handshake is detected, you can find the IP address of the website by identifying the relevant packet.

To filter packets by the website's IP address (e.g., 142.251.163.105 for a Google server), use the following filter:

ip.addr == 142.251.163.105
This will display all packets associated with that particular IP address.