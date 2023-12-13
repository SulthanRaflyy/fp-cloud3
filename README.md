# Final Project Teknologi Komputasi Awan 
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


## Rancangan Arsitektur

**[Inser Picture Here!]**

| No. | Kebutuhan | Spesifikasi | Harga |
|----|-------------------------|-----------------------------------------|-------|
| 1 | Database | 1vCPU, 2GB RAM | $8 |
| 2 | Load Balancer | 2vCPU, 2GB RAM | $18 |
| 3 | Worker 1 | 2vCPU, 2GB RAM | $18 |
| 4 | Worker 2 | 2vCPU, 2GB RAM | $18 |
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


