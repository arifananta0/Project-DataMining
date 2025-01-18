# PENAMBANGAN-DATA-4504
#### Tugas tentang mata kuliah penambangan data kelompok A11.4504.
#### Nama : Muhammad Arif Ananta
#### NIM : A11.2022.14533
### JUDUL
- Prediksi Pemenang Pertandingan Sepak Bola
# Ringkasan dan Permasalahan Project + Tujuan yang Akan Dicapai + Model / Alur Penyelesaian
-Ringkasan:
Proyek ini bertujuan untuk memprediksi hasil pertandingan sepak bola menggunakan data statistik dari pertandingan sebelumnya. Dengan menggunakan pendekatan machine learning, model akan dilatih untuk mengenali pola-pola yang berkontribusi pada kemenangan sebuah tim.
-Permasalahan:
Sepak bola adalah olahraga dengan banyak variabel yang memengaruhi hasil pertandingan. Prediksi hasil pertandingan sangat relevan untuk penggemar, analis olahraga, dan pelaku industri taruhan. Permasalahan yang akan diselesaikan adalah bagaimana memanfaatkan data pertandingan untuk memprediksi pemenang.

-Tujuan:
Membangun model machine learning yang dapat memprediksi hasil pertandingan sepak bola dengan akurasi yang baik.

Model / Alur Penyelesaian:
1Pengumpulan Data: Menggunakan dataset yang telah tersedia dalam format CSV (misalnya,matches.csv) yang berisi data lengkap dari pertandingan Premier League.

2. Preprocessing Data: Melakukan pembersihan data yang mencakup penanganan nilai yang hilang, normalisasi, dan encoding atribut kategori.

3. Eksplorasi Data: Menganalisis pola dan tren dalam data menggunakan visualisasi dan statistik deskriptif untuk mendapatkan wawasan awal.

4. Pemilihan Model: Menerapkan berbagai algoritma machine learning, seperti Decision Tree, Random Forest, SVM, atau Logistic Regression untuk memprediksi hasil pertandingan.

5. Evaluasi Model: Menggunakan metrik evaluasi seperti akurasi, precision, recall, dan F1-score untuk mengevaluasi kinerja setiap model.

6. Optimasi Model: Melakukan tuning hyperparameter untuk memperbaiki performa model.

7. Prediksi dan Analisis Hasil: Mengimplementasikan model pada data baru untuk
memprediksi hasil pertandingan dan menganalisis faktor yang paling memengaruhi prediksi.
-Bagan Alur Penyelesaian:
# Penjelasan Dataset, EDA dan Proses Features Dataset
Penjelasan Dataset:
Sumber Data: Dataset diambil dari file matches.csv, yang berisi data pertandingan sepak bola
lengkap dengan atribut yang menggambarkan hasil pertandingan dan statistik pertandingan.

Dengan Atribute : 
1. Date - Tanggal pertandingan
2. HomeTeam - Nama tim yang bermain sebagai tuan rumah
3. AwayTeam - Nama tim tamu
4. FTHG (Full Time Home Goals) - Jumlah gol yang dicetak oleh tim tuan rumah
5. FTAG (Full Time Away Goals) - Jumlah gol yang dicetak oleh tim tamu
6. FTR (Full Time Result) - Hasil pertandingan akhir (H = Home Win, D = Draw, A = Away Win)
Proses Features Dataset:

Transformasi Variabel Kategoris: Mengubah nama tim menjadi encoding numerik.
Penambahan Variabel Baru: Seperti selisih gol (FTHG - FTAG).
Normalisasi: Menskala data numerik untuk model yang sensitif terhadap skala.
# Proses Learning / Modeling
Proses Learning:

-Logistic Regression: Untuk memprediksi hasil kategori pertandingan.
-Random Forest: Untuk menangkap hubungan non-linear.
-Gradient Boosting: Untuk meningkatkan akurasi dengan teknik ensemble.
# Peforma Model
Performa Model:
Evaluasi model dilakukan dengan beberapa metrik utama:
Akurasi: Mengukur persentase prediksi yang benar dari keseluruhan data uji.
Precision: Mengukur proporsi prediksi hasil positif yang benar.

Logistic Regression: Memberikan hasil yang cukup baik sebagai baseline, tetapi kurang mampu menangani hubungan non-linear.
Random Forest: Menunjukkan peningkatan performa dengan akurasi dan recall yang lebih tinggi dibanding Logistic Regression.
Gradient Boosting: Memberikan hasil terbaik dengan akurasi 82%, berkat kemampuannya mempelajari pola secara iteratif dan menangani data yang kompleks.
# Diskusi Hasil dan Kesimpulan
-Diskusi Hasil:
Hasil evaluasi menunjukkan bahwa model Gradient Boosting adalah yang paling unggul untuk dataset ini, diikuti oleh Random Forest. Logistic Regression, meskipun cepat dan sederhana, kurang optimal dalam menangkap pola data yang lebih kompleks.
Model Gradient Boosting mampu memberikan prediksi yang akurat karena pendekatannya yang menggabungkan banyak pohon keputusan secara iteratif untuk memperbaiki kesalahan dari iterasi sebelumnya. Akan tetapi, waktu pelatihan model ini lebih lama dibanding Random Forest dan Logistic Regression

-Kesimpulan:
Variabel selisih gol dan performa tim sebelumnya adalah faktor penting dalam prediksi hasil pertandingan sepak bola.
Gradient Boosting memberikan performa terbaik dengan akurasi, precision, dan recall tertinggi di antara model yang diuji.
Untuk pengembangan lebih lanjut, dataset dapat diperluas dengan fitur tambahan seperti statistik pemain individu, kondisi cuaca, atau strategi tim.
Implementasi model dapat mendukung analisis strategis bagi pelatih, analis, atau pihak terkait dalam dunia sepak bola.
