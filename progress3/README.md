## Progres 3 - Implementasi Database dan Pengujian

## 1. Script SQL DDL

Script SQL DDL digunakan untuk membuat database dan tabel pada Sistem Pemesanan Makanan Online. Pada tahap ini, database dibuat berdasarkan rancangan yang telah disusun pada Progres 1 dan Progres 2.

Database yang digunakan adalah:

```sql
db_pemesanan_makanan_online
```

File script SQL lengkap terdapat pada file berikut:

```text
progress3.sql
```

Script SQL tersebut berisi perintah untuk membuat database, membuat tabel, menentukan primary key, foreign key, unique, not null, check constraint, memasukkan data uji, serta melakukan pengujian query.

## 2. Constraint yang Digunakan

Constraint digunakan untuk menjaga data agar tetap valid dan sesuai dengan relasi antar tabel. Berikut adalah constraint yang digunakan dalam database Sistem Pemesanan Makanan Online:

| No | Constraint  | Penjelasan                                                                                                       |
| -- | ----------- | ---------------------------------------------------------------------------------------------------------------- |
| 1  | Primary Key | Digunakan sebagai identitas unik pada setiap tabel.                                                              |
| 2  | Foreign Key | Digunakan untuk menghubungkan tabel yang saling berelasi.                                                        |
| 3  | Unique      | Digunakan agar data tertentu tidak boleh sama, seperti email pelanggan dan username admin.                       |
| 4  | Not Null    | Digunakan agar kolom penting tidak boleh kosong.                                                                 |
| 5  | Check       | Digunakan untuk membatasi nilai tertentu, seperti harga, stok, jumlah, dan subtotal agar tidak bernilai negatif. |
| 6  | Default     | Digunakan untuk memberikan nilai awal pada status pesanan, pembayaran, dan pengiriman.                           |

## 3. Data Uji

Data uji dimasukkan untuk memastikan bahwa setiap tabel dapat menyimpan data dengan benar. Data uji yang digunakan meliputi data pelanggan, admin, kategori menu, menu, pesanan, detail pesanan, pembayaran, kurir, dan pengiriman.

| No | Nama Tabel     | Keterangan                                                   |
| -- | -------------- | ------------------------------------------------------------ |
| 1  | pelanggan      | Menyimpan data pelanggan yang melakukan pemesanan makanan.   |
| 2  | admin          | Menyimpan data admin atau pengelola restoran.                |
| 3  | kategori_menu  | Menyimpan kategori menu seperti makanan, minuman, dan snack. |
| 4  | menu           | Menyimpan data menu makanan dan minuman yang tersedia.       |
| 5  | pesanan        | Menyimpan data pesanan pelanggan.                            |
| 6  | detail_pesanan | Menyimpan rincian menu yang dipesan pelanggan.               |
| 7  | pembayaran     | Menyimpan data metode dan status pembayaran.                 |
| 8  | kurir          | Menyimpan data kurir yang mengantar pesanan.                 |
| 9  | pengiriman     | Menyimpan data alamat tujuan dan status pengiriman.          |

## 4. Query SQL

Pada tahap pengujian, dilakukan beberapa query SQL untuk memastikan database dapat berjalan sesuai kebutuhan sistem. Query yang diuji meliputi query untuk menampilkan data, menggabungkan tabel, menghitung total pendapatan, menampilkan pesanan berdasarkan kondisi tertentu, dan mengubah status pesanan.

| No | Query                                 | Tujuan                                                                    |
| -- | ------------------------------------- | ------------------------------------------------------------------------- |
| 1  | Menampilkan daftar tabel              | Untuk memastikan semua tabel berhasil dibuat.                             |
| 2  | Menampilkan data pelanggan            | Untuk memastikan data pelanggan berhasil dimasukkan.                      |
| 3  | Menampilkan data menu                 | Untuk memastikan data menu berhasil dimasukkan.                           |
| 4  | Menampilkan menu, kategori, dan admin | Untuk menguji relasi tabel menu, kategori_menu, dan admin.                |
| 5  | Menampilkan detail pesanan            | Untuk menguji relasi tabel pesanan, pelanggan, detail_pesanan, dan menu.  |
| 6  | Menampilkan data pengiriman dan kurir | Untuk menguji relasi tabel pengiriman, pesanan, pelanggan, dan kurir.     |
| 7  | Menampilkan pesanan COD               | Untuk menampilkan pesanan dengan metode pembayaran COD.                   |
| 8  | Menghitung total pendapatan           | Untuk menghitung total pendapatan dari pembayaran yang berhasil.          |
| 9  | Menampilkan pesanan belum selesai     | Untuk menampilkan pesanan dengan status menunggu, diproses, atau dikirim. |
| 10 | Update status pesanan                 | Untuk menguji perubahan status pesanan dan status pengiriman.             |

## 5. Skenario Pengujian

Berikut adalah skenario pengujian yang dilakukan pada database Sistem Pemesanan Makanan Online:

