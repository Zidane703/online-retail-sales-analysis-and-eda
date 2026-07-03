# 🛒 Online Retail Sales Analysis & Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Pandas](https://img.shields.io/badge/Library-Pandas%20%7C%20Matplotlib%20%7C%20Seaborn-brightgreen.svg)

## 📌 Gambaran Umum Proyek (Project Overview)
Proyek ini fokus pada eksplorasi dan analisis data transaksi bisnis ritel online (*Online Retail Dataset*). Tujuan utama dari analisis ini adalah untuk membersihkan data dari anomali transaksi, memahami karakteristik distribusi data melalui statistik deskriptif, serta mengidentifikasi pasar geografis (negara) yang memberikan kontribusi omzet (*revenue*) terbesar bagi perusahaan.

## 🎯 Tujuan Analisis (Business Objectives)
1. **Data Cleaning:** Membersihkan data transaksi dari *missing values*, data duplikat, serta transaksi yang dibatalkan (*cancelled orders*).
2. **Statistik Deskriptif:** Memahami metrik dasar dari kuantitas barang terjual dan harga satuan produk.
3. **Analisis Pasar Internasional:** Menemukan **Top 10 Negara Penyumbang Omzet Terbesar** untuk membantu pengambilan keputusan strategis pemasaran dan logistik.

---

## 🧹 1. Tahapan Data Cleaning
Dataset ritel mentah sering kali memiliki *noise* yang dapat membiaskan hasil analisis. Tahapan pembersihan yang dilakukan meliputi:
* **Penanganan Missing Values:** Mengidentifikasi dan menangani kolom yang hilang, khususnya pada `CustomerID` dan `Description`.
* **Filter Transaksi Pembatalan:** Menyingkirkan *invoice* yang diawali dengan huruf **'C'** (Cancelled/Retur) agar perhitungan omzet merefleksikan penjualan aktual.
* **Filter Nilai Negatif:** Menghapus data dengan `Quantity` atau `UnitPrice` $\le 0$.
* **Pembuatan Fitur Baru (Feature Engineering):** Menambahkan kolom `Total_Revenue` yang dihitung dari `Quantity * UnitPrice`.

---

## 📊 2. Statistik Deskriptif (Descriptive Statistics)
Setelah data dibersihkan, diperoleh gambaran distribusi data penjualan sebagai berikut:
* Rata-rata (*mean*) kuantitas barang per transaksi menunjukkan kebiasaan pembelian pelanggan (eceran vs grosir).
* Distribusi nilai `Total_Revenue` menunjukkan adanya beberapa transaksi bernilai tinggi (*high-value orders*) yang berpotensi berasal dari klien B2B.

*(Catatan: Anda bisa menambahkan tabel ringkasan fungsi `.describe()` di sini jika diperlukan)*

---

## 🌍 3. Top 10 Negara Penyumbang Omzet Terbesar
Berdasarkan agregasi total omzet (`Total_Revenue`) per negara, berikut adalah 10 pasar terbesar bagi bisnis ritel ini:

| Peringkat | Negara | Kontribusi Omzet / Dominasi Pasar |
| :---: | :--- | :--- |
| **1** | United Kingdom (UK) | Pasar domestik utama (penyumbang mayoritas omzet) |
| **2** | *[Nama Negara Ke-2]* | Pasar ekspansi terbesar di Eropa |
| **3** | *[Nama Negara Ke-3]* | Pasar potensial dengan rata-rata nilai transaksi tinggi |
| ... | *[Dst sampai Top 10]* | ... |

*(💡 Opsional: Jika Anda mengupload gambar grafik ke GitHub, Anda bisa memunculkan gambarnya di sini dengan sintaks: `![Top 10 Countries](nama_file_gambar.png)`)*

---

## 💡 Rekomendasi Bisnis (Business Recommendations)
Berdasarkan temuan di atas, beberapa langkah strategis yang direkomendasikan untuk manajemen:
1. **Fokus Retensi Pasar Utama:** Memastikan ketersediaan stok (*inventory management*) dan efisiensi pengiriman di negara Top 1 (UK).
2. **Ekspansi Pasar Internasional Potensial:** Memberikan promosi khusus atau menurunkan biaya ongkos kirim untuk negara di peringkat 2 hingga 5 untuk meningkatkan *retention rate*.
3. **Segmentasi Pelanggan:** Mengelompokkan pelanggan berdasarkan frekuensi dan nilai belanja untuk program loyalitas (*VIP Customer Program*).

---

## 🛠️ Struktur Repository
* `[Nama_File_Notebook_Anda].ipynb`: Notebook utama berisi alur kode lengkap dari *loading data* hingga visualisasi.
