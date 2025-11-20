# Analisis-Data-Spotify-dan-Visualisasi
Analisis perilaku pengguna Spotify meliputi data cleaning, EDA, visualisasi, pengujian statistik, dan pembangunan model Random Forest untuk prediksi churn. Repositori ini menyajikan insight mendalam tentang faktor-faktor yang memengaruhi retensi pengguna dan menampilkan pipeline analisis end-to-end, mulai dari pengolahan data hingga model final.

## 🎧 Spotify User Behavior Analysis & Visualization

Proyek ini bertujuan untuk menganalisis perilaku pengguna Spotify berdasarkan data penggunaan aplikasi, memahami faktor yang memengaruhi churn, serta membangun model prediksi menggunakan Random Forest. Dataset berisi 8.000 observasi dengan 12 fitur terkait demografi, pola mendengarkan, dan interaksi pengguna dengan aplikasi.

## 🔍 Tahapan Proyek
### 1. Data Cleaning

- Menangani `inkonsistensi tipe data` pada kolom kategorikal dan numerik
- Memeriksa dan memastikan tidak ada `missing values` dan `data duplikat`
- Mengetahui `ukuran dataset` yang dimiliki
  
### 2. Exploratory Data Analysis (EDA)

- **Numerical description:** `df.describe()` untuk mengetahui mean, std, min/max, quantiles.  
- **Outlier detection:** menggunakan IQR atau grafik boxplots untuk menandai nilai ekstrem.  
- **Missing & duplicates report:** Hasil EDA.  

### 3. Data Visualization

- Visualisasi distribusi data dengan `histogram`, `boxplot`, dan `KDE plot`
- Bar chart & pie chart untuk komposisi demografi serta tipe langganan
- Visualisasi segmentasi perilaku pengguna

### 4. Pengujian Statistik

- Uji statistik untuk mengetahui apakah perbedaan yang terlihat pada grafik signifikan secara statistik atau tidak.

### 5. Machine Learning Modeling (Random Forest)

- Membangun model klasifikasi untuk memprediksi user churn
- Feature importance untuk memahami variabel paling berpengaruh
- Evaluasi model menggunakan akurasi, precision, recall, F1-score, dan ROC-AUC

## 📊 Dataset Overview

Dataset terdiri dari fitur berikut:

- Demografi: `id_pengguna`, `jenis_kelamin`, `usia`, `negara`
- Perilaku Penggunaan: `waktu_mendengarkan`, `lagu_diputar_per_hari`, `tingkat_lewati_lagu`, `mendengarkan_offline`
- Interaksi Aplikasi: `jenis_perangkat`, `iklan_didengar_per_minggu`, `tipe_langganan`
- Target: `status_berhenti` (0 = tidak churn, 1 = churn)

## 🎯 Hasil & Insight Utama

- Mengidentifikasi pola perilaku yang membedakan pengguna churn dan non-churn
- Fitur seperti `waktu_mendengarkan`, `lagu_diputar_per_hari`, `tingkat_lewati_lagu`, dan `usia` berkontribusi signifikan dalam model
- Model Random Forest cenderung **mengutamakan klasifikasi kelas mayoritas** (pelanggan yang tidak berhenti) sehingga memiliki recall sangat tinggi untuk kelas 0.
- Model **kesulitan mengenali pelanggan churn (kelas 1)**, ditandai dengan recall dan F1-score yang sangat rendah pada kelas ini.
- Hal ini kemungkinan besar disebabkan oleh **ketidakseimbangan data** antara kelas pelanggan berhenti dan tidak berhenti.
