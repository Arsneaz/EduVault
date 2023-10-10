![image](https://github.com/Arsneaz/EduVault/assets/96061442/611d9d2b-779e-4f6f-9c93-27bda816caba)![image](https://github.com/Arsneaz/EduVault/assets/96061442/2fc5f82c-dae8-4efe-a0ab-c821b52d8be1)---
title: "Physical Layer"
date: 2023-10-09 21:19:25
tags: []
categories: []
---

### Physical Layer
---
Komponen fisik yang terdiri dari perangkat keras, media dan konektor lr lainnya
yang berfungsi untuk mentransmisikan data.

Pada lapisan transmitter : menerapkan fungsi elektris, mekanis, dan prosedur
untuk membangun dan mentransmisikan data biner.
Pada sisi receiver: menerima data dan mengirimkannya ke layer atasnya

* Encoding
---
Encoding merubah bits menjadi format yang dikenali oleh perangkat keras dalam jaringan.

![image](https://github.com/Arsneaz/EduVault/assets/96061442/3745a232-fafd-469d-b0cf-cf692a035fe1)
![image](https://github.com/Arsneaz/EduVault/assets/96061442/5e5b5ebc-2636-4dbc-b044-14ce12b5caed)
![image](https://github.com/Arsneaz/EduVault/assets/96061442/e8f95ac9-9eff-4fb9-83a4-dbcc1125f017)
![image](https://github.com/Arsneaz/EduVault/assets/96061442/47c06399-b3c0-4b2a-a6ff-de593688f6d4)
![image](https://github.com/Arsneaz/EduVault/assets/96061442/36469da9-ed67-43ba-bb1a-d8ae36911c06)

### Data Link Layer
---
1. Menjadi penyedia layanan interface baik bagi network layer
2. Penentuan pengelompokan bit dari physical layer ke dalam frame
3. Menangani masalah error transmisi
4. Pengaturan aliran frame

Data di enkapsulasi oleh layer link dengan header dan trailer untuk membentuk sebuah frame (data link frame terdiri dari tree parts).
- Header
- Data
- Trailer

Jumlah informasi yang dibawa dari frame bervariasi bergantung pada hak akses informasi dan topologinya.

### Tugas Dari Data-Link Layer
1. Error Control
Data bisa mengalami error pada saat proses pengiriman, error control bertujuan untuk menangani bila ada kerusakan data.
![image](https://github.com/Arsneaz/EduVault/assets/96061442/afbeed6c-a3b7-4f3d-8f03-57f9ce68e971)
2. Error Detection
![image](https://github.com/Arsneaz/EduVault/assets/96061442/f25aecd0-6c07-49c7-8796-91a114840f51)
3. Flow Control
![image](https://github.com/Arsneaz/EduVault/assets/96061442/a5f5616f-9416-4812-9e39-fe8490593fa3)
4. Addressing
![image](https://github.com/Arsneaz/EduVault/assets/96061442/69236a47-a455-4bef-90e7-6058eb38317e)

### Jenis Filtering
---
1. Stataic Packet Filtering: Jenis filter yang di implementasikan pada kebanyakan router, dimana modifikasi terdapat aturan-aturan filter yang harus dilakukan secara mineral.
![image](https://github.com/Arsneaz/EduVault/assets/96061442/63174ade-7c4a-4959-af11-c8b15f3063c0)
2. Dynamic Packet Filtering: apabila proses-proses tertentu disisi luar jaringan dapat merubah aturan filter.
![image](https://github.com/Arsneaz/EduVault/assets/96061442/16d2c3cf-955b-48a8-b44d-cbfca295c9ce)







