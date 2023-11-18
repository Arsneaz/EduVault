## 📚 TCP / IP

**Author:** Ceb  
**Date:** November 18, 2023

### TCP/IP Model
<p align="center">
  <img width="460" height="300" src="https://github.com/Arsneaz/EduVault/assets/96061442/b44138b5-6229-4d61-ad30-825f3ce48017">

### Application Layer
Application Layer adalah _interface_ yang berjalan antara software pada komputer dengan network dan bertuas menangani protokol high-level dan menyediakan layanan bagi software yang berjalan pada komputer    
1. **Telnet**    
   Program yang memungkinkan akses terminal secara remote lewat suatu jaringan (Port 23)
2. **SMTP (Send Mail Transfer Protocol)**    
   Suatu protokol aplikasi yang merupakan sistem pengiriman _message_ (pesan atau email) (Port 25)
3. **POP (Post Office Protocol Ver 3)**    
   Protokol untuk mengambil / menerima pesan (Port 110)
   FTP (File Transfer Protocol)
4. **FTP (File Transfer Protocol)**    
    Protokol sekaligus program yang dapat digunakan untuk
    melakukan operasi file dasar pada host remote dan untuk
    mentransfer file antar host (port 21, 20)
6. **TFTP (Trivial Transfer Protocol)**    
   Protokol yang dipasang pada boot ROM komputer. Digunakn
    untuk men-download software operating system utama saat
    melakukan boot system pada jaringan.

### Transport Layer
Menyediakan service transport dari host pengirim ke penerima, serta melakukan _segmentasi_ data dari layer application pada sisi pengirim kemudian menyusunnya kembali pada sisi penerima. Terdiri dari 2 Protokol Utama:
1. Transmission Control Protocol (TCP)
2. User Datagram Protocol (UDP)

### TCP Segments
vTCP Segment terdiri dari dua bagian
1. TCP Packet Header yang, panjangnya 20 Bytes
2. TCP Data, yang tidak boleh lebih dari **Maximum Segment Size (MSS) Bytes**

### TCP Three-Way Handshake
Untuk membuat koneksi TCP yang stabil, kita membutuhkan Three-Way Handshake untuk koneksi antara dua perangkat di dalam jaringan. Hal ini memastikan metode yang digunakan untuk memastikan bahwa _sender_ dan _receiver_ siap dalam _data transfer_
1. **SYN (Synchronize)**    
    The process begins with the client (initiating device) sending a TCP packet with the SYN flag (synchronize) set to the server   (responding device). This packet indicates an intention to establish a connection and includes an initial sequence number.
2. **SYN-ACK (Synchronize-Acknowledge)**    
   Upon receiving the SYN packet, if the server is willing to establish a connection, it responds with a TCP packet that has both the SYN and ACK (acknowledge) flags set. The acknowledgment number is set to one more than the received sequence number.
3. **ACK (Acknowledge)**    
    Finally, the client acknowledges the server's response by sending a TCP packet with the ACK flag set. The sequence number is set to one more than the received acknowledgment number.

Pada tahap ini, _Three-Way Handshake_ sudah selesai dan koneksi yang stabil telah didapatkan antara _client_ dan _server_
<p align="center">
  <img width="460" height="300" src="https://github.com/Arsneaz/EduVault/assets/96061442/5dfe9c70-e3af-4052-99cc-e4a9a3d8f1a0">
</p>

### TCP Retransmission
ARQ (Automatic Repeat Request) adalah sebuah teknik untuk mengatasi kesalahan (error) atau kehilangan frame dengan mentransmisikan ulang frame tergantung metode yang diambil:
- Stop-and-wait
- go-back-N
- Selective repeat
Parameter yang digunakan untuk menetukan error atau tidaknya pada sebuah pengiriman data adalah **ACK** dan timeout-nya
<p align="center">
  <img width="460" height="300" src="https://github.com/Arsneaz/EduVault/assets/96061442/399092ff-2f6b-47d1-832b-d5d87845cbb6">
</p>

