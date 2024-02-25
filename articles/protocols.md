# Network protocols

## [TODO]

* Show for each concepts an used case with GNU/Linux

* Higher level introduction to Network protocol
* In another article express layer model in network.

### Web Browser: Defenitly Firefox

# Network Protocols Usage

Network protocols play a critical role in making the internet work.
Without them, there would be no way for servers or devices to communicate with each other.
Every piece of online content—from text to images, video and audio—is delivered to the end user via network protocols.

A network protocol is a mechanism or a set of procedures that enables devices to communicate
back and forth across the internet.

In order to communicate together, two devices must support the same protocol or 
a gateway will need to be used to translate the communication.

شیوه‌نامهٔ ارتباطی
دو دستگاه یا موجودیت ارتباطی، برای ارسال پیغام به یکدیگر نیاز به روش‌ها و زبانی مشترک دارند.
یک شیوه‌نامهٔ ارتباط به استاندارد سازی و تعریف روش برقراری ارتباط و ارسال پیام می‌پردازد.

There are **three main types of network protocols** you need to be aware of:

**Network management protocols**

These protocols set out policies designed to monitor, manage and maintain a network. 
Examples include:
* SNMP
* FTP
* POP3
* Telnet
* DNS
* DHCP
* NTP

**Network communication protocols**

A group of protocols used to establish rules and formatting (such as syntax, synchronization and semantics) for exchanging data across a network. 
Types of network communication protocols include:
* TCP
* UDP
* IP
* ICMP
* HTTP
* IRC
* BGP 
* ARP
    
**Network security protocols**

(extra S letter in name point to secure)
Security protocols are protocols that use security measures such as cryptography and encryption to protect data. 
Examples include:
* HTTPS
* SFTP
* SSL/TLS

## Network Protocol vs. Internet Protocol

While there are many different types of network protocols,
Transmission Control Protocol (TCP) is one of the most widely used 
Why? 
due to its ability to break down data into packets (packetize, atomic unit)
so they can be transferred (you can read more about TCP further below).

Under the traditional TCP/IP model of networking, TCP is used alongside the Internet Protocol (IP) to identify hosts to send data across the internet.

Within this model, IP identifies and defines the IP address of devices or applications that data will be forwarded to,
and then TCP routes the data through a network to guide the content to its final destination.

IP: For identification of sender and reciever
TCP: Do actual transmission between them.

Together they constructs a way of comminucation called TCP/IP
which is Internetet Network woks based on it.

## Network Protocol vs. Communication Protocol

Network management and communication protocols are two of the most important types of protocols.

Essentially, communication protocols including 
TCP/IP and HTTP 
are designed to enable two devices to exchange data, whereas 
network management protocols are designed to help manage and troubleshoot performance.

For example, 
network management protocols such as 
Simple Network Management Protocol (SNMP) can monitor and troubleshoot the connection between an endpoint and the network so that administrators can better understand the status and availability of infrastructure.

(port: udp 161 162)
* https://www.site24x7.com/help/admin/adding-a-monitor/configuring-snmp-linux.html
* https://www.techtarget.com/searchnetworking/definition/SNMP

In contrast, communication protocols are mainly concerned with defining formatting and syntax rules to set out a framework for two devices to exchange data with each other.

Below we’re going to look at nine types of network protocols that empower and drive modern networking.

## Transmission Control Protocol (TCP) A.K.A. Internet Protocol (IP)

Connection oriented transmission
Guaranty messages will be received in another side

TCP is a protocol that converts data into packets so that it can be sent between a server and a client.
(TCP doing Packetize transmission Unit)

Organizations use TCP to transfer content such as files, text, images and emails 
because it guarantees that the packets will be delivered accurately and in the correct order.

TCP protocol convert and segments files to units callled packets
atomit data unit in this protocol is packet

شیوه‌نامهٔ TCP فایل‌ها را به بسته‌های کوچکی به نام packet تقسیم می‌کند.

It’s worth noting that 
TCP will establish a connection between the origin and the destination devices 
before attempting to transfer data. 

## This three-way handshake is outlined briefly below:

*  The client or web browser sends to the destination server a Synchronize Sequence Number (SYN).
*  The destination server sends an acknowledgement message known as SYN-ACK.
*  The origin device receives the SYN-ACK message 
and generates an ACK (acknowledgement message), which finalizes the connection.

# User Datagram Protocol (UDP)

Connection less
Best effort

UDP is a communication protocol that’s designed to send packets from one device to another on a network. 
Many organizations use UDP as an alternative to TCP because it offers higher transfer speeds.

While this increase in speed comes at the cost of accuracy, UDP better supports video/audio streaming services, online games or voice-over-internet-protocol (VoIP) calls, which can handle some degree of data loss.

Data integrity in this model not matter.
loosing one or many bits in a video or voice streams not important for destination device.

Another key difference between the two is that UDP won’t attempt to establish a connection before sending packets on to the destination. At the same time, it also doesn’t guarantee the delivery of data to the other device.

## File Transfer Protocol (FTP)
Application:
Q: How to send a file over network?
A: By using FTP protocol


FTP is a network protocol that’s used to transfer files from one device to another over an unencrypted TCP/IP connection.(channel)

