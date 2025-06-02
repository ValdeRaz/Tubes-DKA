Ini adalah tubes DKA dari Kelompok RosunTech yang terdiri dari 2 anggota yaitu:
- Muhammad Irgiansyah (103012300039)
- Bill Stephen Sembiring (103012330197)

Dataset yang digunakan:
https://www.kaggle.com/datasets/sampadab17/network-intrusion-detection

Klasifikasi dilakukan dalam dua pendekatan:
- Biner (normal vs intrusion).
- Multi-kelas (DoS, Probe, R2L, U2R).

Algoritma yang digunakan dibatasi pada dua pendekatan utama:
- K-Nearest Neighbors (KNN): Metode klasifikasi berbasis kedekatan fitur antara data uji dan data latih.
- Fuzzy Logic: Digunakan untuk mengakomodasi ketidakpastian dan ambiguitas dalam data, terutama dalam menentukan kelas berdasarkan aturan logika fuzzy mamdani dan sugeno.
Evaluasi hanya dilakukan menggunakan data uji dari dataset yang sama, tanpa implementasi pada jaringan.
Proyek tidak mencakup integrasi model ke dalam sistem IDS secara operasional.

Deskripsi Fitur
Beberapa fitur penting yang tersedia dalam dataset meliputi:
- Duration: Lamanya koneksi berlangsung.
- Protocol_type: Jenis protokol yang digunakan (TCP, UDP, ICMP).
- Service: Layanan jaringan yang digunakan (http, ftp, smtp, dll).
- Flag: Status koneksi berdasarkan protokol.
- Src_bytes & Dst_bytes: Jumlah byte yang dikirim dari dan ke sumber.
- Count & srv_count: Jumlah koneksi ke host atau layanan dalam jangka waktu tertentu.
Label target berupa klasifikasi biner (normal/intrusion) atau multi-kelas (tipe-tipe serangan).

Metodologi
1. Pengumpulan dan Eksplorasi Dataset
Memahami struktur dataset, fitur-fitur yang tersedia, dan distribusi label.

2. Pra-pemrosesan Data
- Encoding fitur kategorikal (misalnya protocol_type, service, flag).
- Normalisasi data numerik untuk mendukung performa KNN.
- Penanganan data yang hilang, duplikat, atau tidak konsisten.

3. Pembagian Dataset
Dataset dibagi menjadi data latih dan data uji (misalnya 80:20 split).

4. Implementasi Algoritma
KNN:
- Menentukan nilai k yang optimal.
- Menghitung jarak (misalnya Euclidean) antara data uji dan data latih.
- Klasifikasi berdasarkan mayoritas tetangga terdekat.

Fuzzy Logic:
- Menentukan fuzzy sets untuk setiap fitur (contoh: rendah, sedang, tinggi).
- Menetapkan aturan fuzzy (fuzzy rules) berdasarkan pengetahuan domain.
- Melakukan proses inferensi dan defuzzifikasi untuk klasifikasi.

6. Evaluasi Model
Menggunakan metrik:
- Akurasi
- Precision
- Recall
- F1-score
Perbandingan performa antara KNN dan Fuzzy.

7. block diagram pada fuzzy dan knn

8. Analisis
- Analisis kekuatan dan kelemahan dari kedua metode.
- Identifikasi fitur yang paling berpengaruh terhadap performa model.

9. Penyusunan Laporan
- Menyusun hasil eksperimen dan visualisasi performa model.
- Diskusi dan kesimpulan.
