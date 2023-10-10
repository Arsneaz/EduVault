## Lecture 5: Query Processing
Nama : 
1. Arsyadana Estu Aziz (121140068)
2. Ardoni Yeriko Rifana Gultom (121140141)
3. M Rizki Alfaina (121140228)

### Parsing and Translation
Melakukan check syntax and grammar, validasi ralsi yang digunakan
Mengubah query/SQL ke dalam bentuk yang bisa diolah oleh Query Processing Engine dalma bentu aljabar relasi

### Optimation
Membuat evaluation plan yang optimal (dengan cost yang rendah)

### Evaluatoins
Pemilihan query-evaluation plan terbaik (cost), merupakan eksekusi terhadap query tersebut yang menghasilkan jawaban query

### Estimation Quary Cost
Biaya evaluasi dapat diukur dari banyaknya sumber daya sistem yang digunakan (misalkan; CPU time usage). Strategi yang dipilih dalam evaluasi query tergantung pada estimasi biaya dari masing-masing strategi yang ada. 
 
### Operasi Seleksi
Dalam pemrosesan query file scan merupakan operasi paling dasar dalam pengaksesan data. Penelusuran ini menggunakan algoritma pencarian untuk menemukan dan mengambil record data.

Operasi penghilangan duplikasi data dengan cara mengurutkan record terlebih dahulu, maka data yang sama akan berada di baris yang sama.

### Evaluasi Ekspresi
Mengevaluasi query bagian per bagian secara berurutan.
- Materialisasi 
  Menampung hasil operasi menggunakan tabel temporer yang kemudian dgunakan untuk level berikutnya.
- Pipeline
  Mengganti tabel temporer dengan suatu pipeline operasi (berupa buffer). Penggunaan pipeline akan menghilangkan biaya pembacaan dan penulisan tabel-tabel temporer.
---

### Query Processing
Mengacu pada serangkaian aktivitas yang terlibat dalam mengekstraksi data dari database. Kegiatannya mencakup penerjemahan kueri dalam bahasa database tingkat tinggi ke dalam ekspresi yang dapat digunakan pada tingkat fisik sistem file.

Sebelum *Query Processing* dilakukan, sistem harus mengubah *query* menjadi bentuk yang lebih bisa digunakan untuk sistem seperti 
1. *Parsing and translation*
2. *Optimization*
3. *Evaluation*.
Sistem merubah representasi *parse-tree query* yang akan diubah kembali menjadi ekspresi aljabar-relasi.
(Kebnayakan *compiler* mengurus parsing secara otomatis kepada user).

### Measures of Query Cost
Terdapat beberapa kemungkinan evaluasi untuk setiap *query*, dan sangat penting untuk membandingkan alternatif, sehingga memperhitungkan cost untuk menemukan cost terbaik. 
 
Query Cost dapat diukur dengan pengaksesan disk CPU Time dan pendistribusian ke database sistem. Pada database yang besar, penting untuk melakukan optimasi agar kecepatan pengaksesan disk lebih baik dari awal dengan menggunakan number of block transfer dari disk untuk menghitung cost dari query-evaluation plan. Jika subsistem disk mengambil rata-rata dari t_r detik untuk transfer blok data, dan mempunyai rata-rata waktu akses blok dari t_s detik, kemudian operasi transfer b blok dan perform S seek akan mengambil b * t_r + S * t_s detik.

Waktu respon untuk rencana evaluasi kueri, dengan asumsi tidak ada aktivitas lain yang terjadi di komputer, akan memperhitungkan semua biaya ini, dan dapat digunakan sebagai ukuran dari biaya rencana. Sayangnya, waktu respon suatu rencana sangat sulit diperkirakan tanpa benar-benar melaksanakan rencana tersebut, karena alasan berikut :
1. Waktu respon bergantung pada isi buffer saat kueri mulai dieksekusi; informasi ini tidak tersedia ketika kueri dioptimalkan, dan sulit untuk diperhitungkan meskipun tersedia.
2. Dalam sistem dengan banyak disk, waktu respon bergantung pada bagaimana akses didistribuskan diantara disk, yang sulit diperkirakan tanpa pengetahuan rinci tentang tata letak data pada disk. 