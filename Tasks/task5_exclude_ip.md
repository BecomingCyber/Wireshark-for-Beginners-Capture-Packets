Task 5: Locate All HTTPS Packets from a Capture Not Containing a Certain IP Address

5.1 Exclude a Specific IP Address

To locate all HTTPS packets (TCP port 443) excluding traffic from a specific IP address (e.g., 8.43.85.97), use the following conditional statement in the Display Filter bar:


!(ip.addr == 8.43.85.97) and tcp.port == 443
This filter excludes any packets from the IP address 8.43.85.97 and only shows HTTPS traffic.

5.2 Combine Multiple Filters Using Parentheses

To combine multiple conditions, use parentheses to group the conditions correctly. For example, to filter for both HTTP and HTTPS traffic, excluding a certain IP address, use:

!(ip.addr == 8.43.85.97) and (tcp.port == 80 or tcp.port == 443)
This filter will:

Exclude packets from the IP address 8.43.85.97.
Show both HTTP (port 80) and HTTPS (port 443) traffic.
