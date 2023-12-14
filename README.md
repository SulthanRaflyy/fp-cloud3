# **Final Project Teknologi Komputasi Awan** 
## Kelas D 

### Kelompok 3 


| Nama | NRP |
|---------------------------|------------|
| Andyana Muhandhatul Nabila | 5027211029 |
| Kevin Putra Santoso | 5027211030 |
| Andana Satrio Herdiansyah | 5027211031 | 
| Bagus Cahyo Arrasyid | 5027211033 |
| Sulthan Akmal Rafliansyah | 5027211039 |
| Ridho Husni Indrawan | 5027211043 |

## Pendahuluan 
Dalam rangka memenuhi penilaian pada mata kuliah teknologi komputasi awan. Pada penilaian akhir semester diberikan tugas final project yang telah diberikan oleh dosen pengampu Bapak Fuad Dary Rosyadi, S.Kom., M.Kom. Seluruh mahasiswa yang mengambil mata kuliah teknologi komputasi awan yang dibagi menjadi beberapa kelompok setiap kelasnya yang beranggotakan 4- 5 orang. Kelompok ini sama dengan kelompok tugas presentasi kelas sebelumnya. Pada tugas ini mencakup capaian pembelajaran mata kuliah mahasiswa mampu memahami dan menerapkan berbagai servis pada layanan awan dan mahasiswa mampu merancang dan mengaplikasikan teknologi komputasi awan.

Berikut ini adalah final project mata kuliah teknologi komputasi awan. Sebagai seorang lulusan Teknologi Informasi dengan keahlian di bidang pengembangan aplikasi berbasis komputer dan manajemen layanan awan, saya memiliki kemampuan yang mumpuni untuk merancang, membangun, dan mengelola solusi teknologi informasi yang inovatif. Seiring dengan perkembangan teknologi, penting bagi kita untuk terus beradaptasi dan memanfaatkan peluang bisnis yang muncul di era digital.

Dalam konteks ini, saya memiliki kesempatan untuk berkolaborasi dalam proyek digital marketing yang menarik. Sebuah aplikasi berbasis API telah diberikan kepada saya dengan spesifikasi yang menarik, bertujuan untuk mempermudah pengelolaan pesanan dalam bisnis digital marketing ini.

Aplikasi ini menyediakan beberapa endpoint penting, termasuk pengambilan seluruh pesanan, pengambilan detail pesanan berdasarkan ID, pembuatan pesanan baru, pembaruan pesanan, dan penghapusan pesanan. Seluruh proses ini terintegrasi dengan MongoDB, dengan konfigurasi database yang memadai untuk mendukung pengelolaan data pesanan. Berikut rincian spesifikasi endpoint yang ditentukan : 
1. Get All Orders:
   - Endpoint: `GET /orders`
   - Deskripsi: Mendapatkan daftar seluruh pesanan.
2. Get a Specific Order by ID:
   - Endpoint: `GET /orders/<order_id>`
   - Deskripsi: Mendapatkan detail pesanan berdasarkan ID.
3. Create a New Order:
   - Endpoint: `POST /orders`
   - Deskripsi: Membuat pesanan baru.
4. Update an Order by ID:
   - Endpoint: `PUT /orders/<order_id>`
   - Deskripsi: Memperbarui pesanan yang sudah ada.
5. Delete an Order by ID:
   - Endpoint: `DELETE /orders/<order_id>`
   - Deskripsi: Menghapus pesanan berdasarkan ID.

MongoDB Configuration:
- Database: `orders_db`
- Connection URI: `mongodb://localhost:27017/orders_db`

Dengan adanya proyek ini, kita memiliki peluang untuk meningkatkan efisiensi bisnis, meningkatkan pengalaman pelanggan, dan mengoptimalkan proses manajemen pesanan melalui aplikasi yang telah disediakan. Proposal ini akan merinci rancangan arsitektur cloud untuk mendukung aplikasi ini, serta langkah-langkah instalasi, implementasi, dan uji coba kinerja menggunakan Locust. Rancangan arsitektur cloud akan mencakup estimasi harga yang diperlukan untuk mendukung infrastruktur tersebut, yang nantinya akan dijelaskan dalam presentasi diskusi pada minggu ke-15.


