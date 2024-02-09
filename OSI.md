# OSI MODEL

All People Seem To Need Data Processing
##### Application

Provides the user interface. It's the spot where users actually communicate to the computer. It only comes into play when its clear that access to the network will be needed soon. For example, you could uninstall all network components like TCP/IP & NIC cards and still use a browser to view a local HTML document. However, it would be quite difficult to do much else. If you'd like to retrieve a remote HTML document, you wouldn't be able to do so without accessing the Application Layer.

Essentially, the application layer is the interface between actual application programs and the next layer down by providing ways for the application to send information through the protocol stack. Remember, browsers don't live in the application layer, but they interface with it as well as other relevant protocols when asked to access remote resources.

Some functions of the application layer include identifying and confirming communication partner's availability and verifying required resources to permit the specified type of communication. This is important because most browser functions require more than desktop resources. It's actually very common for components of several network applications to communicate and carry out a requested function. Event examples:
- Web Browsing
- File Transfers
- Email
- Enabling remote access
- Network Management
- Client/Server Processes
- Information Location


##### Presentation

Presents data in the proper format
Handles processing like encryption

The presentation layer presents data to the Application layer and is responsible for data translation and code formatting. It can be considered like a translator providing coding and conversion services. In practice, data transferring is typically converted into a standard format before transmission. ASCII is an example of one of those formatted data types. It can be re-formatted to its native state for reading.

OSI will also include protocols that define how standard data should be formatted. Which means key functions like data compression, decompression, encryption, and decryption are also associated with this layer.
##### Session

The session layer is responsible for setting up, managing, and dismantling sessions between presentation layer entities and keeping user data separate. Dialog control between devices also occurs at this layer.

Communication between hosts various applications is coordinated and organized via three different modes: *Simplex, half duplex, and full duplex*

Simplex -> One way communication
Half-Duplex -> Two way communication which can only take place in one direction at a time.
Full-Duplex -> 'Real conversation' where devices can transmit and receive at the same time.

TLDR; Keeps different applications' data separate!

##### Transport
Provides reliable or unreliable delivery
Performs error correction before retransmitting

Segments and reassembles data into a single data stream. Services on this layer will take all various data received from upper-layer applications and then combine it into the same, concise data stream.. These protocols provide end-to-end data transport services and can establish logical connections between the sending host and destination host on an internetwork.

Some well known transport layer protocols are TCP & UDP. Transport layer can either be connection based or connectionless.

Connection oriented communications require a call setup or three way handshake (SYN -> SYN/ACK -> ACK -> Data Transfer)


Flow Control

Floods and data loses can be tragic. There is a fail-safe solution in-place known as flow control that can ensure data integrity at the Transport layer remains. It allows applications to request reliable data transport between systems. Flow control prevents a sending host from overflowing the buffer in the receiving host.

Reliable data Transport requires these achievements:
- Segments delivered are acknowledged back to the sender upon their reception.
- Any segments not acknowledged are retransmitted.
- Segments are sequenced back into their proper order upon arrival at their destination.
- A manageable data flow is maintained in order to avoid congestion, overloading, or worse, data loss.

Transport layer will enforce this by issuing a 'not ready' indicator to the sender or potential source of the flood. When the peer receiver processes the segments already in its memory reservoir (buffer), it sends out a 'ready' transport indicator. When the machine waiting to transmit receives the 'go' indicator, it will resume.

Connection-oriented characteristics
- Virtual Circuit/Three-Way-Handshake
- Sequencing
- Acknowledgements
- Flow Control 
##### Network
Provides logical addressing, routers will use for path determination (IP addressing)

##### Data-Link
Combines Packets into bytes and bytes into frames
Provides access to media using MAC address
Performs error detection not correction

##### Physical
Move bits between devices
Specifies voltage, Wire Speed, and Pinout of cables.


The lower layers determine how to rebuild a data stream from a transmitting host to a destination hosts application (how data is transmitted). The lower layers are:
- Transport
- Network
- Data-Link
- Physical

The upper layers define how the applications within the end stations will communicate with each other and with users.
