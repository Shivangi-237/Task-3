#FILE HANDLING UTILITY

*COMPANY*: CODETECH IT SOLUTIONS

*NAME*: SHIVANGI SHARMA

*INTERN* ID: CT08RVQ

*DOMAIN*: JAVA

*DURATION*: 4 WEEKS

*MENTOR*: NEELA SANTOSH

#This Java-based chat application consists of two primary components: a Chat Server and a Chat Client, enabling real-time communication between multiple users over a network. The server efficiently manages multiple clients simultaneously, ensuring smooth communication, while the client provides an interface for sending and receiving messages in a group chat format. The application utilizes socket programming and multi-threading to facilitate seamless interaction between users.

The Chat Server operates on port 12345, continuously listening for incoming client connections using a ServerSocket. When a new client connects, the server assigns a separate ClientHandler thread to manage communication with that specific user. This allows multiple clients to participate in the chat without interfering with each other. Upon connecting, the client is prompted to enter a username, which is then broadcasted to all other connected users, informing them of the new participant.

A key feature of the server is its message broadcasting mechanism, ensuring that messages sent by any client are relayed to all others except the sender. The server keeps track of all active clients in a Set, ensuring proper management of connected users. If a client disconnects, their reference is removed from the set, preventing unnecessary resource usage and keeping the chat environment updated with only active participants.

On the client side, users can connect to the server and interact in real-time through a console-based interface. The client establishes a socket connection with the server and utilizes BufferedReader and PrintWriter for handling incoming and outgoing messages. A separate thread is dedicated to listening for messages from the server, ensuring real-time updates while allowing users to type and send their own messages simultaneously. This approach prevents blocking and ensures that new messages appear instantly without disrupting user input.

The client continuously sends user messages to the server, which broadcasts them to all connected participants. The connection remains active until the user decides to terminate it, ensuring a persistent communication channel. The use of multi-threading allows the system to efficiently manage multiple clients without lag or delays, making the chat experience smooth and interactive.

This chat system effectively demonstrates essential networking concepts, such as:

Socket Programming: Establishing real-time TCP-based communication between the server and multiple clients.
Multi-threading: Ensuring each client has an independent thread to handle message exchange efficiently.
Message Broadcasting: Allowing group chat functionality where messages from one client are shared with all others.
Client Management: Tracking active users and removing disconnected clients to maintain an updated list of participants.
Overall, this Java chat application provides a fundamental implementation of network-based messaging, focusing on server-client communication, multi-threading, and real-time message exchange. It ensures efficient handling of multiple users, making it a reliable example of basic group chat functionality using Java networking.
