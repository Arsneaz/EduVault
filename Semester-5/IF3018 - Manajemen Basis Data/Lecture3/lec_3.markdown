---
title: "Performace Turing: Schema Turing"
date: 2023-09-15 13:36:57
tags: [Manajemen Basis Data]
categories: []
---

More additional notes later

## Overview
---
* Setelah desain ER, penyempurnaan skema dan definisi pandangan

Kita harus mulai dengan memahami *beban kerja*
1. Per

## Understanding the Workload
---
* Untuk setiap Query dalam workload:
1. Relasi mana yang diaksesnya?
2. Atribut mana yang diambil?
3. Atribut mana yang terlibat dalam kondisi seleksi/penggabungan? Seberapa
   selektiflah kondisi itu.

* Untuk seitap pembaruan dalam beban kerja:
1. Atribut mana yang terlibat dalam kondisi seleksi/penggabungan? Seberapa
   selektifkah kondisi itu?
2. Jenis pembaruan (INSERT/DELETE/UPDATE), dan atribute yang terpengaruh.

## Decision
---
* Indeks apa yang harus dibuat? (Relasi mana yang harus memiliki indeks, serta
    bidang apa yang harus menjadi kunci pencarian)
* Untuk seiap indeks, indeks apa yang harus digunakan? (Hash/pohon?
    Dinamis/Statis? Padat/Jarang)
* Pertimbangkan skema konseptual
1. Pertimbangkan skema alternatif yang dinormalisasi? (Ingat, ada banyak
   pilihan dalam menguraikan menjadi BCNF, dll)
2. Haruskan kita membatalkan beberapa langkah dekomposisi dan memilih bentuk
   normal yang lebih rendah (Denormalisasi)
3. Partisi horizontal, replikasi dan tampilan.

## Tuning the Conceptual Schema
---
* Pilihan skema konseptual harus dipandu oleh beban kerja. Selain masalah
    redudansi:
1. Kita mungkin mempertimmbangkan dekomposisi horizontal
2. Kita mungking mempertimbangkan dekomposisi vertikal
3. Kita mungkin lebih memilih skema skema 3NF dariapda BCNF
4. Kita mungkin melakukan dernomalisasi (membatalkan langkah dekomposisi atau
   kita dapat menambahkan field ke suatu relasi)
Jika perubahan tersebut dilkaukan setelah database digunakan, disebut evolusi
skema; mungkin menutupi perubahan dengan mendefinisikan views

## Schema Tuning
---
* Dapat dilakukan dengan beberapa
1. Memisahkan tabel
Terkadang memisahkan tabel yang dirnomalisasi dapat meningkatkan kinerja.
dapat membagi tabel dengan dua cara
1. secara horzontal (membagi jumlah kolom row data)
2. secara vertikal (membagi jumlah attribute)

2. Denormalisasi
1. Menambahkan kolom yang berlebihan
2. Menambahkan atribute yang turunan
3. Tabel yang runtuh
4. Mennggandakan tabel

## Splitting Horizontal
---
* Menempatkan baris dalam dua tabel terpisah, bergantung pada nilai data dalam
    satu atau lebih baris
* Gunakan pemisahan horizontal jika
1. Tabel berukuran besar, dan untuk memperkecil ukurannya akan mengurangi
   jumlah halaman indeks yang dibaca dalam kueri
2. Pemmisahan tabel berkaitan dengan pemisahan baris secara alami, seperti
   situs geografis yang berbeda atau data historis vs data terkini
3. Pemisahan tabel mendistribusikan tabel dalam penyimpanan fisik.

## Spliting Vertical
---
* Relasi partisi untuk mengisolasi data yang paling sering diakses - hanya
    mengambil informasi yang diperlukan.
* Menjaga relasi dalam bentuk normal
* Gunakan pemisahan vertikal jika
1. Beberapa kolom diakses lebih sering dibandingkan kolom lainnya
2. Tabel memiliki baris yang  lebar, dan pemisahan tabel akan mengurangi jumlah
   halaman yang perlu dibaca.

## Denormalisasi
---
* Dapat dilakukan dengan tabel atau kolom
* Mengasumsikan normalisasi sebelumnya
* Membutuhkan pengetahuan menyeluruh tetang bagaimana data digunakan.


## Tabel Runtuh /  Collapsing Tables
---
* Jika sebagian besar pengguna perlu melihat sekumpulan data gabungan lengkap
    dari dua tabel, mencitukan kedua tabel menjadi satu dapat meningkatkan
    kinerja dengan menghilangkan penggabungan

