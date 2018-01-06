### Unit 1

# Network Systems and Protocols

1. [Types of network](#types-of-network)
1. [Network protocols and standards](#network-protocols-and-standards)
1. [Application layer protocols](#application-layer-protocols)

## Unit Details

## [1.1. Types of network](#types-of-network)

- Based on Size
- Based on Topology
- Network Access Methods
- How internet works ?
- Basic Client Server Architecture
- Network models
  - OSI Model,
    1. Application Layer
    1. Presentation Layer
    1. Session Layer
    1. Transport Layer
    1. Network Layer
    1. Data Link Layer
    1. Physical Layer
  - TCP/IP Model
    1. Application Layer
    1. Transport Layer
    1. Network Layer
    1. Physical Layer

## [1.2 Network protocols and standards](#network-protocols-and-standards)

- Types of Network protocols and standards
  - TCP/IP
  - AppleTalk
  - UDP
  - 802.2
  - 802.3
  - FDDI
  - 802.5
- Wireless technologies
  - 802.11
  - Infrared
  - Bluetooth
  - 3G
- Factors Affecting range and speed of wireless technologies

## [1.3 Application layer protocols]((#application-layer-protocols))

1. DNS
1. DHCP
1. HTTP
1. FTP
1. SMTP

---

# Types of network

## Based on Size

1. Personal Area Network (PAN)
1. Local Area Network (LAN)
1. Metropolitan Area Network (MAN)
1. Wide area network (WAN)
1. Internet

## Based on Topology

1. Star Topology
1. Bus Topology
1. Ring Topology
1. Mesh Topology
1. Tree Topology

## Network Access Methods

### 1. CSMA Carrier Sense Multiple Access

Carrier sense multiple access (CSMA) is a media access
control (MAC) protocol in which a node verifies the absence 
of other traffic before transmitting on a shared transmission
medium. A transmitter attempts to determine whether another
transmission is in progress before initiating a transmission
using a carrier sense mechanism. That is, it tries to detect
the presence of a carrier signal from another node before
attempting to transmit. If a carrier is sensed, the node
waits for the transmission in progress to end before
initiating its own transmission.

### 2. Token Passing

In network communication, token passing is a channel access method
where a signal called a token is passed between nodes
that authorizes the node to communicate.
It uses Round-robin scheduling algorithms.
The advantage over other channel access method is
that collisions are eliminated, and that the channel
bandwidth can be fully utilized without idle time when
demand is heavy.
The disadvantage is that even when demand is light,
a station wishing to transmit must wait for the token,
increasing latency.

## How internet works ?

### Client Server Architecture

1. Client
1. Server
1. Request
1. Response

## Network models

### OSI Model

#### 1. Application Layer

- Contains variety of protocols that are commonly used.
- One widely used application protocol is HTTP (HyperText Transfer Protocol)
- Which is the basis for the World Wide Web. 
- When a browser wants a Web page, it sends the name of the page it wants to the server hosting the page using HTTP. The server then sends the page back.
- Other application protocols are used for
  - file transfer (FTP)
  - electronic mail (SMTP)

#### 2. Presentation Layer

- Unlike the lower layers, which are mostly concerned with moving bits around, the presentation layer is concerned with the syntax and semantics of the information transmitted.
- In order to make it possible for computers with different internal data representations to communicate, the data structures to be exchanged can be defined in an abstract way, along with a standard encoding to be used ‘‘on the wire.’’
- Manages these abstract data structures
- Allows higher-level data structures (e.g., banking records) to be defined and exchanged.
  
#### 3. Session Layer

- The session layer allows users on different machines to establish sessions between them. 
- Sessions offer various services, such as:
  - Dialog control (keeping track of whose turn it is to transmit),
  - Token management (preventing two parties from attempting the same critical operation simultaneously), and 
  - Synchronization (checkpointing long transmissions to allow them to pick up from where they left off in the event of a crash and subsequent recovery).
- Examples
  - Session Maintenance in Banking Transactions
  - E-commerce (Carts Data/info)
  - User Sessions (Facebook)

#### 4. Transport Layer

- The basic function of the transport layer is
  - to accept data from above it,
  - split it up into smaller units if need be,
  - pass these to the network layer, and
  - ensure that the pieces all arrive correctly at the other end.
- This must be done efficiently and in a way that isolates the upper layers from the inevitable changes in the hardware technology over the course of time.
- The transport layer also determines
  - what type of service to provide to
    - the session layer, and,
    - ultimately, to the users of the network.
- The most popular type of transport connection is
  - an error-free point-to-point channel that delivers messages or bytes &
  - in the order in which they were sent.
- However, other possible kinds of transport service exist, such as the transporting of isolated messages with no guarantee about the order of delivery, and the broadcasting of messages to multiple destinations.
- The type of service is determined when the connection is established.
- (As an aside, an error-free channel is completely impossible to achieve; what people really mean by this term is that the error rate is low enough to ignore in practice.)
- The transport layer is a true end-to-end layer;
  - it carries data all the way from the source to the destination.
- In other words, a program on the source machine carries on a conversation with a similar program on the destination machine, using the message headers and control messages. In the lower layers, each protocols is between a machine and its immediate neighbors, and not between the ultimate source and destination machines, which may be separated by many routers.
- The difference between layers 1 through 3, which are chained, and layers 4 through 7, which are end-to-end.
  
#### 5. Network Layer

- The network layer controls the operation of the subnet.
- A key design issue is determining how packets are routed from source to destination. Routes can be based on static tables that are ‘‘wired into’’ the network and rarely changed, or more often they can be updated automatically to avoid failed components.
- They can also be determined at the start of each conversation, for example, a terminal session, such as a login to a remote machine.
- Finally, they can be highly dynamic, being determined anew for each packet to reflect the current network load.
- If too many packets are present in the subnet at the same time, they will get in one another’s way, forming bottlenecks.
- Handling congestion is also a responsibility of the network layer, in conjunction with higher layers that adapt the load they place on the network. More generally, the quality of service provided (delay, transit time, jitter, etc.) is also a network layer issue.
- When a packet has to travel from one network to another to get to its destination, many problems can arise.
- The addressing used by the second network may be different from that used by the first one.
- The second one may not accept the packet at all because it is too large. The protocols may differ, and so on.
- It is up to the network layer to overcome all these problems to allow heterogeneous networks to be interconnected.
- In broadcast networks, the routing problem is simple, so the network layer is often thin or even nonexistent.

#### 6. Data Link Layer

- The main task of the data link layer is to transform a raw transmission facility into a line that appears free of undetected transmission errors.
- It does so by masking the real errors so the network layer does not see them.
- It accomplishes this task by having the sender break up the input data into data frames (typically a few hundred or a few thousand bytes) and transmit the frames sequentially.
- If the service is reliable, the receiver confirms correct receipt of each frame by sending back an acknowledgement frame.
- Another issue that arises in the data link layer (and most of the higher layers as well) is how to keep a fast transmitter from drowning a slow receiver in data.
- Some traffic regulation mechanism may be needed to let the transmitter know when the receiver can accept more data.
- Broadcast networks have an additional issue in the data link layer: how to control access to the shared channel.
- A special sublayer of the data link layer, the medium access control sublayer, deals with this problem.

#### 7. Physical Layer

- The physical layer is concerned with transmitting raw bits over a communication channel.
- The design issues have to do with making sure that when one side sends a 1 bit it is received by the other side as a 1 bit, not as a 0 bit.
- Typical questions here are
  - what electrical signals should be used to represent a 1 and a 0,
  - how many nanoseconds a bit lasts,
  - whether transmission may proceed simultaneously in both directions,
  - how the initial connection is established,
  - how it is torn down when both sides are finished,
  - how many pins the network connector has, and what each pin is used for.
- These design issues largely deal with mechanical, electrical, and timing interfaces, as well as the physical transmission medium, which lies below the physical layer.

### TCP/IP Model

#### 1. Application Layer

- The TCP/IP model does not have session or presentation layers.
- No need for them was perceived. Instead, applications simply include any session and presentation functions that they require.
- Experience with the OSI model has proven this view correct: these layers are of little use to most applications.
- On top of the transport layer is the application layer.
- It contains all the higher- level protocols. Such As:
  1. DNS (Domain Name Server) - Protocol
  1. DHCP (Dynamic Host Control Protocol)
  1. HTTP (Hyper Text Transfer Protocol)
  1. FTP (File Transfer Protocol)
  1. SMTP (Simple Mail Transfer Protocol)

#### 2. Transport Layer

- The layer above the internet layer in the TCP/IP model is now usually called the transport layer. 
- It is designed to allow peer entities on the source and destination hosts to carry on a conversation, just as in the OSI transport layer. 
- Two end-to-end transport protocols have been defined here.
  - The first one, TCP (Transmission Control Protocol), is a reliable connection-oriented protocol that allows a byte stream originating on one machine to be delivered without error on any other machine in the internet.
    - It segments the incoming byte stream into discrete messages and passes each one on to the internet layer.
    - At the destination, the receiving TCP process reassembles the received messages into the output stream. 
    - TCP also handles flow control to make sure a fast sender cannot swamp a slow receiver with more messages than it can handle.
  - The second protocol in this layer, UDP (User Datagram Protocol), is
    - an unreliable,
    - connectionless protocol for applications that do not want TCP’s sequencing or flow control and wish to provide their own.
- It is also widely used for one-shot, client-server-type request-reply queries and applications in which prompt delivery is more important than accurate delivery, such as transmitting speech or video.

#### 3. Internet/Network Layer

- The internet layer holds the whole architecture together.
- It roughly corresponds to the OSI network layer.
- Its job is to permit hosts to inject packets into any network and have them travel independently to the destination (potentially on a different network).
- They may even arrive in a completely different order than they were sent, in which case it is the job of higher layers to rearrange them, if in-order delivery is desired.
- Note that ‘‘internet’’ is used here in a generic sense, even though this layer is present in the Internet.
- The analogy here is with the (snail) mail system.
  - A person can drop a sequence of international letters into a mailbox in one country, and with a little luck, most of them will be delivered to the correct address in the destination country.
  - The letters will probably travel through one or more international mail gateways along the way, but this is transparent to the users.
  - Furthermore, that each country (i.e., each network) has its own stamps, preferred envelope sizes, and delivery rules is hidden from the users.
- The internet layer defines an official packet format and protocol called IP
- (Internet Protocol), plus a companion protocol called ICMP (Internet Control Message Protocol) that helps it function.
- The job of the internet layer is to deliver IP packets where they are supposed to go. Packet routing is clearly a major issue here, as is congestion (though IP has not proven effective at avoiding congestion).

#### 4. Physical Layer

- All these requirements led to the choice of a packet-switching network based on a connectionless layer that runs across different networks.
- The lowest layer in the model, the link layer describes what links such as serial lines and classic Ethernet must do to meet the needs of this connectionless internet layer.
- It is not really a layer at all, in the normal sense of the term, but rather an interface between hosts and transmission links.
- Early material on the TCP/IP model has little to say about it.

<!-- - Intranet & Extranet
  - Intranet
    - Intranet is a computer network system in which a specific organizational systems share information, computing services and operational systems with each other by using an Internet (IP) technology.
    - This term basically refers to the network of a specific organization.
    - You can also says it a private network.
    - Authenticated users of the organization can access the database system, search engines, directory and can distribute documents and workflow.
    - Employees can makes interactive communication in shape of chatting, audio and videoconferencing, groupware and teleconferencing.
  - Extranet
    - Extranet is a kind of computer network that allows the outside users to access the Intranet of organization.
    - This network system is basically used for business to business (B2B) purposes.
    - This system basically allows the outside users of an organization, like partners, suppliers, vendors and other stakeholders to remain in touch with the activities of organization. -->

<!-- - Multiplexing & De-Multiplexing
  - Transport layer at the sender side receives data from different Applications , encapsulates every packet with a Transport Layer header and pass it on to the underlying Network Layer. This job of transport layer is known as Multiplexing.
  - At the receiver's side, the transport gathers the data, examines it socket and passes the data to the correct Application. This is known as De-Multiplexing.
  - Sockets are the door between Transport and Application Layer.  If you want to read about socket, visit this. Socket.  Let us take a very simple example that will make you clear with all these terms.
  - Suppose that there are two houses. One is in India and Other is in America. In the house in India, lives a person James along with his 5 children. And in the house in America, lives a person Steve along with his 4 children. Now all 5 children of James write a letter to every children of Steve on every Sunday. Therefore total number of letters will be 20. Thus, all the children writes the letter , put them in envelopes and hand over it to James. Then James write source house address and the destination house address on the envelope and give it to the postal service of India. Now the postal service of India puts some other addresses corresponding to the country and delivers it to the America postal Service. The American Postal sees the destination address on the envelopes and will deliver those 20 letters to the Steve House. Steve collects the letter from the postman and after considering the name of his respective children on the envelopes, he gives the letter to each of them.
  - In this example we have processes and the layers as:
    - Processes = children
    - Application Layer messages = envelopes
    - Hosts = The two Houses
    - Transport Layer Protocol = James and Steve
    - Network Layer protocol = Postal Service
  - When James collects all the letters from his children, he multiplexes all and encapsulates them with the respective children name on the letter and  house address and give it to the Indian postal service.
  - On the receiving side, Steve collects all the letters from postal service of America and de-multiplexes them to see , which letter is for which child and delivers it respectively. -->

<!-- - Circuit Switching & Packet Switching -->
<!-- - Modes of Communication -->
  <!-- - Simplex
    - Simplex is one direction. A good example would be your keyboard to your CPU. The CPU never needs to send characters to the keyboard but the keyboard always sends characters to the CPU. In many cases, Computers almost always send characters to printers, but printers usually never send characters to computers (there are exceptions, some printers do talk back). Simplex requires only one lane (in the case of serial).
  - Duplex
    - Half Duplex
      - Half-Duplex is like the dreaded "one lane" road you may have run into at construction sites. Only one direction will be allowed through at a time. Railroads have to deal with this scenario more often since it's cheaper to lay a single track. A dispatcher will hold a train up at one end of the single track until a train going the other direction goes through. The only example I could think of for Half-Duplex is actually a Parallel interface. Even though parallel is eight lanes, data travels through the lanes in the same direction at the same time but never in both directions at the same time. The IEEE-1284 allows printers to send messages to the computer. The printer cannot send these messages while the computer is sending characters but when the computer stops sending characters, then the printer can send messages back. It's kind of like some roads that head into downtown. In the morning, they're one way roads, allowing traffic to go into downtown. In the evening their one way roads, allowing traffic to head out of downtown. The only advantage that Half-Duplex would have is the single lane or single track is cheaper then the double lane or double track.
    - Full Duplex
      - Full-Duplex is like the ordinary two-lane highway. In some cases, where traffic is heavy enough, a railroad will decide to lay a double track to allow trains to pass in both directions. In communications, this is most common with networking. Our fiber optic hubs have two connectors on each port, one for each lane of a two-lane roadway. Full-Duplex fiber is two cables bundled or tied together to form the two-lane roadway. In 100Base-TX, the two lanes are housed in the same jacket. RS232 was also designed to handle Full-Duplex but some of our short haul modems and converters give the user the option to go Half-Duplex or Simplex to reduce the number of conductors needed to connect between them. -->

# Network protocols and standards:
  
  - Types {eg:}
    - TCP/IP (Transmission Control Protocol/Internet Protocol)
      - TCP/IP is the basic communication language or protocol of the Internet.
      - It can also be used as a communications protocol in a private network (either an intranet or an extranet).
      - When you are set up with direct access to the Internet, your computer is provided with a copy of the
      - TCP/IP program just as every other computer that you may send messages to or get information from also has a copy of TCP/IP.
    - AppleTalk
      - AppleTalk was a proprietary suite of networking protocols developed by Apple Inc. for their Macintosh computers.
      - AppleTalk includes a number of features that allow local area networks to be connected with no prior setup or the need for a centralized router or server of any sort.
      - Connected AppleTalk-equipped systems automatically assign addresses, update the distributed namespace, and configure any required inter-networking routing.
      - It is a plug-n-play system.
      - AppleTalk was released in 1985, and was the primary protocol used by Apple devices through the 1980s and 1990s.
      - Versions were also released for the IBM PC and compatibles and the Apple IIGS. AppleTalk support was also available in most networked printers (especially laser printers), some file servers, and a number of routers.
    - UDP
    - 802.2, 
    - 802.3, 
    - FDDI, 
    - 802.5;
  - wireless technologies eg 
    - 802.11, infrared, 
    - Bluetooth, 
    - 3G; 
  - factors affecting range and speed of wireless technologies

- WAN technologies
  - Frame relay
  - MPLS
    - What is MPLS?
      - Multi-Protocol Label Switching is a method of ensuring packets of data get where they're supposed to, via a sensible route, and that packets are prioritised appropriately.
      - Packets are labelled with one or more labels. As each packet passes through the MPLS network, labels may be added, replaced or stripped off. The network distributes information so that each switch knows what it is supposed to do if it encounters a particular label.
    - The Benefits of MPLS Networks
      - Improve Uptime 
        - by sending data over an alternative path in less than 50 milliseconds (if one exists). MPLS also reduces the amount of manual intervention your network provider has to do to create a WAN, reducing the likelihood of human error bringing down your circuit.
      - Create Scalable IP VPNs
        - with MPLS it's easy to add an additional site to the VPN. There is no need to configure a complex mesh of tunnels, as is common with some traditional approaches.
      - Improve User Experience
        - by prioritising time-sensitive traffic such as VoIP. Multi-Protocol Label Switching offers multiple Classes of Service, enabling you to apply separate settings to different types of traffic.
      - Improve Bandwidth Utilisation
        - by putting multiple types of traffic on the same link, you can let high priority traffic borrow capacity from lower priority traffic streams whenever required. Conversely, when the lower priority traffic needs to burst beyond its usual amount of bandwidth, it can use any capacity that's not being used by higher priority services.
      - Hide Network Complexity
        - an MPLS connection between two sites can be configured to act like a long ethernet cable, with the hops involved hidden from view. This is sometimes known as VPLS (Virtual Private LAN Service).
      - Reduce Network Congestion
        - Sometimes the shortest path between two locations isn't the best one to take, as congestion has made it less attractive (at least for the time being). MPLS offers sophisticated traffic engineering options that enable traffic to be sent over non-standard paths. This can reduce latency (the delay in sending/receiving data). It also reduces congestion on the paths that have just been avoided as a result of traffic engineering.
    - MPLS is particularly well suited for use in Carrier Networks and corporate Wide Area Networks
      - The technology is particularly well-suited to use in corporate Wide Area Networks
      - Multi-Protocol Label Switching is particularly useful for situations where...
        - multiple types of traffic share a data connection, with some types of traffic requiring priority over others
        - uptime is important, key locations have multiple connections so that alternative paths always exist
        - network congestion occurs sometimes on some connections
        - new sites will need to be able to connect to many different locations, while being entirely invisible to many other sites on the network.
      - This is why MPLS is widely used by the major telecoms companies. It's also very popular with organisations that need a scalable WAN that can carry both voice (phone calls) and data.
  - ATM
    - ATM (asynchronous transfer mode) is a dedicated-connection switching technology that organizes digital data into 53-byte cell units and transmits them over a physical medium using digital signal technology.
    - Individually, a cell is processed asynchronously relative to other related cells and is queued before being multiplexed over the transmission path.
    - Because ATM is designed to be easily implemented by hardware (rather than software), faster processing and switch speeds are possible. 
    - The prespecified bit rates are either 155.520 Mbps or 622.080 Mbps.
    - Speeds on ATM networks can reach 10 Gbps.
    - Along with Synchronous Optical Network (SONET) and several other technologies, ATM is a key component of broadband ISDN (BISDN).
- Network access methods
  - CSMA
  - Token passing;

# Application layer protocols

- 1. DNS (Domain Name Server) - Protocol
  - DNS Lookup PROCESS
    - Your computer asks your router for a DNS Record
    - Your router asks your ISP for a DNS Record
    - Your ISP asks the Root Name server for the Name Server.
    - The Root server gives your ISP the Name server.
    - Your ISP asks the Name server for a DNS record.
    - The Name server gives you ISP the DNS Record.
    - Your ISP gives your Router the DNS Record.
    - Your Router gives your computer the DNS Record.
  - DNS Management
    - DNS management controls Domain Name System (DNS) server clusters. DNS data is typically deployed on multiple physical servers. The main purposes of DNS management software are: to reduce human error when editing complex and repetitive DNS data.
  - DNS Flavours
    - Generic
      - .com, .edu, .gov, .org, .net
    - Countries
      - .np, .in, .uk, .pk
    - ICANN (Internet Corporation for Assigned Names and Numbers)
    - ICANN was formed in 1998. It is a not-for-profit partnership of people from all over the world dedicated to keeping the Internet secure, stable and interoperable. It promotes competition and develops policy on the Internet’s unique identifiers.
    - ICANN doesn’t control content on the Internet. It cannot stop spam and it doesn’t deal with access to the Internet. But through its coordination role of the Internet’s naming system, it does have an important impact on the expansion and evolution of the Internet.
- 2. DHCP (Dynamic Host Control Protocol)
  - DHCP Server
  - DHCP Lookup
  - Issue:
    - An issue that arises with automatic assignment of IP addresses from a pool is for how long an IP address should be allocated.
    - If a host leaves the network and does not return its IP address to the DHCP server, that address will be permanently lost.
    - After a period of time, many addresses may be lost.
    - To prevent that from happening, IP address assignment may be for a fixed period of time, a technique called leasing.
    - Just before the lease expires, the host must ask for a DHCP renewal.
    - If it fails to make a request or the request is denied, the host may no longer use the IP address it was given earlier.
- 3. HTTP (Hyper Text Transfer Protocol)
- 4. FTP (File Transfer Protocol)
- 5. SMTP (Simple Mail Transfer Protocol)
  - Simple Mail Transfer Protocol (SMTP) is an Internet standard for electronic mail (email) transmission.
  - First defined by RFC 821 in 1982, it was last updated in 2008 with Extended SMTP additions by RFC 5321, which is the protocol in widespread use today.
  - Although electronic mail servers and other mail transfer agents use SMTP to send and receive mail messages, user-level client mail applications typically use SMTP only for sending messages to a mail server for relaying.
  - For retrieving messages, client applications usually use either IMAP or POP3.
  - Internet Message Access Protocol
  - SMTP communication between mail servers uses port 25.

## Transport Layer Protocols

- TCP
- UDP

## Internet Layer Protocols

- IP
- ICMP