## Rancangan Arsitektur
![ArsitekturCloud_New](https://github.com/SulthanRaflyy/fp-cloud3/assets/103870239/a6506507-ad69-48e8-afe7-6517b8402a07)

| No. | Kebutuhan | Spesifikasi | Harga |
|----|-------------------------|-----------------------------------------|-------|
| 1 | Database | 1vCPU, 2GB RAM | $8 |
| 2 | Load Balancer | 2vCPU, 2GB RAM | $18 |
| 3 | Worker 1 | 2vCPU, 2GB RAM | $18 |
| 4 | Worker 2 | 2vCPU, 2GB RAM | $18 |
| 5 | Worker 3 | 2vCPU, 2GB RAM | $18 |
| 6 | Worker 4 | 2vCPU, 2GB RAM | $18 |
| 7 | Worker 5 | 2vCPU, 2GB RAM | $18 |
| | | **Total** | **$62** |

## Implementasi

**[Nunggu Konfirmasi Bagyo]**


## Analisis Pengujian
### Analisis Hasil Pengujian
#### 1. Pengujian A
- Number of User = 1
- Spawn Rate = 25
- Runtime = 60s
![nu1sr25](https://github.com/SulthanRaflyy/fp-cloud3/assets/103870239/2f206f24-b0a3-452a-8600-169a83876d6f)

**Analisis**
- Tidak ada kegagalan dalam permintaan GET atau POST.
- Waktu rata-rata respons GET relatif tinggi, yang menunjukkan bahwa waktu yang dibutuhkan untuk memperoleh respons dari server cukup lambat.
- Permintaan POST memiliki waktu respons yang jauh lebih cepat dibandingkan dengan permintaan GET.

#### 2. Pengujian B
- Number of User = 1
- Spawn Rate = 50
- Runtime = 60s
![nu1sr50](https://github.com/SulthanRaflyy/fp-cloud3/assets/103870239/2de7b9d2-2be1-479e-89b4-6b0a05158c81)

**Analisis**
- Sama seperti pengujian sebelumnya, tidak ada kegagalan.
- Waktu rata-rata respons untuk permintaan GET dan POST lebih rendah dibandingkan dengan pengujian pertama.
- Distribusi waktu respons menunjukkan peningkatan kinerja, dimana waktu rata-rata respons menurun untuk kedua metode.

#### 3. Pengujian C
- Number of User = 1
- Spawn Rate = 100
- Runtime = 60s
![nu1sr100](https://github.com/SulthanRaflyy/fp-cloud3/assets/103870239/631a85e8-066a-41c8-8d1d-d6df5327a608)

**Analisis**
- Tidak ada kegagalan yang tercatat.
- Waktu rata-rata respons GET dan POST stabil dan konsisten dengan pengujian kedua.
- Tidak ada perubahan signifikan dalam waktu respons yang menunjukkan bahwa server menangani permintaan dengan konsistensi.

#### 4. Pengujian D
- Number of User = 1000
- Spawn Rate = 1000
- Runtime = 60s
![nu1000sr1000](https://github.com/SulthanRaflyy/fp-cloud3/assets/103870239/9aa88636-fabd-4299-a269-1936f680e074)

**Analisis**
- Tidak ada kegagalan yang tercatat meskipun ada peningkatan besar dalam jumlah pengguna dan laju spawn.
- Waktu rata-rata respons untuk permintaan GET meningkat secara dramatis, menunjukkan bahwa server mungkin mengalami kesulitan dalam menangani permintaan bersamaan dalam jumlah besar.
- Permintaan POST juga menunjukkan peningkatan waktu respons tetapi tidak sebesar permintaan GET.

### Analisis Keseluruhan
- Secara keseluruhan, server tampaknya dapat menangani permintaan dengan baik tanpa kegagalan ketika diuji dengan 1 pengguna dengan laju spawn yang meningkat dari 25 hingga 100.
- Namun, ketika diuji dengan 1000 pengguna dengan laju spawn yang sama dengan jumlah pengguna, kinerja server menurun secara signifikan, khususnya untuk permintaan GET, yang bisa jadi indikator bahwa server mungkin tidak cukup kuat untuk menangani beban tinggi pengguna bersamaan.

## Kesimpulan

**[Nunggu Implementasi]**