| No | Skenario Pengujian                              | Hasil yang Diharapkan                                                   |
| -- | ----------------------------------------------- | ----------------------------------------------------------------------- |
| 1  | Membuat database                                | Database berhasil dibuat.                                               |
| 2  | Membuat tabel                                   | Seluruh tabel berhasil dibuat.                                          |
| 3  | Menampilkan daftar tabel                        | Seluruh tabel tampil di database.                                       |
| 4  | Memasukkan data uji                             | Data berhasil masuk ke masing-masing tabel.                             |
| 5  | Menampilkan data pelanggan                      | Data pelanggan tampil dengan benar.                                     |
| 6  | Menampilkan data menu                           | Data menu tampil dengan benar.                                          |
| 7  | Menampilkan menu berdasarkan kategori dan admin | Data menu tampil bersama kategori dan admin pengelola.                  |
| 8  | Menampilkan detail pesanan                      | Data pesanan tampil bersama nama pelanggan, menu, jumlah, dan subtotal. |
| 9  | Menampilkan data pengiriman                     | Data pengiriman tampil bersama nama pelanggan dan kurir.                |
| 10 | Menghitung total pendapatan                     | Total pendapatan dari pembayaran berhasil dapat dihitung.               |
| 11 | Menampilkan pesanan belum selesai               | Data pesanan yang belum selesai berhasil ditampilkan.                   |
| 12 | Update status pesanan                           | Status pesanan dan status pengiriman berhasil diperbarui.               |

## 6. Screenshot Hasil Implementasi dan Query

Berikut adalah screenshot hasil implementasi database dan pengujian query SQL.

### 6.1 Menampilkan Daftar Tabel

Query ini digunakan untuk memastikan bahwa seluruh tabel berhasil dibuat pada database.

![Show Tables](screenshots/ss_query_01_show_tables.png)

### 6.2 Menampilkan Data Pelanggan

Query ini digunakan untuk menampilkan seluruh data pelanggan yang telah dimasukkan ke dalam database.

![Data Pelanggan](screenshots/ss_query_02_data_pelanggan.png)

### 6.3 Menampilkan Data Menu

Query ini digunakan untuk menampilkan seluruh data menu yang tersedia pada sistem.

![Data Menu](screenshots/ss_query_03_data_menu.png)

### 6.4 Menampilkan Menu Berdasarkan Kategori dan Admin

Query ini digunakan untuk menampilkan daftar menu lengkap dengan kategori dan admin yang mengelola menu tersebut.

![Menu Kategori Admin](screenshots/ss_query_04_menu_kategori_admin.png)

### 6.5 Menampilkan Detail Pesanan

Query ini digunakan untuk menampilkan detail pesanan pelanggan, seperti nama pelanggan, nama menu, jumlah pesanan, dan subtotal.

![Detail Pesanan](screenshots/ss_query_05_detail_pesanan.png)

### 6.6 Menampilkan Data Pengiriman dan Kurir

Query ini digunakan untuk menampilkan data pengiriman pesanan, alamat tujuan, kurir yang bertugas, dan status pengiriman.

![Pengiriman Kurir](screenshots/ss_query_06_pengiriman_kurir.png)

### 6.7 Menampilkan Pesanan dengan Metode Pembayaran COD

Query ini digunakan untuk menampilkan pesanan pelanggan yang menggunakan metode pembayaran COD atau bayar di tempat.

![Pembayaran COD](screenshots/ss_query_07_pembayaran_cod.png)

### 6.8 Menghitung Total Pendapatan

Query ini digunakan untuk menghitung total pendapatan dari seluruh pesanan yang status pembayarannya berhasil.

![Total Pendapatan](screenshots/ss_query_08_total_pendapatan.png)

### 6.9 Menampilkan Pesanan yang Belum Selesai

Query ini digunakan untuk menampilkan data pesanan yang belum selesai, yaitu pesanan dengan status Menunggu, Diproses, atau Dikirim.

![Pesanan Belum Selesai](screenshots/ss_query_09_pesanan_belum_selesai.png)

### 6.10 Update Status Pesanan dan Pengiriman

Query ini digunakan untuk mengubah status pesanan dan status pengiriman pada pesanan tertentu. Setelah dilakukan update, query pengecekan dijalankan untuk memastikan bahwa status berhasil berubah.

![Update Status](screenshots/ss_query_10_update_status.png)

## 7. Kesimpulan

Berdasarkan hasil implementasi dan pengujian, database Sistem Pemesanan Makanan Online berhasil dibuat sesuai dengan rancangan pada Progres 1 dan Progres 2. Seluruh tabel berhasil dibuat, data uji berhasil dimasukkan, relasi antar tabel dapat berjalan dengan baik, dan query SQL dapat digunakan untuk menampilkan informasi pelanggan, menu, pesanan, pembayaran, serta pengiriman.

Dengan demikian, database sudah dapat digunakan sebagai dasar penyimpanan data untuk Sistem Pemesanan Makanan Online.
