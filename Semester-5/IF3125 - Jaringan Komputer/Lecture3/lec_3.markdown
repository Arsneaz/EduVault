---
title: "Review Protokol Jaringan"
date: 2023-09-12 08:01:46
tags: [Jaringan-Komputer]
categories: [Notes]
---

## Protokol Jaringan
---
* Protokol adalah sebuah kesepakaatn, aturan atau standar yang mengatur
    hubungan, komunikasi.
* Protokol yang mengatur agar komputer yang berbeda platform dapat saling
    mengirimkan informasi.
* Diterapkan pada perangkat keras, perangkat lunak maupun kombinasi dari
    keduanya.

## Model OSI (Open System Interconnection)
---
* *Open System* berati sekumpulan protokol yang memungkinan terjadinya
    komunikasi *antar sistem yang berbeda*.
* Model OSI berbentuk kerangka berlapis ( *layerd framework* ) untuk mendesain
    sebuah kerangka network. 
* Setiap layter mendefinisikan sekumpulan fungsi layanan yang berbeda sehingga
    memungkinkan komunikasidata melalui jaringan komputer.
* Dalam mesin yang berbeda, **layer yang sama** saling berkomunikasi
    (peer-to-peer communication) dan diatur oleh sebuah protokol.
* Terdapat pemisahan layer (Lapisan atas dan Lapisan bawah) yang digunakan
    sebagai Application(Application, Presentation, Session Layer) atau data transport(Transport, Network, Data Link, Physical).

### Penjelasan OSI Layer
1. Presentation
Layer dimana user berinteraksi dengan network. Menyediakan service-service pada
jaringan.
Contoh service adalah:
1. File Transfer
2. Mail Services
3. Directory Services
4. Web Services

2. Presentation
Mendefinisikan bagaimana format data ditampilkan sehingga data yang dikirimkan
dapat dikenali oleh komputer penerima
1. Compression : Komperesi data pada sisi pengirim dan dekompresi pada sisi
   penerima.
2. Encryption : Enkripsi pada sisi pengirim dan dekripsi pada sisi penerima.

We can look at example format data: jpg, ASCII.

3. Session
Mendefinisikan bagaimana menjalin, mengontrol, dan mengakhiri komunikasi antara
2 host.

4. Transport
Segmentasi data pada sisi pengirim dan menyatukannya kembali pada sisi
penerima, serta memastikan data sampai pada tujuan dengan urutan yang benar
(sequencing) dan terhindar dari error (error recovery).
Mendefinisikan *well-known* services (ports), such as:
- Port 80 to service http
- Port 21 to service ftp
- Port 22 to service ssh
- Port 25 to service smtp, dll

Terdapat fitur pada layer transport.
- Flow control
- Acknowledgement
- Re-transmission

Ada 2 tipe metode pengirima data:
- Reliable, Connection-oriented
- Unreliable, Connectionless

Bentuk data yang dikirim dalam bentuk **segment** atau **datagram**

5. Network
Menyediakan pengalamatan logic (IP Address) serta menemukan alur terbaik ke suatu
tujuan (Routing). Biasanya device yang mengirimkan adalah [Switch layer 3,
Router] dalam bentuk data **Pakcket**.

6. Data Link
Menyediakan pengalamatan fisik (MAC Address) serta mendeteksi error (error
detection) dengan **Frame Check Sequence** (FCS).
Biasanya dalam bentuk data **Frame**.

7. Physical
Mengatur bagaimana data diletakan dalam media komunikasi (kabel), serta
melakukan konversi bit-bit frame data link menjadi sinyal-sinyal elektronik
(encode) kemudian mengirimkan sinyal tersebut ke media fisik. serta
mendefinisikan fungsi dan prosedur agar transmisi data bisa terjadi.
Biasanya dalam bentuk data **Bits** (sequence of 0 and 1).

## TCP/IP 
---
* Standard yang dipakai internet saat ini. Merupakan sekumpulan protokol
    (Protocol Suite) komunikasi yang digunakan dalam internet.
    {Application, Transport, Internet, Physical}

### TCP Layer
1. Application
Menangani protokol high-level, isu-isu representatsi, encoding, dan kontrol
session. Menyediakan layanan (services) bagi software yang berjalan pada
komputer
Sebagai interface antara software yang berjalan pada komputer dengan network.

2. Transport
Meneydiakan services transport dari host pengirim ke penerima
Melakukan segmentasi data dari layer application pada sisi pengirim (encode) kemudian menysunnya kembali (decode) pad sisi penerima.
Terdiri dari 2 Protokol Utama
- Transmission Control Procotol (TCP)
- User Datagram Protocol (UDP)

3. Internet
Menyediakan pengalamatan logik (IP Address) serta menentukan proses routing.
- RARP (Address Resolutioon Protocol)
  Memungkinkan host menemukan internet address jika diketahui physical address.
- Internet Control Message Protocol (ICMP)
  Mekanisme yang digunakan host dan gateaway untuk mengirim notifikasi masalah
  datagram ke pengirim.
- Internet Group Message Protocol (IGMP)
  Digunakan untuk memudahkan transmisi simultan dari suatu message ke gropu
  penerima (Multicast)

4. Physical (Network Access)
Disebut sebagai layer host-to-host network.
Memformat data menjadi sebuah data yang disebut **frame**.
Mendefinisikan alamat fisik (MAC Address) untuk mengidentifikasi kartu jaringan
pada komputer pengirim dan penerima.

## Model OSI & TCP/IP
Model TCP/IP mendapat kepercayaan karena protol-protokol yang dimilikinya.
Sebaliknya, model OSI yang tidak digunakan untuk membangun jaringan komputer.
Model OSI digunakan sebagai panduan untuk memahami proses komunikasi yang
terjadi pada jaringan.
