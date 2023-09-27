# Laporan Proyek Machine Learning - Bily Hakim Erlangga

![water.jpg](image%2Fwater.jpg)
## Domain Proyek

Air minum adalah kebutuhan mutlak untuk manusia bertahan hidup, terlebih tubuh manusia terdiri dari air sebesar 70%. Kekurangan air akan sangat mempengaruhi 
kondisi tubuh yang tidak disarankan oleh siapapun praktisi kesehatan. Berikut adalah beberapa dampak yang terjadi jika tubuh kekurangan air ([Dampak Kurang Minum Air Putih](https://yankes.kemkes.go.id/view_artikel/2638/dampak-kurang-minum-air-putih)):

1. Sistem Imun yang melemah
2. Sangat sulit untuk berfokus
3. memicu mood yang menjadi buruk (Bad Mood)
4. Tekanan darah menurun
5. Dan masih banyak lagi

Diikuti juga dengan perkembangan teknologi informasi, terutama dalam bidang machine learning. Penulis menyadari bahwa dalam bidang kesehatan 
bisa dilakukan kolaborasi antar studi guna memudahkan manusia. menurut paper javaid dkk ([Significance of machine learning in healthcare ...](https://www.sciencedirect.com/science/article/pii/S2666603022000069))
bahwa implementasi machine learning dalam layanan kesehatan, memberikan dampak yang positif. 

Selain dari hal tersebut, mengutip dari Perserikatan Bangsa Bangsa (PBB) pada tahun 2019 mencatat bahwa 1/4 populasi dunia atau 2.2 milyar masih kekurangan air yang layak untuk diminum ([1 in 3 people globally do not have ...](https://www.sciencedirect.com/science/article/pii/S2666603022000069)).
Di Indonesia sendiri, menurut Bappenas, ketersediaan air di beberapa bagian pulau jawa dan bali sudah tergolong langka. Hal ini lah yang menjadikan penulis memiliki ide
untuk membuat sistem seperti ini. penulis menyadari, bahwa solusi yang ditawarkan penulis bukan tentang solusi langsung dari kelangkaan air layak minum,
tapi ide besarnya, bagaimana bisa membuat suatu alat yang otomatis menemukan mata air yang memiliki kualitas air yang dapat diminum.

Sistem ini dibuat dengan memanfaatkan teknologi machine learning, bagaimana ia bisa menghasilkan prediksi kelayakan suatu air dengan indikator nilai 1 untuk layak diminum dan 0 untuk tidak layak.

Dari sisi bisnis, hal ini juga bisa disematkan dalam sebuah dispenser yang mengubah air keran menjadi air minum layak, agar menambahkan sensor yang terhubung kedalam perangkat iot
dan menyampaikan notifikasi apabila air yang dihasilkan dispenser tersebut mengalami kegagalan sistem, sehingga memberikan peringatan awal. Dan masih banyak manfaat lainnya
yang luput dari perhatian penulis.

## Business Understanding

Pada bagian ini, kamu perlu menjelaskan proses klarifikasi masalah.

Bagian laporan ini mencakup:

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
- Pernyataan Masalah 1
- Pernyataan Masalah 2
- Pernyataan Masalah n

### Goals

Menjelaskan tujuan dari pernyataan masalah:
- Jawaban pernyataan masalah 1
- Jawaban pernyataan masalah 2
- Jawaban pernyataan masalah n

Semua poin di atas harus diuraikan dengan jelas. Anda bebas menuliskan berapa pernyataan masalah dan juga goals yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Menambahkan bagian “Solution Statement” yang menguraikan cara untuk meraih goals. Bagian ini dibuat dengan ketentuan sebagai berikut: 

    ### Solution statements
    - Mengajukan 2 atau lebih solution statement. Misalnya, menggunakan dua atau lebih algoritma untuk mencapai solusi yang diinginkan atau melakukan improvement pada baseline model dengan hyperparameter tuning.
    - Solusi yang diberikan harus dapat terukur dengan metrik evaluasi.

## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.
