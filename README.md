# Multi-Threaded_Chat_Server_-_Rooms

In this project, students are required to implement a multi-threaded chat room service. The system will have one (multi-threaded) chat server, several chat rooms, and multiple chatclients. Socket interface is used to implement network communications.

You may start with the provided client.c and server.c program (please download them from the folder socket programming). They list the basic program structures of the client and server usingsocket programming.

Chat Server

There is only one chat server, whose IP address is known. It listens on a well-known port toaccept JOIN request from the client. The JOIN request should contain the chat room name(suppose the name of the chat room is first) the client wants to join.

1. If the chat room first does not exist, the chat server creates a new thread (usepthread_create()) to serve for this chat room first. first will have a new port. It will receive thechat messages for chat room first, and forward the messages to all chat clients who are already infirst.
  
2. If the chat room first already exists, the chat server can make the client join the chat room directly.
