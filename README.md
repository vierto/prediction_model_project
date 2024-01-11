# Project Prediction Model (MySkill.id) by Vendly

The algorithms used to predict the data are Logistic Regression, Gradient Boosting, and Random Forest.

## Problem Statement

Kekhawatiran adanya keterlambatan pembayaran kartu kredit pada FinanKu yang akan merugikan bisnis. Sehingga orang-orang yang memiliki potensi untuk mengalami keterlambatan bayar bisa diprediksi lebih cepat untuk menentukan strategi yang sesuai dalam menghadapi kondisi di masa mendatang.

## Objective

Membuat sebuah model yang dapat memprediksi setidaknya 60% dari pelanggan yang akan mengalami telat bayar kartu kredit [Accuracy & Recall di atas 60%]

## Variabel Yang Tersedia

Dari dataset yang dimiliki terdapat beberapa data yang tersedia:
1. <b>Customer ID:</b> Unique ID Customer
2. <b>Branch:</b> Lokasi Cabang Nasabah Terdaftar
3. <b>City:</b> Lokasi Kota Nasabah Terdaftar
4. <b>Age:</b> Umur Nasabah Pada Periode Observasi
5. <b>Avg. Annual Income/Month:</b> Rata-rata penghasilan nasabah dalam satu tahun
6. <b>Balance (Q1-Q4):</b> Saldo mengendap yang dimiliki nasabah di akhir kuartal
7. <b>Num of Products (Q1-Q4):</b> Jumlah kepemilikan produk nasabah di akhir kuartal
8. <b>HasCrCard (Q1-Q4):</b> Status kepemilikan produk kartu kredit nasabah di akhir kuartal
9. <b>Active Member (Q1-Q4):</b> Status keaktifan nasabah
10. <b>Unpaid Tagging:</b> Status nasabah gagal bayar

## Eksperimen

Periode Tinjauan:
1. Nasabah direview selama satu tahun terakhir
2. Nasabah direview selama 6 bulan terakhir

Penyesuaian Variabel:
1. Balance dilihat dari rata-rata selama horizon waktu & dilihat perubahan pada akhir tinjauan dan awal tinjauan
2. Melihat kepemilikan jumlah produk dari rata-rata, maksimum, dan minimum pada periode tinjauan
3. Status keaktifan nasabah dilihat dalam bentuk bulan

## Kesimpulan dari Prediction Model

Dari semua model, rata-rata memiliki <i>accuracy</i> di atas 60% dan <i>recall</i> di bawah 60% yaitu sekitar 30%-40%. Maka dari itu berdasarkan data <i>accuracy</i> dan juga <i>recall</i>, masih banyak nasabah yang sebenarnya berpotensi gagal bayar namun diprediksi tidak gagal bayar. Sehingga bisa disampaikan bahwa dalam iterasi pembangunan model ini masih belum mencapai <i>objective</i> yang diinginkan.

Solusi pengembangan selanjutnya yang dapat dilakukan diantaranya:
1. Memperbanyak <i>sample</i> (jumlah nasabah dengan asumsi <i>datasets</i> yang tersedia saat ini bukan merupakan total populasi nasabah)
2. Melakukan oversampling terhadap kelas minoritas (gagal bayar) agar pembangunan model tidak bias
3. Memperluas horizon waktu
4. Mencoba variasi variabel lainnya (menambah variabel baru, atau membuang variabel yang memiliki nilai importance rendah pada hasil terakhir)
5. Mencoba algoritma <i>supervised machine learning</i> lainnya
