Task 3: Use a Display Filter to Detect HTTPS Packets

3.1 Displaying HTTPS Traffic
You can use Wireshark’s display filters to focus on specific types of traffic, such as HTTPS (which uses TCP port 443).

To filter for HTTPS traffic:

In the Display Filter bar at the top of Wireshark, enter the following filter:

tcp.port == 443
This filter will display only packets that are being transmitted over TCP port 443, which is used for HTTPS.