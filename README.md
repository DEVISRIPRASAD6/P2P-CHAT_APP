Peer-to-Peer Chat Application

Team Information

Team Name: SAIBABU

Team Members & Roll Numbers:

DEVI SRI PRASAD-230001015

SAI BABU-230001036

GNANIKA-230041007

Overview

This is a Peer-to-Peer (P2P) Chat Application implemented in Python using sockets and threading. The program enables multiple peers to communicate directly by sending and receiving messages, maintaining a list of connected peers.

Features

✅ Simultaneous Send & Receive: Uses multi-threading for concurrent messaging.✅ Peer List Management: Maintains a list of active peers.✅ Structured Message Format: Ensures consistent message formatting.✅ Query Functionality: Retrieves a list of connected peers.✅ Manual & Automatic Peer Connectivity: Connect manually or auto-connect.✅ Duplicate Entry Prevention: Avoids duplicate peer entries.✅ Handles Ephemeral Ports: Extracts IP and fixed ports from received messages.

System Requirements

Programming Language: Python 3.x

Libraries Used:

socket (for networking)

threading (for simultaneous send/receive)

sys and select (for input handling)

Operating System: Windows / Linux / macOS

Installation & Setup

Step 1: Clone the Repository

git clone https://github.com/youruserid/P2P-CHAT_APP.git
cd P2P-CHAT_APP

Step 2: Run the Application

python p2p_chat.py

Step 3: Provide Input Details

When prompted, enter:

Your Team Name

Your Listening Port

Usage Instructions

Menu Options

***** Menu *****
1. Send message
2. Query active peers
3. Connect to a peer
4. Connect to active peers
0. Quit

Sending a Message

Enter choice: 1
Enter recipient's IP address: 192.168.1.10
Enter recipient's port number: 8080
Enter your message: Hello!
[SENT] 192.168.1.10:8080 TeamA Hello!

Receiving a Message

[RECEIVED] 10.206.4.201:9090 (teamX): Hey there!

Querying Active Peers

Enter choice: 2
[PEERS] Connected Peers:
- 192.168.1.10:8080
- 10.206.4.122:1255

Connecting to Peers

Manually Connect to a Peer: Enter IP and Port.

Auto-Connect to Active Peers: Connects to known peers automatically.

Exiting the Application

Enter choice: 0
[EXIT] Shutting down...

Message Format & Standardization

Messages must follow this format:

<IP ADDRESS:PORT> <Team Name> <Your Message>

Example:

10.206.4.201:8080 blockchain hello

Technical Implementation Details

Multithreading: Separate thread for receiving messages.

Sockets: Uses TCP sockets for reliable communication.

Peer List Management: Ensures unique peer storage.

Ephemeral Ports Handling: Extracts IP and fixed ports to prevent duplicate entries.

Bonus Feature Implementation:
✔ Automatic Peer Connectivity via connect_to_active_peer().
✔ Prevention of Duplicate Entries in peer list.

Testing & Expected Output

Test Case 1: Sending Messages Between Peers

✅ Peer1 (IP: 10.206.5.228:6555) sends "Hey" to Peer2 (10.206.4.201:1255).✅ Peer2 receives:

[RECEIVED] 10.206.5.228:6555 (Peer1): Hey

✅ Peer2 queries active peers:

[PEERS] Connected Peers:
- 10.206.5.228:6555

✅ Peer1 then sends another message, but Peer2 does NOT create duplicate entries.
