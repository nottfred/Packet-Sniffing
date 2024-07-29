Wireshark
Task 1
Install and set up Wireshark on Ubuntu:
● To install the most recent stable release of Wireshark on Ubuntu Linux, employ the add-apt-repository command as follows:
●Wireshark should not be run as a superuser for security reasons.
●The user can be added to the Wireshark group to add packet capture capabilities:

Task 2
Start a packet capture on an ethernet port and save it to file:
● The wired interface in Wireshark encompasses the capture of Ethernet packets, identified by the prefix ‘en’.
● Wireshark provides features to initiate packet capture, halt the capture, store the packets in a file, and load capture files.
● Saving a capture is only possible once the capture has been stopped.

Task 3
Use a display filter to detect HTTPS packets:
● To view specific packets within an existing packet capture, utilize a display filter.
● To exclusively display HTTPS traffic, apply a filter on TCP port 443 using the expression:
tcp.port == 443

Task 4
Visit a web page and detect its IP address using a display filter:
● You can utilize a TLS handshake display filter to identify a website visit within a packet list.
tls.handshake.type ==1
● A specific IP address is utilized as a filter to retrieve packet information for a particular website:
Locate all HTTPS packets from a capture not containing a certain IP address:
● You can use a conditional statement in Wireshark to include or exclude packets from the capture:
● To prevent execution order errors, it’s important to use parentheses in compound conditionals. 
