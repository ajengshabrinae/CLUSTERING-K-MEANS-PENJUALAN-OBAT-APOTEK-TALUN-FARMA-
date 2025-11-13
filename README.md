📊 Aplikasi Clustering K-Means untuk Analisis Penjualan Obat
Aplikasi web interaktif berbasis Streamlit untuk melakukan analisis clustering K-Means pada data penjualan obat.

✨ Fitur Utama
Upload Data - Upload dataset CSV dengan validasi otomatis
Pilih Fitur - Pilih fitur-fitur yang akan digunakan untuk clustering
Tentukan Jumlah Cluster - Menggunakan metode Elbow untuk menentukan K optimal
Visualisasi Hasil - Visualisasi 2D dan 3D interaktif
Download Laporan - Download hasil dalam format Excel, CSV, atau TXT
🚀 Cara Menjalankan
1. Install Dependencies
pip install -r requirements.txt
2. Jalankan Aplikasi
streamlit run app.py
Aplikasi akan terbuka di browser pada alamat http://localhost:8501

📁 Format Dataset
Dataset harus berupa file CSV dengan format sebagai berikut:

Separator: Titik koma (;)
Kolom yang diperlukan:
Nama Obat - Nama obat (teks)
Jumlah - Jumlah penjualan (angka)
Harga - Harga total (angka)
Jenis Obat - Jenis obat (0 = Antibiotik, 1 = Non-Antibiotik)
Contoh Format:
Nama Obat;Jumlah;Harga;Jenis Obat
AMOXICILLIN 500MG;558;3420000;0
PARACETAMOL 500MG;1510;3020000;1
📖 Panduan Penggunaan
Langkah 1: Upload Data
Klik tombol "Browse files" pada bagian Upload Data
Pilih file CSV dataset Anda
Sistem akan otomatis memvalidasi data
Jika berhasil, preview data akan ditampilkan
Langkah 2: Pilih Fitur
Pada bagian Pilih Fitur, pilih minimal 2 fitur untuk clustering
Disarankan memilih 3 fitur untuk visualisasi 3D
Fitur yang tersedia:
Jumlah (jumlah penjualan)
Harga (harga total penjualan)
Jenis Obat (0 atau 1)
Langkah 3: Tentukan Jumlah Cluster
Perhatikan grafik Metode Elbow yang ditampilkan
Pilih jumlah cluster (k) optimal berdasarkan "siku" pada grafik
Gunakan slider untuk memilih jumlah cluster (2-10)
Klik tombol "Jalankan Clustering"
Langkah 4: Visualisasi Hasil
Setelah clustering selesai, Anda dapat melihat:

Distribusi Cluster - Jumlah dan persentase obat per cluster
Visualisasi 2D - Scatter plot dengan pilihan fitur sumbu X dan Y
Visualisasi 3D - Scatter plot 3D (jika menggunakan 3 fitur)
Detail Cluster - Statistik dan daftar obat per cluster
Langkah 5: Download Laporan
Pilih format laporan yang diinginkan:

Excel (.xlsx) - Berisi data clustering, centroid, dan statistik
TXT (.txt) - Laporan lengkap dalam format teks
CSV (.csv) - Data hasil clustering
📊 Interpretasi Hasil
Davies-Bouldin Index (DBI)
Metrik evaluasi kualitas clustering
Semakin rendah nilai DBI, semakin baik clustering
Nilai DBI < 1.0 menunjukkan clustering yang baik
DBI mengukur seberapa terpisah antar cluster dan seberapa kompak dalam cluster
Centroid
Titik pusat dari setiap cluster
Ditampilkan dalam nilai standar (setelah normalisasi)
Merepresentasikan karakteristik rata-rata dari cluster
🔧 Troubleshooting
Error saat upload file
Pastikan file berformat CSV dengan separator titik koma (;)
Cek encoding file (gunakan UTF-8 atau UTF-8-sig)
Pastikan semua kolom yang diperlukan ada dalam file
Visualisasi tidak muncul
Pastikan sudah klik tombol "Jalankan Clustering"
Untuk visualisasi 3D, pastikan sudah memilih 3 fitur
Data tidak valid
Cek apakah ada nilai kosong atau tidak valid pada kolom numerik
Pastikan kolom "Jenis Obat" hanya berisi nilai 0 atau 1
📝 Catatan
Aplikasi ini menggunakan algoritma K-Means dari scikit-learn
Data akan dinormalisasi menggunakan StandardScaler sebelum clustering
Hasil clustering bersifat non-deterministik, namun menggunakan random_state=42 untuk reproduktibilitas
🛠️ Teknologi yang Digunakan
Streamlit - Framework aplikasi web
Pandas - Manipulasi data
Scikit-learn - Algoritma K-Means dan evaluasi
Matplotlib - Visualisasi
NumPy - Komputasi numerik
SciPy - Perhitungan jarak
📄 Lisensi
Aplikasi ini dibuat untuk keperluan analisis data penjualan obat.
