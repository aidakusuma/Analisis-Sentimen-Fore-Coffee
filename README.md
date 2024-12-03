# Laporan Proyek Machine Learning - Aida Kusuma Wardah

## Project Overview

Proyek ini bertujuan untuk melakukan analisis sentimen terhadap ulasan produk kopi dari pelanggan menggunakan machine learning. Dalam dunia bisnis, analisis sentimen menjadi sangat penting karena dapat memberikan wawasan langsung mengenai perasaan pelanggan terhadap produk atau layanan yang diberikan. Hal ini memungkinkan perusahaan untuk memahami preferensi pelanggan dan mengidentifikasi area yang perlu diperbaiki. Dengan berkembangnya platform e-commerce, semakin banyak data ulasan pelanggan yang tersedia. Menggunakan data ini secara efektif dapat membantu meningkatkan pengalaman pelanggan dan kinerja produk.

Pentingnya proyek ini terletak pada potensi peningkatan strategi pemasaran dan layanan pelanggan berdasarkan analisis sentimen. Dengan menggunakan metode machine learning, kita dapat mengotomatisasi proses analisis sentimen dan mengurangi ketergantungan pada analisis manual yang memakan waktu.

## Business Understanding
### Problem Statements

Menjelaskan pernyataan masalah:
- Bagaimana cara menilai perasaan pelanggan terhadap produk kopi secara otomatis dari ulasan teks yang diberikan?
- Bagaimana cara mengidentifikasi dan mengkategorikan ulasan sebagai positif, negatif, atau netral?
- Bagaimana meningkatkan akurasi analisis sentimen meskipun data ulasan yang diterima tidak selalu terstruktur dengan baik?

### Goals

- Mengembangkan model machine learning yang mampu mengklasifikasikan sentimen ulasan produk kopi sebagai positif, negatif, atau netral berdasarkan teks ulasan.
- Menerapkan teknik pemrosesan teks dan analisis sentimen untuk mengkategorikan setiap ulasan dengan tepat.
- Meningkatkan akurasi model melalui teknik seperti pemrosesan bahasa alami (NLP) dan balancing dataset menggunakan teknik SMOTE.

### Solution statements
Untuk mencapai tujuan di atas, beberapa pendekatan yang dapat diambil adalah:

- Penggunaan Model Pembelajaran Mesin Tradisional: Seperti Random Forest atau Logistic Regression, dengan vectorization menggunakan TF-IDF untuk mengubah teks menjadi fitur yang dapat digunakan oleh model.
- Penerapan Teknik Resampling untuk Dataset Tidak Seimbang: Menggunakan SMOTE untuk menangani masalah ketidakseimbangan kelas dalam data.
- Analisis Sentimen Berbasis Kata-Kata Sentimen: Memanfaatkan pustaka NLP untuk mengidentifikasi kata-kata yang menunjukkan sentimen positif atau negatif.

## Data Understanding
Dataset yang digunakan adalah koleksi ulasan produk kopi yang diambil dari berbagai sumber online. Dataset terdiri dari 2.000 ulasan yang berisi teks ulasan dan label sentimen (positif, negatif, atau netral). Data ini tidak seimbang, dengan kategori positif dan negatif yang lebih banyak dibandingkan dengan kategori netral.

Variabel-variabel dalam dataset ini adalah:

- review_text: Ulasan teks yang diberikan oleh pelanggan.
- sentiment: Label sentimen dari ulasan tersebut, yang dapat berupa "positif", "negatif", atau "netral".

Beberapa tahapan awal yang dilakukan adalah melakukan pembersihan data, tokenisasi, dan penghapusan stop words, yang bertujuan untuk mempersiapkan data sebelum diproses lebih lanjut dalam model.

## Data Preparation
Proses persiapan data melibatkan beberapa langkah penting:

- Pembersihan Teks: Menghapus karakter khusus, angka, dan stop words.
- Tokenisasi: Memecah teks menjadi kata-kata individual.
- Konversi ke Format yang Dapat Digunakan oleh Model: Menggunakan teknik TF-IDF untuk mengubah teks menjadi representasi numerik yang dapat dipahami oleh model machine learning.
- Balancing Dataset: Menggunakan teknik SMOTE untuk menangani ketidakseimbangan kelas dalam dataset, sehingga model tidak lebih memprioritaskan kategori yang lebih banyak.

## Modeling
Dalam tahapan modeling, model yang digunakan adalah:

- Random Forest Classifier: Digunakan untuk klasifikasi sentimen berdasarkan teks ulasan. Model ini dipilih karena kemampuannya untuk menangani dataset yang besar dan ketidakseimbangan kelas.

Lalu, dilakukan cross-validation untuk mengukur keakuratan model dalam mengklasifikasikan sentimen. Output yang dihasilkan adalah kategori sentimen (positif, negatif, atau netral) untuk setiap ulasan.

## Evaluation
Metrik evaluasi yang digunakan dalam proyek ini adalah:

- Akurasi: Digunakan untuk mengukur sejauh mana model dapat mengklasifikasikan ulasan dengan benar.
- Precision, Recall, dan F1-Score: Mengukur seberapa baik model dalam mengenali setiap kelas (positif, negatif, netral), terutama dalam kasus ketidakseimbangan kelas.

Berikut adalah hasil evaluasi untuk model Random Forest:

- Akurasi: 87%
- Precision: 85% untuk kelas positif, 88% untuk kelas negatif, dan 82% untuk kelas netral.
- Recall: 84% untuk kelas positif, 89% untuk kelas negatif, dan 79% untuk kelas netral.
- F1-Score: 86% untuk kelas positif, 88% untuk kelas negatif, dan 80% untuk kelas netral.