<p align="center"> Jenis Protokol yang digunakan </p>
<p align="center">
  <img width="460" height="300" src="https://github.com/Arsneaz/EduVault/assets/96061442/0cc3d4c7-c981-433b-913f-928e46f79cd5">
</p>
<p align="center">
  <img width="460" height="300" src="https://github.com/Arsneaz/EduVault/assets/96061442/c5e09330-652e-4d21-a478-95340ce344ab">
</p>
<p align="center">
  <img width="460" height="300" src="https://github.com/Arsneaz/EduVault/assets/96061442/b38d7e9d-c3bd-428b-8c32-f35b769c4437">
</p>

### Port
Port dapat mengidentifikasi aplikasi dan layanan yang menggunakan koneksi di dalam jaringan TCP/IP. Port dapat dikenali dengan 16-bit angka yang disebut sebagai **Port Number** dan diklasifikasikan dengan jenis protokol transport apa yang digunakan, kedalam **Port TCP** dan **Port UDP**. Maximum port untuk transport adalah **65,538** (2^16 - 1).    
Port dikategorikan menjadi 3 
1. **Well-known ports (0-1023)**: These are reserved for system services and commonly used applications. For example, HTTP typically uses port 80, and HTTPS uses port 443.
2. **Registered ports (1024-49151)**: These ports can be registered with the Internet Assigned Numbers Authority (IANA) for specific services but are available for general use. They are used by applications that aren't as common as those using well-known ports.
3. **Dynamic or private ports (49152-65535)**: These are also known as ephemeral ports. They are used by client applications for communication with servers. When a client initiates a connection to a server, it typically uses a dynamically assigned ephemeral port for that particular session.
   
In the context of TCP and UDP, the combination of an IP address and a port number uniquely identifies a specific endpoint in a network. For example, in the address "192.168.0.1:8080," 192.168.0.1 is the IP address, and 8080 is the port number. This allows multiple network services on a single device to operate independently, as each service can use a different port.

### Internet Layer
Menyediakan pengalamatan logic (IP Address) sehingga setiap komputer memiliki IP address yan berbeda (unik), serta menentukan proses _routing_ sehingga router dapat menentukan kemana paket harus dikirimkan agar sampai ke tujuan.    
Di dalam conteks dari Internet Layer dari TCP/IP Model, terdapat beberapa protokol di dalam Internet Layer: 
1. **Internet Protocol**, IP is a fundamental protocol in the Internet layer responsible for logical addressing and routing. It provides a unique IP address to each device on a network and enables the delivery of data packets from the source to the destination across interconnected networks.
2. **Address Resolution Protocol (ARP)**, ARP is used for mapping a known IP address to a MAC (Media Access Control) address in a local network. When a device wants to communicate with another device on the same network, it needs to know the MAC address corresponding to the IP address. ARP is the protocol that helps in this mapping process.
3. **Internet Control Message Protocol (ICMP)**, ICMP is a network layer protocol used for sending error messages and operational information about network conditions. It is often employed by network devices, such as routers, to communicate error conditions or provide diagnostic information. ICMP includes the familiar "ping" command, which is widely used for network testing and troubleshooting.
4. **Internet Group Management Protocol (IGMP)**, IGMP is used by hosts and adjacent routers on a network to establish multicast group memberships. It is particularly relevant for managing multicast group communication, where data is sent from one sender to multiple recipients.
5. **Internet Protocol Version 6 (IPv6)**, IPv6 is the next generation of the Internet Protocol and is designed to replace IPv4. It provides a larger address space, improved security features, and additional enhancements compared to IPv4. As the world transitions to IPv6, it coexists with IPv4 to facilitate the smooth transition

### Physical Layer / Network Access
Disebut juga sebagai layer _host-to-network_. Protokol-protokol LAN dan WAN berada pada layer ini. Melakukan formatting data menjadi sebuah unit **Frame**.
Mendefinisikan pengalaman fisik (**Mac Address**) untuk mengindentifikasi kartu jaringan komputer pengirim dan penerima. Serta melakukan error pada frame yang diterima (_error-conncetion / error checking_).



