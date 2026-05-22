# Python-Projects
# 🚗 Car Price Analytics: Memahami Driver Utama Penentu Harga Mobil Second & Baru

## 📌 1. Latar Belakang & Masalah Bisnis
Industri otomotif sekunder (mobil bekas) memiliki volatilitas harga yang sangat tinggi. Perusahaan dealer mobil seringkali kesulitan menentukan harga beli dan harga jual optimal (*pricing strategy*) yang kompetitif namun tetap menjaga margin keuntungan. 

**Tujuan Proyek:**
Proyek ini bertujuan untuk menganalisis faktor-faktor apa saja yang secara signifikan mendominasi penentuan harga kendaraan (*Car Price Drivers*) seperti pengaruh Brand, Mileage (jarak tempuh), Jenis Bahan Bakar, Transmisi, serta depresiasi harga berdasarkan tahun rilisnya.

---

## 🛠️ 2. Tech Stack & Arsitektur Proyek
Proyek ini dibangun menggunakan pendekatan **Pure Python Scripting (Production-Ready)** untuk memudahkan otomasi laporan berkala.

- **Bahasa:** Python 3.10+
- **Library Utama:** `pandas` (Data Manipulation), `matplotlib` & `seaborn` (Advanced Data Visualization)
- **IDE:** VS Code

---

## 📊 3. Ringkasan Temuan & Visualisasi Data
*(Catatan: Grafik di bawah ini diekspor otomatis ke folder `output/` saat skrip dijalankan)*

### A. Distribusi Harga Mobil Pasar
Grafik ini digunakan untuk mengidentifikasi konsentrasi harga terbesar di pasar guna menyusun segmentasi target konsumen yang tepat (*Low, Mid, High-End*).
![Distribusi Harga](output/1_distribusi_harga.png)

### B. Analisis Segmentasi Pasar Berdasarkan Brand
Membantu divisi pengadaan barang (*procurement*) untuk mengetahui brand mana saja yang memiliki nilai pasar premium tertinggi.
![Harga Per Brand](output/2_harga_per_brand.png)

### C. Pengaruh Jarak Tempuh (Mileage) terhadap Penurunan Harga (Depresiasi)
Melalui analisis regresi linear sederhana ini, kita dapat menghitung persentase penurunan harga kendaraan untuk setiap kelipatan jarak tempuh tertentu.
![Mileage vs Harga](output/3_mileage_vs_harga.png)

### D. Tren Harga Berdasarkan Tahun Rilis dan Kondisi Mobil
Analisis tren ini membantu tim penjualan mengantisipasi seberapa cepat harga aset menurun seiring bertambahnya usia kendaraan, dikelompokkan berdasarkan kondisi fisik (*New, Like New, Used*).
![Tren Harga](output/4_tren_harga_tahunan.png)

---

## 💡 4. Rekomendasi Bisnis Terkait (Data-Driven Insights)
1. **Strategi Procurement Berdasarkan Jarak Tempuh:** Mengingat tingginya tingkat depresiasi harga mobil seiring naiknya *Mileage* (sebagaimana terlihat di grafik regresi), disarankan bagi diler untuk fokus membeli mobil bekas dengan jarak tempuh di bawah batas psikologis tertentu untuk menjaga profit margin saat penjualan kembali.
2. **Optimalisasi Portofolio Inventori:** Berdasarkan visualisasi harga per Brand, brand premium seperti Tesla/Mercedes mempertahankan nilai yang tinggi, namun memiliki pangsa pasar yang lebih mengerucut. Kombinasi inventori ideal adalah 70% Brand volume tinggi (seperti Honda/Ford) dan 30% Brand premium untuk memaksimalkan *cash flow* perputaran barang.

---

## 🚀 5. Cara Menjalankan Proyek Ini Secara Lokal
1. Clone repositori ini:
   ```bash
   git clone [https://github.com/username-anda/car-price-analysis.git](https://github.com/username-anda/car-price-analysis.git)
