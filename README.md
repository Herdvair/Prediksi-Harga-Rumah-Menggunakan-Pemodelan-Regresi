# Prediksi-Harga-Rumah-Menggunakan-Pemodelan-Regresi

# Latar Belakang
Proyek ini membangun model prediksi harga rumah menggunakan dataset Boston Housing yang terdiri dari 506 baris dan 14 kolom. Dataset berisi fitur-fitur numerik yang mencakup kondisi lingkungan, sosial-ekonomi, aksesibilitas, hingga karakteristik rumah, dengan target variabel medv (Median value of owner-occupied homes). Tujuan utama proyek ini adalah menerapkan algoritma regresi untuk memprediksi harga rumah serta mengevaluasi performa model dalam menangkap pola hubungan antar variabel.

# Analisis Objektif
1. Melakukan data cleaning pada dataset Boston Housing.
2. Mengidentifikasi variabel-variabel utama yang berpengaruh terhadap harga rumah.
3. Membangun model regresi linear regularisasi (Ridge & Lasso Regression) untuk prediksi harga rumah.
4. Mengevaluasi performa model menggunakan metrik error (RMSE, MAE, MAPE).
5. Membandingkan hasil model untuk memilih metode dengan generalisasi terbaik.

# Temuan Penting
1. Data Understanding
    - Dataset berisi 13 fitur numerik dan 1 target (medv).
    - Tidak ditemukan data duplikat atau missing value.
    - Tidak perlu penanganan outlier karena distribusi masih wajar.

2. Evaluasi Model Ridge Regression
    - Training: RMSE = 4.96, MAE = 3.56, MAPE = 18%
    - Testing: RMSE = 5.04, MAE = 3.24, MAPE = 17%

      Interpretasi : Model mampu menghindari overfitting dan memiliki generalisasi cukup baik.

3. Evaluasi Model Lasso Regression
     - Training: RMSE = 5.30, MAE = 3.83, MAPE = 18%
     - Testing: RMSE = 5.02, MAE = 3.36, MAPE = 17%

       Interpretasi : Model mampu menghindari overfitting dan memiliki generalisasi cukup baik.

# Kesimpulan
Berdasarkan hasil evaluasi, regresi ridge menunjukkan performa lebih baik pada data training dibandingkan regressi lasso. Dapat dilihat hasil RMSE pada data training ridge lebih kecil dibandingkan lasso, kemungkinan lasso melakukan seleksi fitur jadi berpengaruh dalam akurasi hasil model training. Namun pada data testing, keduanya menujukan hasil yang hampir sama baik dari segi RMSE, MAE dan MAPE. Artinya, kedua model ini memiliki generalisasi yang baik meskipun ridge lebih stabil karena semua fitur dipertahankan dan lasso lebih strict dalam pemilihan fitur karena lasso dapat membuang fitur yang dinilai tidak relevan pada harga rumah.
