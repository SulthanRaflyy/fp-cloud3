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

Implementasi projek menggunakan penyedia platform awan https://www.digitalocean.com/ dengan setting akun github student pack yang mendapatkan kredit sebesar $200 selama satu tahun. Berikut merupakan langkah-langkah implementasi:
1. Akses https://www.digitalocean.com/  dan Login menggunakan akun github student pack

[![1.jpg](https://i.postimg.cc/vmj3kX4V/1.jpg)](https://postimg.cc/PLWW8WzX)

2. Setelah masuk pada halaman awal DigitalOcean kita membuat Project baru pada bagian navbar kiri layar dan mengisi nama dan tujuan pembuatan project.

[![2.jpg](https://i.postimg.cc/3JHb3Lnj/2.jpg)](https://postimg.cc/mh8SwSxh)

3. Selesaikan pembuatan project dan buka project tersebut, melakukan pembuatan VM dengan mengklik tombol create pada bagian atas project. Droplets digunakan untuk membuat Load Balancer dan Worker sedangkan Database digunakan sebagai Database atau tempat menyimpan data.

[![3.jpg](https://i.postimg.cc/ZKFsnrMG/3.jpg)](https://postimg.cc/BXbBw1sp)
		
4. Pembuatan Droplets dan Load balancer diawali dengan pemilihan area Cloud VM, dilanjut menentukan OS yang akan digunakan, kemudian memilih konfigurasi yang sesuai permintaan disertai dengan penambahan akses keamanan, dan finalisasi pembuatan berupa penamaan dan kuantitas Droplets juga pembayaran.

[![4.jpg](https://i.postimg.cc/zvTtnWXR/4.jpg)](https://postimg.cc/K3vDb1TZ)

[![5.jpg](https://i.postimg.cc/VkfGCJyd/5.jpg)](https://postimg.cc/qzFxfMvT)

[![6.jpg](https://i.postimg.cc/hGh22Ntn/6.jpg)](https://postimg.cc/3y5jRSGf)

[![7.jpg](https://i.postimg.cc/P5S6zdhK/7.jpg)](https://postimg.cc/hX7bKWX7)

[![8.jpg](https://i.postimg.cc/q7759zQ9/8.jpg)](https://postimg.cc/ZW1HNYGc)

5. Pembuatan Database VM diawali dengan pemilihan area dari penyedia Cloud DB, dilanjut pemilihan jenis dari Database, kemudian melakukan pemilihan konfigurasi DB dan yang terakhir finalisasi pembuatan berupa penamaan dan kuantitas DB juga pembayaran.

[![9.jpg](https://i.postimg.cc/MTC3MtxS/9.jpg)](https://postimg.cc/wykQnX7f)

[![10.jpg](https://i.postimg.cc/43FSZsSn/10.jpg)](https://postimg.cc/gw8DHFdP)

[![11.jpg](https://i.postimg.cc/K8xVD9Tc/11.jpg)](https://postimg.cc/PPV2tQK0)

6. Setelah selesai maka akan muncul Droplets dan Database yang sudah dibuat disertai keterangan IP pada masing-masing Droplets

[![12.jpg](https://i.postimg.cc/4NzqtCmF/12.jpg)](https://postimg.cc/SJxgFvLW)

7. Melakukan setup Worker Droplets, dapat melalui web console atau menggunakan ssh via terminal perangkat lokal. Jika menggunakan ssh harus memiliki kredensial keamanan yang telah diatur saat pembuatan (SSH Key / Password). Format ssh root@<IPDroplets> kemudian masukkan kredensial keamanan sebelumnya

[![13.jpg](https://i.postimg.cc/pVj6bNYX/13.jpg)](https://postimg.cc/w36VLGGS)

8. Pada Worker Droplet setup dengan membuat file app.py dengan command nano app.py dan mengcopy-paste kode dibawah:
```   
from flask import Flask, jsonify, request
from flask_pymongo import PyMongo
from bson import ObjectId

app = Flask(__name__)

# Configuration for MongoDB
app.config['MONGO_URI'] = 'mongodb://localhost:27017/orders_db'
mongo = PyMongo(app)

# Routes

# Get all orders
@app.route('/orders', methods=['GET'])
def get_orders():
    orders = mongo.db.orders.find()
    orders_list = []
    for order in orders:
        order['_id'] = str(order['_id'])  # Convert ObjectId to string
        orders_list.append(order)
    return jsonify({"orders": orders_list})

# Get a specific order by ID
@app.route('/orders/<string:order_id>', methods=['GET'])
def get_order(order_id):
    order = mongo.db.orders.find_one({'_id': ObjectId(order_id)})
    if order:
        order['_id'] = str(order['_id'])  # Convert ObjectId to string
        return jsonify({"order": order})
    else:
        return jsonify({"message": "Order not found"}), 404

# Create a new order
@app.route('/orders', methods=['POST'])
def create_order():
    data = request.json
    new_order = {
        'product': data['product'],
        'quantity': data['quantity'],
        'customer_name': data['customer_name'],
        'customer_address': data['customer_address']
    }
    result = mongo.db.orders.insert_one(new_order)
    new_order['_id'] = str(result.inserted_id)  # Convert ObjectId to string
    return jsonify({"message": "Order created successfully", "order": new_order})

# Update an order by ID
@app.route('/orders/<string:order_id>', methods=['PUT'])
def update_order(order_id):
    data = request.json
    updated_order = {
        'product': data.get('product'),
        'quantity': data.get('quantity'),
        'customer_name': data.get('customer_name'),
        'customer_address': data.get('customer_address')
    }
    mongo.db.orders.update_one({'_id': ObjectId(order_id)}, {'$set': updated_order})
    updated_order['_id'] = order_id
    return jsonify({"message": "Order updated successfully", "order": updated_order})

# Delete an order by ID
@app.route('/orders/<string:order_id>', methods=['DELETE'])
def delete_order(order_id):
    result = mongo.db.orders.delete_one({'_id': ObjectId(order_id)})
    if result.deleted_count > 0:
        return jsonify({"message": "Order deleted successfully"})
    else:
        return jsonify({"message": "Order not found"}), 404

if __name__ == '__main__':
    app.run(host=’0.0.0.0’)
```
9. Setelah itu save program dan melakukan instalasi requirement untuk file app.py yang akan dijalankan yaitu python3, pip, pip flask dan pip flask-pymongo
10. Selanjutnya setup database, saat mengklik database vm maka akan muncul Connection Details yang digunakan untuk menghubungkan worker dengan database dengan format public network dan flag pada bagian atas, user:do-admin dan <namaDB> pada bagian bawah setting koneksi. Jangan lupa memasukkan URl mongoDB tersebut ke dalam konfig app.py pada worker. Apabila belum memiliki database maka disarankan untuk membuat database terlebih dahulu 

[![14.jpg](https://i.postimg.cc/W18yWMmG/14.jpg)](https://postimg.cc/hXJMhQ5v)

[![15.jpg](https://i.postimg.cc/hjz3t6ks/15.jpg)](https://postimg.cc/2bYxHc8L)

12. Setelah melakukan setup worker dan database, waktunya setup load balancing. Sama seperti worker, kita dapat menggunakan web console ataupun ssh dengan format yang sama dengan worker karena sama-sama berjenis droplets. Kita melakukan konfigurasi nginx sebagai load balancer dengan mengedit file /etc/nginx/conf.d/default.conf dengan konfig berikut:
```
upstream worker{
    server <IPWorker1>:<PortWorker>;
    server <IPWorker2>:<PortWorker>;
    ...
}

server {
    listen 80;
    server_name <IPLoadBalancer>;

    location / {
        proxy_pass http://worker;
    }
}
```
12. Selanjutnya menghidupkan server dengan command python3 app.py pada worker dan service nginx start
13. Selamat bermain dan beranalisis



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

Berdasarkan hasil pengujian kinerja server, dapat disimpulkan bahwa server mampu menangani permintaan dengan baik pada tingkat pengguna yang moderat, hingga 100 pengguna dengan laju spawn yang meningkat. Meskipun tidak terdapat kegagalan pada uji skenario ekstrem dengan 1000 pengguna, terjadi peningkatan dramatis pada waktu respons untuk permintaan GET, menunjukkan adanya potensi ketidakmampuan server dalam menangani beban tinggi. Oleh karena itu, disarankan untuk mengoptimalkan kemampuan server, khususnya dalam menangani permintaan GET dalam skenario penggunaan yang ekstrem, guna memastikan kinerja yang responsif dan konsisten di bawah tekanan beban yang tinggi.


