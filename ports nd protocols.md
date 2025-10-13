# Ports and Protocols
 port : virtual entry or exit point used for communnication by software applicaton to exchange information
 protocols : set of rules for data excange between network devices
 ## Network port fundementals
 port : a logical opening in a computer that represent a service
 port numbers from 0 to 65,535
|  |  |
| ------ | ------ |
| Well known ports | 0 to 1023 (uses well known ports)
| Registered ports | 1024 to 49,151   
| ephemeral | 49,152 to 65,535 (short lived temporaray ports which are opened for a just small period of time)

BOth well known and registered ports are registered with IANA(Internet assigned numbers authority)

## TCP(transmission control protocol)
protocol within the ip with set of rules for exchanging the data
responsible for relaible transmission of data break down  messages into small packets
uses three way handshake
use sequence number and ack messages to assure the data is recieved correctly
Use PORT for communication process 
### UDP(user datagram protocol)
used specially for the time - sensitive transmissions
simple and smaller packets than TCP 8 bytes
used in situation where the speed of the transmission is mouvh more important than the precision the data
### ICMP(internet control message protocol)
part  of a ip where a set of network protocols used in network
used when service or host is unavailable
when packet time to live is expired
icmp priortize speed and simplicity over data integrity and security
header-type-code-checksum
### WEb ports and protocols
HTTP(hypertext transfer protocol)
port number 80
An application layer protocol that enables plain text communication between client and server
HTTPS(hypertext transfer protocol secure)
same but uses ssl tunnel and tls tunnel for encryption and decryption
SSL : secure sockets Layer
TLS : Transport Layer Security
### Email ports and protocols
| |   |
| ----- | ------ |
|SMTP(simple mail transfer protocol (25)| used for sending emails SMTPS(465,587) 
|POP3(post office protocol)110 | used to retrive emais from a remote server to local client. POP limits access for multiple devices as messages are stored only on the initial devices POP3S 
|IMAP(Internet message access protocol)143| allow users to operate directly on email server IMAPS(993)
SMTP for sending emails
POP3 and IMPA for reciving emaila
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