With FTP, a user can load up a web browser(ftp://) or FTP client such as FileZilla or FTP Voyager and send up to 2GB at once.

Many organizations use FTP because of its ability to send large files or lots of files at once in a way that’s fast and efficient. 

Unfortunately, this efficiency comes at the cost of security as FTP transmits all data in plain text.
(plain text not suitable word here. files may be in binary form. maybe raw suitable)

For this reason, many organizations opt to use a secure version of FTP called File Transfer Protocol Secure Sockets Layer (FTPS), which functions the same but uses SSL encryption to obscure the transferred data.
using a secure version of FTP, sftp add extra feature(security) to traditional ftp protocol.

## Hypertext Transfer Protocol (HTTP)

Widely used in WEB
Industry standard
HTTPS shaped our web

HTTP is a communication protocol that enables systems to communicate on the World Wide Web.

With HTTP, a client will send a hypertext message request to a web server asking for access to the resources needed to load a web page.
for example: get me first page of amazon.com
Type in a web brower address bar, destination webserver address

https://www.amazon.com/

The webserver hosting the content will then respond and enable the client to load all the necessary text, images and videos featured on the page. 

When webserver receives our client(web browser request message) process it, and if authorize and exists genreate appropriate response message and send back.

## HTTP’s request-response cycle is outlined briefly below:

### client side

* The client(web browser) sends an HTTP request message to the web server,
requesting access to the web page content.

### server side

* The web server processes the request message.
validate and prepare appropriate response.

* The web server sends a response message back, that includes the requested content(file) or web page.

### client side

* The client(web browser) receives the message and loads the content in the web browser for the end user to view.

---

There is also an encrypted version of HTTP called HTTPS, which uses SSL/TLS encryption method to encrypt requests and responses so they can’t be accessed by third parties.
To ensuring communication channel is secure by any unauthorize person apply ssl/tls method to traditionlal HTTP protocol,

### Web server examples:

* Apache 
* Oracle weblogic
* Nginx
* Microsoft IIS


## Simple Network Management Protocol (SNMP)

SNMP is an application layer protocol that’s used to collect management information from devices such as computers, routers, switchers, firewalls and printers.
(collects data from Host)

Network monitoring platforms often use SNMP to monitor the performance and status of devices throughout a network in real time.
Q: How to inform by devices in a Network?
(Uptime, Status, performance)
A: By using SNMP protocol.

The protocol works with an SNMP manager or software client sending SNMP GET requests to SNMP-enabled devices.

SNMP-enabled devices each have a local SNMP agent that collects performance data 
from the device and will forward this information to the SNMP manager 
so that a network administrator can get a top-down view of performance and status of each monitored devices.


# Internet Control Message Protocol (ICMP)

Communication

Q: How to fastly ensure a device exists and up in network?
A: By using ICMP protocol
(ping host device to see is it alive or not)

ICMP is a network communication protocol that devices use to warn about connectivity issues and errors. 

ICMP can notify devices that a forwarded message was too long or arrived out of order, and will issue an error message requesting that the device resend the content.

Troubleshooting tools such as Ping send ICMP requests to a device and measure the round-trip time, or the time it takes for the device to respond to the request. 

The amount of delay in the response can then be used to measure the quality of the connection.

Other tools such as traceroute use ICMP to troubleshoot and measure the efficiency of network routes, telling the user how much time it took to traverse from one device to another.

Sometimes, cybercriminals will use the protocol as part of an ICMP flood attack where they attempt to overwhelm a server with illegitimate ICMP requests to take its computing resources away from the end user.

### traceroute command


---

# Email protocols

# Post Office Protocol (POP)

POP3 is a network protocol that enables a server to retrieve emails from a remote server and download them to the local device. 

Whenever the client connects to the server via TCP, it automatically downloads all the new messages to it, making them accessible to the user both online and off-line.

Email platforms (client/agent) like Microsoft Outlook can use POP3 to collect email messages from remote servers via TCP/IP so that they’re available off-line.
(they download messages when online and save them)

Under the default setting, all emails are deleted from the server automatically once the download is complete, but the user can also configure it to store emails on the server for a certain time period.

# Internet Message Access Protocol (IMAP)

Newer one
Multiple device access to emails

IMAP is another protocol that’s used for retrieving emails. 

With IMAP, whenever a user clicks on an email, it isn’t downloaded or stored on their computer locally but remains on the remote server, enabling the user to check their email from multiple devices.

The main difference between IMAP and POP3 is that the latter only allows users to download and access emails locally on the same computer.
IMAP also doesn’t automatically delete emails from the server.


# Simple Mail Transfer Protocol (SMTP)

SMTP is a mail delivery protocol that allows a device to send and deploy email to a remote endpoint with a TCP connection.

Many providers including Microsoft Outlook, Gmail and Yahoo Mail use SMTP to send messages to remote servers.

Briefly, an organization will first create an SMTP server, which employees can connect to and communicate with via a mail user agent (MUA) or email client such as Gmail.

Through this connection, they can deliver emails to the SMTP server and other users.

Unlike POP3, SMTP cannot retrieve emails from a mailbox, and unlike POP3, it doesn’t automatically delete emails.


---


mail command in unix like
python client to access mail server
telnet to access mail server 
nc to check or realy connect?
python simple mail, server client with script


## Mail servers

Microsoft Exchange
Gmail, SaaS
Postfix 
self hosted mail server



# Resources 

## Based on this article

[9 Types Of Network Protocols & When To Use Them](https://www.forbes.com/advisor/business/types-network-protocols/)

## Other resources 

* https://en.wikipedia.org/wiki/Internet_protocol_suite


