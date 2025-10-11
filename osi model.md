
 # Open System Interconnection(OSI) model

 ## .Application Layer
 ## .Presentation Layer
 ## .Session Layer
 ## .Transport Layer
 ## .Network Layer
 ## .Data Link Layer
 ## .Physical Layer

 ## Layer 1 Physical Layer

 .Part of a network that send data as bits (0's and 1's) through cables or wireless signals 
 .it delays with the hardware like wires,switches and how signals travel
 >Communication is done by the synchronus and asynchronus
 Synchronus: use refernce clock to coordinate the transmissions by both sender and reciever More Bandwidth utilisation
 Asynchronus: uses start and stop bits to indicate when transmission occur from sender to the reciever
 .Bandwidth is utilized in two ways 
 1.Base band : use all available frequencies on medium to transmit data
 2.Broad band : Divides bandwidth into separate channels
 >If single baseband uses all bandwidth there are different mechanisms to do 
 1.Time Division Multiplexing : Multiple signals share same communcation channel but instead of sending data simultaneously each one get a time slot to transmit
 ex : Every person in a classroom will get a chance to speak
 2.Stastical Time Division Multiplexing : Dynamically allows time slots as needed
 ex : Only intrested will get a chance to speak 
 3. Frequency Division Multiplexing : divides the medium into channels based on frequency and each session is transmited over a different channel
 >Multiplexing allows multiple people to use a base band connection at same time
### Transistion Modulation:
 . if it changes or switches during the cycle then 1 is represnted otherwise 0 
 ex: Fiber optic cable connected as on and off for fan if it is on then represnted as 1 if its off then 0

 .Cables are also part of it TIE/EIA 568A,TIA/EIA/568B  these are the standard wiring ethernet cables
 .cross over cables : conneted to different cables A to B
 .straight through cables : connected to same cables B to B
 <>Examples : Fiber Optic Cables,Ethernet Cables


 ## Layer 2 Data Link Layer

 .Packages the data(bits) recieved into frames and then transmit throughout the network by identifying unique network device MAC adresses
 -Media Access Control(MAC) : Physical adress of a device but operates as logical topology 
 48 bit physical adressing system assigned to evert Network Interface Card(NIC) 
 D2:33:C5:99:44:76  Each letter or a digit is 4 bits 
 first 6 are the vendor code next are the unique value which exact machine belongs to
 ### Logical Link Control
 . provides services connections and allows acknowledgement of reciept of messages
 . basic form of flow control
 . provides basic error control functions (data recieved or corrupted)
 > Communication can be in Three ways Isynchronus,Synchronus,asynchronus
 Isynchronus : Network device use a common reference clock source and create time slot for transmission
 <> Examples : MAC,NIC,Switches 


## Layer 3 Network Layer 

 Logical Adressing + Switching + Route discoverey or seletion
 .Logical Adressing : assing ip address to the devices 
 .Switching can be done in three ways
 1.Packet Switching : finding the best path through routers to reach the destination
 2.Circuit Switching : Dedicated communication link is established between the two devices
 3.Message Switching : Data is divide into messages and then stoerd and thenn forward
 .Route discoverey and selection1 : manually configured as a static route or dynamically through Routing Protocol
 ### Routing Protocol
 .How the data flows across the network 
 .How the router communicate the information and choose the best path
 Flow Control : Prevents the sender from sending too fast asks to send slow or fast as required
 Packet Reordering : Big data is converted into small packets and choose different directions to reach the destination. Each packet gets the sequence and the Number
 <>Example : routers,ipv4,ipv6,multilayer switches

 ## Layer 4 Transpot Layer

 Dividing line between the upper layers and lower layers of osi models
 data into segments 
 .Transmission control protocol(TCP) : Connection Orieanted protocol a reliable way to transport segments across network
 .User Datagram protocoln (UDP) : Connectionless unrelaible to transport segments across network

 | TCP | UDP |
 | ---- | ---- |
 |Reliable | unrelaible
 |connection orieanted| connection less 
 |segment retransmission and flow control througj windowing| no retransmission and no windowing
 |segment sequencing| no sequencing
 |Acknowledging segments| no acknowledgement

 Windowing : Allows the clients to adjust the amount of data in each segment less data is being sent with increase in retransmission
 Example: While downloading timer will be shown
 Buffering : Occurs when the device allocate memory to stoe segments if bandwidth is not readily available
 <> Examples TCP,UDP,Firewalls and Load Balancer


 ## Layer 5 Session Layer

 .Kepps conversations separate to perevent interminling of data 
 1.Setup : Check user credentials and assign number of sessions to help to identify them
 2.Maintain : Where the data is transmittes back and forth across network
 3. Tear Down : End of a session after tarnsfer is done or when the other party is disconnected
 <>Example : h.323 (setup,maintain,teardown of voice and video connections ),netbios(used to share the files across the network)


 ## Layer 6 Presentation Layer

 Responsible for formating the data exchanged and securing the data from the with proper encryption
 ### Data Formatting

 Converts the data into a common format that the recieving system can understand
 ASCII(American Standarad code For Informatiom Interchange)
 . Ensure data is redable by recieving system 
 . provide proper data structure
. negotiates data transfer syntax for layer 7 
 Encryption : Used to scramble the data whie transmittimg and keep safe from hackerand ensure data confidentiality
 <>Example : media files,pictuers,scripting Languages

 ## Layer 7 Application Layer 
 Provide Application services where users communicate with the computer

 # Encapsulation and Decapsulation

 process of putting the header(sometimes trailer) to the data 
 Encapsualation is done from layer 7 to layer 1 and decapsulation from layer 1 to layer 7
 ## protocol data unit (PDU)
 -we use pdu to transmit the data and control flags for the data flow
 -a single unit of information is transmitted in a computer network
 ## Control Flags
 |  |  |
 | ---- | ---- |
 |SYN(synchronisation)| used to synchronise connection during three way hand shake
 |ACK(ackonwledgement)| used during 3 way handshake and acknowledges the message recipets of the packets
 |FIN(Finish)| used to taer doen the connection established in three way handshake
 |RST(reset)|when client and server recievs the packet if it was not exected during current connections
 |PSH(Push)|ensure data is given prioritse and processed at the sender and the reciever ends
 |URG(Urgent)|similar to push and identify incoming data as data

 ### L4 TCP/UDP header
 -add the source and destination ports 
 ### L3 IP header
 -add  source and destination ip adresses
 ### L2 ETHERNET header
 -add source and destination mac adresses
 ### L1 Header
 -tranmits frames as series of 1's and 0's
 
  






