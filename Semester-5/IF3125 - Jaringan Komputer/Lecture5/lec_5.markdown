---
title: "Protokol OSI dan TCP"
date: 2023-10-03 08:20:43
tags: [Jaringan Komputer]
categories: [Notes]
---

### Layer 7 Application 
---
Layer dimana user berinteraksi dengan network dan menyediakan service pada
jaringan.
Sebagai **interface** yang memungkinkan aplikasi saling berkomunikasi melalui
network.

### Layer 7 Presentation
---
Mendefinisikan bagaimana format data ditampilkan sehingga data yang dikirimkan
dapat dikenali oleh komputer. 
Biasanya metode yang digunakan pada layer presentation
1. Translasi: interoperabilitas antara metode encoding yang berbeda
2. Compression: kompresi data pada sisi pengirim dan dekompresi pada sisi
   penerima
3. Encrypion: enkripsi pada sisi pengirim dan deskripsi pada sisi penerima

### Peran Transport Laye
---
1. Mengtur komunikasi end-to-end
Setiap host bisa saja memiliki lebih dari 1 aplikasi yang memanfaatkan network
untuk proses komunikasi. Setiap aplikasi tersebut bisa saja berkomunikasi
dengan satu atau lebih aplikasi pada host lain.

2. Segmenting data
Pada umumnya network memiliki batas ukuran dalam satu PDU. Layer transport
bertanggung jawab untuk melakukan segmentasi data yang diterima dari layer
atas.

3. Resembling data
pada sisi penerima, transport layer memanfaatkan informasi yang ada pada header
untuk menyusun ulang segmen-segmen data yang utuh sebeluh diberikan ke layer
atas (apps)

4. Identifikasi aplikasi
agar data dapat disampaikan pada aplikasi yang tepat, layer transport harus
mengidentifikasi target yang dituju.

5. Multiplexing / Demultiplexing
1. Multiplexing: Bundle input dan beberapa sumber menjadi satu output tunggal.
2. Demultiplexing: Menerima input dari satu sumber dan mengirimkan dan
   mengirimkan pada beberapa output. 

### Pocket Number Socket Pair
---
The source and destination ports are placed within the segment
The segments are then encapsulated within an IP packet
The combination of the source IP address and source port number, or the
destination IP address and destination port number is known as a socket

### TCP Communation Process / TCP Server Processes
--
Each appliaction process running on a server is configured to use a port
number
- An indivdual server cannot have two services assigned to the same port number
    within the same transport layer of services.
- An active server application assigned to a specific port is considered open,
    which means that the transport layer accepts, and process segments
    addressed to that port.

### TCP Header
---
https://networklessons.com/cisco/ccie-routing-switching-written/tcp-header ->
Link (malas baca)

### TCP [3 Way Handshake]
---
3 way handshake menunjukan
1. Ada tidaknya mesin tujuan
2. Apakah mesin tujuan menjalankan aplikasi yang di request pada port tujuan
3. Client ingin menjalin komunikasi pada port tujuan

