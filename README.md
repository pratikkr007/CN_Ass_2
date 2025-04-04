# CN_Ass_2
![image](https://github.com/user-attachments/assets/cf28ecda-37fc-4121-9af5-0f8ceffc778f)

Ned File
Key Features:

    Network Definition: Creates a network with 2 clients and 1 server

    Connections:

        client1 → server1 (100ms delay)

        client2 → server1 (100ms delay)

    Module Types: Defines Server and Client as simple modules with input/output gates

    Client.cc

    This OMNeT++ module defines a Client node that initializes by logging its startup and sending a "Hello" message through its "out" gate. The initialize() function creates and sends this message, while the handleMessage() function processes incoming messages by logging their names and deleting them to free memory. The Define_Module(Client); macro registers the class as an OMNeT++ module, enabling its simulation. This setup assumes that the .ned file defines the required "out" gate and that another module (e.g., a Server) will receive and possibly respond to the message.

    Client.h
    The header file defines the Client class, inheriting from cSimpleModule, with two key methods: initialize() (for setup) and handleMessage() (to process messages). It uses include guards to prevent duplicate inclusion and imports the OMNeT++ library. 

    `
