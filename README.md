# Laporan Proyek Machine Learning - Bily Hakim Erlangga

![water.jpg](image%2Fwater.jpg)
## Domain Proyek

Akses terhadap air minum bersih merupakan kebutuhan mutlak bagi kelangsungan hidup manusia, mengingat tubuh manusia terdiri dari sekitar 70% air. Asupan air yang tidak mencukupi 
dapat secara signifikan berdampak pada kesehatan seseorang, situasi yang sangat tidak disarankan oleh para profesional kesehatan. Di bawah ini adalah beberapa konsekuensi yang dapat 
timbul ketika tubuh kekurangan pasokan air yang cukup  ([Dampak Kurang Minum Air Putih](https://yankes.kemkes.go.id/view_artikel/2638/dampak-kurang-minum-air-putih)):

1. Sistem Imun yang melemah
2. Sangat sulit untuk berfokus
3. memicu mood yang menjadi buruk (Bad Mood)
4. Tekanan darah menurun
5. Dan masih banyak lagi

Selain itu, dengan kemajuan teknologi informasi, khususnya di bidang pembelajaran mesin, diakui bahwa integrasi pembelajaran mesin ke dalam perawatan kesehatan dapat memberikan hasil yang 
bermanfaat, seperti yang ditekankan dalam penelitian Javaid et al  ([Significance of machine learning in healthcare ...](https://www.sciencedirect.com/science/article/pii/S2666603022000069))

Selain itu, merujuk pada data Perserikatan Bangsa-Bangsa (PBB) pada tahun 2019, dilaporkan bahwa seperempat dari populasi global atau setara dengan 2,2 miliar orang masih kekurangan akses terhadap air minum yang aman  ([1 in 3 people globally do not have ...](https://www.sciencedirect.com/science/article/pii/S2666603022000069)).
Di Indonesia, menurut Bappenas, beberapa daerah di Jawa dan Bali sudah menghadapi tantangan kelangkaan air. Hal ini yang kemudian memunculkan ide inovatif dari penulis.

Penulis mengakui bahwa solusi yang diajukan tidak secara langsung mengatasi masalah kelangkaan air minum. Sebaliknya, konsep menyeluruhnya berkisar pada pengembangan alat yang mampu secara otomatis mengidentifikasi sumber air dengan kualitas air yang dapat diminum. Sistem ini memanfaatkan teknologi machine learning untuk memprediksi kelayakan air, 
memberikan nilai 1 untuk air yang dapat diminum dan 0 untuk air yang tidak layak minum.

Dari perspektif bisnis, teknologi ini dapat diintegrasikan ke dalam dispenser air, mengubah air keran menjadi air minum yang aman. Hal ini akan melibatkan penggabungan sensor yang terhubung ke perangkat IoT, yang memungkinkan pemantauan secara real-time dan menghasilkan peringatan jika terjadi kegagalan sistem. Sistem seperti ini tidak hanya menawarkan kenyamanan tetapi juga 
memberikan peringatan dini terhadap potensi masalah. Manfaat potensial dari inovasi ini melampaui apa yang awalnya dibayangkan oleh penulis.

## Business Understanding

Tujuan dari bagian ini adalah untuk memperjelas masalah bisnis dan mendefinisikan tujuan proyek.

### Problem Statements
Berikut ini adalah pernyataan masalah yang akan dibahas dalam proyek ini:
- Akses terhadap air minum bersih merupakan tantangan utama di berbagai belahan dunia, termasuk Indonesia.
- Machine Learning memiliki potensi untuk membantu mengatasi tantangan ini dengan mengotomatiskan proses identifikasi mata air dengan kualitas air yang dapat diminum.

### Goals

Berikut adalah tujuan dari proyek ini:
- Mengembangkan model machine learning yang dapat secara akurat memprediksi kualitas air dari mata air.
- Menerapkan model dengan cara yang dapat diakses dan terjangkau oleh masyarakat di negara-negara berkembang.
 

### Solution statements
- Gunakan model machine learning untuk mempelajari hubungan antara kualitas air dan fitur-fitur seperti ph, hardness, dan sebagainya.
- Kembangkan alat yang memungkinkan pengguna untuk mengumpulkan data tentang kualitas air dan mengirimkannya ke model untuk prediksi.

## Data Understanding
Dataset ini berisi pengukuran dan penilaian kualitas air yang terkait dengan potabilitas, yaitu kesesuaian air untuk konsumsi manusia. Tujuan utama dataset ini adalah untuk memberikan wawasan tentang parameter kualitas air dan membantu dalam menentukan apakah air tersebut dapat diminum atau tidak. Setiap baris dalam dataset mewakili sampel air dengan atribut tertentu, dan kolom "Potability" menunjukkan apakah air tersebut layak untuk dikonsumsi.
Dataset yang digunakan untuk proyek ini adalah dataset Water Quality and Potability dari: [Kaggle Dataset](https://www.kaggle.com/datasets/uom190346a/water-quality-and-potability).
Berisi 3276 sampel data.

### Variabel-variabel pada Dataset Water Quality and Potability:
- pH: Tingkat pH air.
- Hardness: Kesadahan air, ukuran kandungan mineral.
- Solids: Total padatan terlarut di dalam air.
- Chloramines: Konsentrasi kloramin di dalam air.
- Sulfate: Konsentrasi sulfat di dalam air.
- Conductivity: Daya hantar listrik air.
- Organic_carbon: Kandungan karbon organik dalam air.
- Trihalomethanes: Konsentrasi trihalometana di dalam air.
- Turbidity: Tingkat kekeruhan, ukuran kejernihan air.
- Potability: Variabel target; menunjukkan potensi air dengan nilai 1 (dapat diminum) dan 0 (tidak dapat diminum).

**Rubrik/Kriteria Tambahan (Opsional)**:
- Penulis melakukan visualisasi data untuk memahami data, berikut adalah hasilnya.
### Univariate Analysis
![univariate.png](image%2Funivariate.png)
### Multivariate Analysis
![multivariate.png](image%2Fmultivariate.png)

## Data Preparation
Train Test Split: Dataset dibagi menjadi satu set pelatihan dan satu set pengujian. Set pelatihan digunakan untuk melatih model, dan set uji digunakan untuk mengevaluasi kinerja model. Pembagiannya adalah 80%-10%, 
dengan 80% data digunakan untuk pelatihan dan 10% digunakan untuk pengujian.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Proses pembagian ini memanfaatkan library dari sklearn, dengan mengimport modul train_test_split
- Train Test Split adalah langkah penting dalam pembelajaran mesin karena memungkinkan model untuk dievaluasi pada data yang belum pernah dilihat sebelumnya. Hal ini membantu untuk memastikan bahwa model tidak overfitting dengan data pelatihan dan 
dapat menggeneralisasi ke data baru.

## Modeling
Penulis menggunakan 5 algoritma machine learning untung membandingkan peforma pada proses prediksi ini, berikut adalah kelima algoritma tersebut:
1. Regresi Logistik: Regresi logistik adalah algoritme klasifikasi yang dapat digunakan untuk memprediksi hasil kategorikal. Algoritme ini bekerja dengan menyesuaikan garis atau kurva pada data, lalu menggunakan garis atau kurva tersebut untuk memprediksi hasil untuk data baru.
2. K-Nearest Neighbors (KNN): KNN adalah algoritme non-parametrik yang dapat digunakan untuk memprediksi hasil kategorikal atau kontinu. Algoritme ini bekerja dengan menemukan k titik data yang paling mirip dengan titik data baru, dan kemudian menggunakan kelas mayoritas dari k titik data tersebut untuk memprediksi hasil untuk titik data baru.
3. Random Forest: Random forest adalah algoritma pembelajaran ensemble yang menggabungkan beberapa pohon keputusan untuk membuat prediksi. Algoritme ini bekerja dengan memilih fitur secara acak dari kumpulan data dan kemudian membangun pohon keputusan untuk setiap fitur. Prediksi dari pohon keputusan kemudian digabungkan untuk membuat prediksi akhir.
4. Naive Bayes: Naive Bayes adalah algoritma probabilistik yang dapat digunakan untuk memprediksi hasil kategorikal. Algoritme ini bekerja dengan mengasumsikan bahwa fitur-fiturnya tidak bergantung satu sama lain.
5. daBoost: AdaBoost adalah algoritma pembelajaran ensembel yang menggabungkan beberapa decision tree untuk membuat prediksi. Algoritme ini bekerja dengan melatih decision tree secara berulang-ulang pada versi data berbobot. Bobot disesuaikan untuk memberikan nilai lebih pada titik data yang salah diklasifikasikan oleh pohon keputusan sebelumnya.

Berikut adalah beberapa kelebihan dan kekurangan dalam algoritma yang digunakan.
### Logistic Regression

* **Kelebihan:**
    * Mudah diinterpretasikan
    * Cepat untuk dilatih
    * Tidak rentan terhadap overfitting
* **Kekurangan:**
    * Tidak dapat menangkap hubungan non-linear antara fitur dan target variable

### K-Nearest Neighbors (KNN)

* **Kelebihan:**
    * Sederhana untuk diterapkan
    * Tidak memerlukan pelatihan
* **Kekurangan:**
    * Sensitif terhadap outlier
    * Membutuhkan banyak memori untuk menyimpan data

### Random Forest

* **Kelebihan:**
    * Akurat dan generalizable
    * Dapat menangkap hubungan non-linear dan kompleks antara fitur dan target variable
* **Kekurangan:**
    * Dapat memakan waktu lama untuk dilatih
    * Sulit untuk diinterpretasikan

### Naive Bayes

* **Kelebihan:**
    * Sederhana untuk diterapkan
    * Cepat untuk dilatih
* **Kekurangan:**
    * Membutuhkan asumsi bahwa fitur-fitur independen satu sama lain

### AdaBoost

* **Kelebihan:**
    * Dapat meningkatkan akurasi model dasar yang lemah
* **Kekurangan:**
    * Dapat rentan terhadap overfitting
    * Membutuhkan banyak memori untuk menyimpan data

Adapun setelah dilakukan modeling, akhirnya diputuskan dengan menggunakan algoritma KNN karena menghasilkan tingkat yang stabil, walaupun akurasi di setiap model cukup rendah
hanya berkisar 60%. Berikut adalah hasil visualisasinya:


## Evaluation
Pada penulisan ini, penulis menggunakan metrik evaluasi akurasi. Dengan cara kerja sebagai berikut:

Akurasi = (TP + TN) / (TP + TN + FP + FN)

Dimana:

* TP: True Positive
* TN: True Negative
* FP: False Positive
* FN: False Negative

Hasilnya bisa dilihat pada gambar berikut:

![output.png](image%2Foutput.png)


Dan visualisasinya:

![model.png](image%2Fmodel.png)

Walaupun Random Forest memiliki tingkat akurasi pada data train yang tinggi sebesar 98%, tetapi pada data test, hasil akurasinya sangat 
rendah. Sehingga ada kemungkinan model ini overfit. Sedangkan hasil yang paling stabil dicapai oleh algoritma KNN sebesar data latih (65%)
dan Data Test (64%), sehingga memilih model ini menjadi cukup masuk akal dibandingkan algoritma lainnya.

Adapun saran perbaikan yang penulis rekomendasikan untuk perbaikan model ini adalah sebagai berikut:
- Meningkatkan jumlah fitur yang digunakan.
- Memperbaiki kualitas fitur yang digunakan.
- Menggunakan model machine learning yang lebih kompleks.
- Melakukan hyperparameter tuning untuk model yang digunakan.
- Menambahkan beberapa teknik untuk preparation data seperti PCA, Standarisasi, dan sebagainya.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.
