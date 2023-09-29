# Laporan Proyek Machine Learning - Bily Hakim Erlangga

![water](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/0569644c-6ec4-4896-befc-7b730852ef31)


## Domain Proyek

Air bersih merupakan kebutuhan pokok manusia dan memiliki peran penting dalam menjaga kesehatan dan kesejahteraan masyarakat. 
Namun, penyediaan air bersih dengan kualitas yang buruk dapat mengakibatkan dampak buruk bagi kesehatan, seperti timbulnya berbagai penyakit. Perubahan kadar pH air juga dapat menyebabkan perubahan bau, rasa, dan warna air. 
Oleh karena itu, penting untuk memiliki sistem pendeteksi air yang dapat memberikan informasi secara digital mengenai kualitas air yang bisa diminum [1].

Saat ini, pendeteksi air bersih layak diminum masih dilakukan secara manual, dengan cara menggunakan cairan kadar pH atau alat ukur. 
Metode ini memiliki beberapa keterbatasan, seperti ketergantungan pada keahlian operator dan waktu yang dibutuhkan untuk melakukan pengukuran. 
Dalam proyek ini, penulis akan mengembangkan sistem pendeteksi air yang menggunakan machine learning untuk memprediksi kualitas air berdasarkan data sensor yang diberikan.

Machine learning adalah bagian dari kecerdasan buatan yang merujuk pada software dan hardware yang dapat menirukan kecerdasan manusia [2]. 
Dalam proyek ini, penulis akan menggunakan algoritma machine learning, seperti _logistic regression_, _KNN_, dan sebagainya, untuk membangun model yang dapat memprediksi kualitas air berdasarkan data sensor yang diberikan.

Dengan adanya sistem pendeteksi air yang menggunakan machine learning, diharapkan dapat meningkatkan efisiensi dan akurasi dalam pendeteksian kualitas air yang bisa diminum. Selain itu, sistem ini juga dapat membantu penduduk yang sulit mendapatkan air bersih dengan memberikan informasi yang lebih akurat dan cepat 
mengenai kualitas air yang tersedia [3]. 
Melalui proyek ini, penulis berharap dapat memberikan kontribusi dalam meningkatkan kualitas hidup masyarakat melalui pemanfaatan teknologi machine learning dalam pendeteksian kualitas air yang bisa diminum.

## Business Understanding

Tujuan dari bagian ini adalah untuk memperjelas masalah bisnis dan mendefinisikan tujuan proyek.

### Problem Statements

1. Apakah pemanfaatan Machine Learning dapat digunakan untuk meningkatkan efisiensi dalam mendeteksi sumber air yang aman untuk diminum?

#### Potensi _Machine Learning_ dalam Mengatasi Masalah
_Machine Learning_ memiliki potensi besar untuk membantu mengatasi tantangan ini dengan mengotomatiskan proses identifikasi mata air dengan kualitas air yang dapat diminum. Dengan memanfaatkan teknologi ini, kita dapat meningkatkan efisiensi dalam mendeteksi sumber air yang aman, 
mengarahkan sumber daya dengan lebih tepat, dan akhirnya memberikan akses air bersih yang lebih baik kepada masyarakat.

### Goals

Berikut adalah tujuan dari proyek ini:
1. Mengembangkan model _machine learning_ yang dapat secara akurat memprediksi kualitas air dari mata air di berbagai wilayah.

### Solution statements
- Penggunaan _Machine Learning_ dalam Solusi: Dalam rangka mencapai tujuan proyek ini, penulis akan menggunakan model machine learning untuk mempelajari hubungan antara kualitas air dan fitur-fitur seperti pH, kekerasan air, dan faktor-faktor lainnya yang memengaruhi kualitas air. Model ini akan digunakan untuk mengidentifikasi sumber air yang dapat diandalkan dan aman untuk dikonsumsi.
- Eksplorasi Berbagai Macam Algoritma Machine Learning: Penulis akan melakukan eksplorasi yang mendalam dengan menggunakan berbagai macam algoritma Machine Learning, termasuk hingga 5 algoritma yang berbeda, untuk menciptakan model prediksi kelayakan air minum yang optimal. Dengan melakukan pendekatan ini, penulis akan memastikan bahwa penulis memilih algoritma terbaik yang sesuai dengan data, sehingga meningkatkan akurasi dan keandalan model. Pendekatan ini juga memungkinkan untuk memaksimalkan potensi Machine Learning dalam proyek ini dan menghasilkan hasil yang optimal bagi masyarakat yang membutuhkan akses air bersih yang aman.

## Data Understanding
Dataset ini berisi pengukuran dan penilaian kualitas air yang terkait dengan potabilitas, yaitu kesesuaian air untuk konsumsi manusia. Tujuan utama dataset ini adalah untuk memberikan wawasan tentang parameter kualitas air dan membantu dalam menentukan apakah air tersebut dapat diminum atau tidak. Setiap baris dalam dataset mewakili sampel air dengan atribut tertentu, dan kolom "Potability" menunjukkan apakah air tersebut layak untuk dikonsumsi. Dataset ini berasal dari kaggle [Water Quality and Potability](https://www.kaggle.com/datasets/uom190346a/water-quality-and-potability) berisi 3276 sampel, dengan beberapa kondisi missing value pada kolom _ph_ sebesar **491** data, lalu _sulfate_ **781** data, dan _Trihalomethanes_ **162** data. Berisi 10 kolom penting, dengan 9 kolom fitur dan 1 kolom target (_Potability_).

### Variabel-variabel pada Dataset Water Quality and Potability:
- **pH (Tingkat pH air)**: Contoh konkret pengukuran pH dalam dataset ini adalah 6.8, 7.2, dll.
- **Hardness (Kesadahan air)**: Kesadahan air diukur dalam miligram per liter (mg/L), dengan contoh konkret seperti 214.3, 181.1, dll.
- **Solids (Total padatan terlarut di dalam air)**: Ukuran total padatan terlarut di dalam air diukur dalam ppm (part per million), dengan contoh seperti 20791.3, 18600.0, dll.
- **Chloramines (Konsentrasi kloramin di dalam air)**: Konsentrasi kloramin diukur dalam ppm, dengan contoh konkret seperti 8.8, 6.5, dll.
- **Sulfate (Konsentrasi sulfat di dalam air)**: Konsentrasi sulfat diukur dalam ppm, dengan contoh seperti 368.4, 356.8, dll.
- **Conductivity (Daya hantar listrik air)**: Daya hantar listrik air diukur dalam mikrosiemen per centimeter (µS/cm), dengan contoh konkret seperti 564.0, 658.8, dll.
- **Organic_carbon (Kandungan karbon organik dalam air)**: Kandungan karbon organik dalam air diukur dalam ppm, dengan contoh seperti 14.2, 8.8, dll.
- **Trihalomethanes (Konsentrasi trihalometana di dalam air)**: Konsentrasi trihalometana diukur dalam ppm, dengan contoh seperti 86.990970, 56.329076, dll.
- **Turbidity (Tingkat kekeruhan, ukuran kejernihan air)**: Tingkat kekeruhan diukur dalam NTU (Nephelometric Turbidity Units), dengan contoh konkret seperti 2.963135, 3.055934, dll.
- **Potability (Variabel target)**: Variabel ini menunjukkan potensi air dengan nilai 1 (dapat diminum) dan 0 (tidak dapat diminum).

### Univariate Analysis

![pink](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/b0e587b3-bf32-4d0f-8be0-d19d67246e72)

Gambar diatas, menunjukan jumlah data pada target, dimana datanya tidak berimbang, dengan persebaran data bernilai 0 (Air tidak layak minum) sebesar 1600 an dan 1 (Layak Minum) sebesar 1000 an.

---

Lalu, bisa ditelusuri masing-masing fitur

![1](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/bd08928c-5989-4a3b-9d13-e67586040eb9)

Bisa dilihat bahwa nilai ph untuk air layak minum di dominasi dengan ph 7

![2](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/9e74c0e0-0164-4df0-9e1a-a7bc6df09090)

Lalu dengan berfokus pada data air layak minum terhadap kesadahan air berada di rentang 180 - 220. Walaupun data air tidak layak minum juga tinggi di rentang yang sama. Hal ini bisa dikomunikasikan lebih lanjut ke _Subject Matter Expert_ (SME)

![3](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/1aea3e08-640b-4aa6-bca9-4dcc1cb86725)

Pada fitur ketiga, target disandingkan dengan solids, rentang persebaran data layak minum berada diantara 1500 an sampai 2000 an.

![4](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/42c9d068-ee6d-4df8-ba22-fe19f983acb7)

Selanjutnya, gambar diatas menunjukan distribusi chloramines dengan persebaran yang bisa anda lihat sebagai berikut.

![5](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/057eda31-4f5d-4fcf-b7ba-635a3ef597a9)

![6](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/c04f15df-afc7-46bf-b24a-7af65c1f7302)

![7](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/35c0c09a-bca2-4b52-9220-751d6f6dd23c)

![8](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/283cb7ee-e4e8-4567-b497-6a2ccf2e9a0a)

![9](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/670230b5-6651-4392-89e5-07cc7554a802)


Berdasarkan grafik tersebut, dapat ditarik beberapa kesimpulan sebagai berikut:
- Tingkat kelayakan minum air umumnya semakin tinggi seiring dengan meningkatnya nilai pH.
- Air dengan nilai pH di bawah 7 dianggap tidak layak minum, sedangkan air dengan nilai pH di atas 7 dianggap layak minum.
- Air dengan nilai pH 7 dianggap ideal untuk minum.

## Data Preparation
Pada tahap ini, dataset akan dibagi menjadi dua set utama: satu set pelatihan dan satu set pengujian. Pembagian ini penting untuk melatih model dan kemudian menguji kinerjanya. Tujuannya adalah untuk memastikan bahwa model yang dikembangkan mampu menggeneralisasi dengan baik ke data yang belum pernah dilihat sebelumnya dan tidak overfitting dengan data pelatihan.

### Train Test Split
Langkah-langkah yang dilakukan dalam proses pembagian data adalah sebagai berikut:

- Import Library: Penulis akan memanfaatkan library scikit-learn (sklearn). Modul ini memudahkan penulis dalam membagi dataset menjadi set pelatihan dan set pengujian.
- Pembagian Data: Penulis akan melakukan pembagian dataset dengan proporsi 90% untuk set pelatihan dan 10% untuk set pengujian. Proses ini dilakukan secara acak untuk memastikan representasi yang baik dari data.
- Penggunaan Data: Set pelatihan akan digunakan untuk melatih model Machine Learning, sedangkan set pengujian akan digunakan untuk menguji kinerja model dan mengukur sejauh mana model dapat melakukan prediksi dengan baik pada data yang belum pernah dilihat sebelumnya.

### Menangani Missing Value
Dalam langkah pre-processing data, penulis telah melakukan pengisian nilai yang hilang (missing values) dengan menggunakan metode mean (nilai rata-rata) dari setiap atribut yang memiliki nilai yang hilang. Hal ini akan memastikan bahwa data yang digunakan untuk melatih 
dan menguji model adalah data yang lengkap dan siap digunakan dalam pengembangan model Machine Learning.

Langkah ini membantu memastikan bahwa tidak ada informasi yang hilang dalam dataset yang dapat memengaruhi kinerja model. Dengan data yang sudah terisi lengkap, penulis 
dapat lebih percaya diri dalam melatih model dan menguji kemampuannya untuk melakukan prediksi dengan akurat.

## Modeling
Penulis memilih 5 algoritma tersebut karena tugas ini termasuk kedalam tugas klasifikasi 2 kelas. 5 Algoritma dibawah merupakan algoritma yang cukup populer dan umum digunakan untuk menyelesaikan permasalahan klasifikasi dan banyak referensi yang beredar sehingga memudahkan penulis untuk membuat modelnya. Berikut adalah kelima algoritma yang dimaksud:

1. _Regresi Logistik_: Regresi logistik adalah algoritme klasifikasi yang dapat digunakan untuk memprediksi hasil kategorikal. Algoritme ini bekerja dengan menyesuaikan garis atau kurva pada data, lalu menggunakan garis atau kurva tersebut untuk memprediksi hasil untuk data baru.
2. _K-Nearest Neighbors_ (KNN): KNN adalah algoritme non-parametrik yang dapat digunakan untuk memprediksi hasil kategorikal atau kontinu. Algoritme ini bekerja dengan menemukan k titik data yang paling mirip dengan titik data baru, dan kemudian menggunakan kelas mayoritas dari k titik data tersebut untuk memprediksi hasil untuk titik data baru.
3. _Random Forest_: _Random forest_ adalah algoritma pembelajaran ensemble yang menggabungkan beberapa pohon keputusan untuk membuat prediksi. Algoritme ini bekerja dengan memilih fitur secara acak dari kumpulan data dan kemudian membangun pohon keputusan untuk setiap fitur. Prediksi dari pohon keputusan kemudian digabungkan untuk membuat prediksi akhir.
4. _Naive Bayes_: _Naive Bayes_ adalah algoritma probabilistik yang dapat digunakan untuk memprediksi hasil kategorikal. Algoritme ini bekerja dengan mengasumsikan bahwa fitur-fiturnya tidak bergantung satu sama lain.
5. _AdaBoost_: _AdaBoost_ adalah algoritma pembelajaran ensembel yang menggabungkan beberapa decision tree untuk membuat prediksi. Algoritme ini bekerja dengan melatih decision tree secara berulang-ulang pada versi data berbobot. Bobot disesuaikan untuk memberikan nilai lebih pada titik data yang salah diklasifikasikan oleh pohon keputusan sebelumnya.

Berikut adalah beberapa kelebihan dan kekurangan dalam algoritma yang digunakan.

### Logistic Regression

* **Kelebihan:**
    * Mudah diinterpretasikan
    * Cepat untuk dilatih
    * Tidak rentan terhadap overfitting
* **Kekurangan:**
    * Tidak dapat menangkap hubungan non-linear antara fitur dan target variable

#### Parameter yang digunakan:

- _solver_: Ini digunakan untuk menyelesaikan masalah optimasi yang mendasari model _Logistic Regression_. Penulis telah mengaturnya ke 'liblinear', yang merupakan salah satu solver yang cocok untuk data yang relatif kecil.
- _class_weight_: Parameter ini digunakan untuk menanganan ketidakseimbangan kelas. Penulis mengaturnya ke 'balanced', yang akan memberikan bobot yang seimbang pada kelas-kelas yang berbeda dalam kasus kelas yang tidak seimbang.

### K-Nearest Neighbors (KNN)

* **Kelebihan:**
    * Sederhana untuk diterapkan
    * Tidak memerlukan pelatihan
* **Kekurangan:**
    * Sensitif terhadap outlier
    * Membutuhkan banyak memori untuk menyimpan data

#### Parameter yang digunakan:

- _n_neighbors_: Ini adalah parameter yang menentukan jumlah tetangga terdekat yang akan digunakan oleh model untuk melakukan prediksi. Penulis mengaturnya ke 10, yang berarti model _KNN_ akan mempertimbangkan 10 tetangga terdekat saat melakukan prediksi.

### Random Forest

* **Kelebihan:**
    * Akurat dan generalizable
    * Dapat menangkap hubungan non-linear dan kompleks antara fitur dan target variable
* **Kekurangan:**
    * Dapat memakan waktu lama untuk dilatih
    * Sulit untuk diinterpretasikan

#### Parameter yang digunakan:

- _n_estimators_: Ini adalah jumlah pohon keputusan yang akan digunakan dalam model _Random Forest_. Penulis mengaturnya ke 60, yang berarti model akan menggunakan 60 pohon keputusan dalam ensemble.
- _max_depth_: Parameter ini mengontrol kedalaman maksimum setiap pohon keputusan dalam ensemble. Penulis mengaturnya ke 20, yang berarti kedalaman maksimum setiap pohon adalah 20.
- _random_state_: Ini adalah biji acak yang digunakan untuk membuat model dapat direproduksi. Penulis mengaturnya ke 55, yang akan memastikan bahwa hasilnya konsisten setiap kali menjalankan model.
- _n_jobs_: Parameter ini mengontrol jumlah pekerjaan yang akan dijalankan secara paralel saat membangun pohon-pohon dalam model Random Forest. Penulis mengaturnya ke -1, yang berarti model akan menggunakan semua core CPU yang tersedia untuk mempercepat pelatihan model.

### Naive Bayes

* **Kelebihan:**
    * Sederhana untuk diterapkan
    * Cepat untuk dilatih
* **Kekurangan:**
    * Membutuhkan asumsi bahwa fitur-fitur independen satu sama lain

#### Parameter yang digunakan:

- Default

### AdaBoost

* **Kelebihan:**
    * Dapat meningkatkan akurasi model dasar yang lemah
* **Kekurangan:**
    * Dapat rentan terhadap overfitting
    * Membutuhkan banyak memori untuk menyimpan data

#### Parameter yang digunakan:

- _learning_rate_: Ini adalah laju pembelajaran yang digunakan dalam proses boosting. Penulis mengaturnya ke 0.05, yang berarti setiap model base (biasanya pohon keputusan) dalam ensemble akan memiliki dampak yang lebih kecil terhadap model akhir.
- _random_state_: Ini adalah biji acak yang digunakan untuk membuat model dapat direproduksi. Penulis mengaturnya ke 55, yang akan memastikan bahwa hasilnya konsisten setiap kali menjalankan model.

## Evaluation
Pada penulisan ini, penulis menggunakan metrik evaluasi akurasi. Cara kerja akurasi sebagai berikut:

$$
\text{Akurasi} = \frac{TP + TN}{TP + TN + FP + FN}
$$

Deskripsi Komponen:

    TP: True Positive
    TN: True Negative
    FP: False Positive
    FN: False Negative


Hasilnya bisa dilihat pada tabel berikut:

| Model        | Training Accuracy | Testing Accuracy |
|--------------|-------------------|------------------|
| Logre        | 0.5131            | 0.5019           |
| KNN          | 0.6594            | 0.6479           |
| RF           | 1.0               | 0.6816           |
| NaiveBayes   | 0.6190            | 0.6367           |
| Boosting     | 0.6244            | 0.6479           |


Dan visualisasinya:

![visualisasi](https://github.com/Cybercanda/submission-mlterapan-1/assets/113665438/fb61e415-ad0c-4233-a9a7-af1cb15e3f89)

- Random Forest (RF) memiliki akurasi tertinggi pada data pengujian, yaitu 0.6816. Namun, akurasi yang sempurna (1.0) pada data pelatihan menunjukkan kemungkinan overfitting.
- K-Nearest Neighbors (KNN) juga memiliki akurasi yang cukup baik pada data pengujian (0.6479) dan tidak menunjukkan tanda-tanda overfitting.
- Naive Bayes (NaiveBayes) memiliki akurasi yang cukup baik pada data pengujian (0.6367).
- AdaBoost (Boosting) juga memiliki akurasi yang sebanding dengan KNN pada data pengujian (0.6479).
- Logistic Regression (Logre) memiliki akurasi yang lebih rendah di antara semua model (0.5019 pada data pengujian).

Secara umum, dalam situasi ini, model _Random Forest_ (RF) mungkin dianggap sebagai model terbaik berdasarkan akurasi pada data pengujian, namun
model yang dihasilkan terlalu ideal sehingga ada indikasi bahwa model tersebut mengalami overfitting dan pada saat testing, hanya mendapatkan akurasi
sebesar 68%. Penulis menyimpulkan bahwa, _KNN_ adalah model yang tepat, karena menghasilkan akurasi kedua paling tinggi setelah _RF_ sebesar 65%
dan akurasi pada data testing 64%.

### Kesimpulan

Dalam proyek ini, penulis menjelajahi penggunaan algoritma _machine learning_ untuk memprediksi kualitas air yang dapat diminum berdasarkan data yang tersedia. Penulis juga mengidentifikasi tantangan akses air bersih di Indonesia dan potensi _machine learning_ untuk mengotomatisasi identifikasi mata air dengan kualitas air yang dapat diminum. 

Dan juga berhasil mengimplementasikan teknik _machine learning_ dan memilih yang terbaik untuk mengidentifikasi air layak minum, yakni dengan menggunakan algoritma _random forest_. Hasil ini sesuai dengan tujuan yang telah ditetapkan sebelumnya. 

Adapun beberapa saran perbaikan yang disarankan penulis adalah sebagai berikut:
- Pertimbangkan penambahan fitur yang lebih relevan.
- Menyeimbangkan data target.
- Lakukan pemrosesan data lebih lanjut seperti normalisasi atau standarisasi data.
- Eksplorasi model machine learning yang lebih kompleks atau perangkat ensambel yang dapat meningkatkan kinerja.
- Lakukan hyperparameter tuning untuk mengoptimalkan parameter model yang digunakan.
- Terapkan teknik pra-pemrosesan data seperti PCA (Principal Component Analysis) jika diperlukan.

**---Ini adalah bagian akhir laporan---**

## Referensi
[1] [Ramadhan, F., Nugraha, A. R., Ridwan, M., Ilham, M., & Hidayat, M. A.] (2020). **Prediksi kualitas air mata air di Indonesia menggunakan algoritma machine learning**. **Jurnal Informatika IKRA-ITH**, **6**(1), 1-10.

[2] Lofandri, Wiki. "Analisis Prediksi Pemeliharaan Peralatan Lab Berbasis Machine Learning." Tesis, Universitas Putra Indonesia "YPTK", 2022.

[3] Febrianti, Fitri. "Implementasi IoT(Internet of Things) Monitoring Kualitas Air dan Sistem Administrasi Pada Pengelola Air Bersih Skala Kecil." Skripsi, Institut Teknologi Nasional Malang, 2021.

## Score from Dicoding

**5 of 5 stars**

![Score.png](image%2FScore.png)

Detail penilaian submission:

Submission Anda akan dinilai oleh reviewer dengan skala 1-5 berdasarkan parameter berikut. 

    Bintang 1: Semua ketentuan terpenuhi, tetapi terdapat indikasi plagiat dengan menggunakan proyek orang lain dan hanya mengubah kontennya saja.
    Bintang 2: Semua ketentuan terpenuhi, tetapi penulisan kode dan laporan berantakan.
    Bintang 3: Semua ketentuan terpenuhi, penulisan kode, dan laporan cukup baik.
    Bintang 4: Semua ketentuan terpenuhi, menerapkan minimal tiga (3) kriteria Rubrik Penilaian Tambahan pada laporan.
    Bintang 5: Semua ketentuan terpenuhi, menerapkan minimal seluruh kriteria (6) Rubrik Penilaian Tambahan pada laporan.
