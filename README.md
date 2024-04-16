# Tugas 3 Machine Learning
## Nama : Ichwanul Fata
## NPM : 2108107010035

## Cara Menjalankan Kode Program
1. Membuat virtual enviroment di dalam repository ini.
2. Aktifkan virtual environment pada terminal dalam lingkungan kode.
3. Install semua library yang ada dalam file requirements.txt.
4. Jalankan semua cell yang ada pada file notebook tersebut 

## Poin 1
### Deskripsi Dataset
Dataset yang digunakan terkait dengan tingkat keluarnya nasabah (churn rate) dari suatu bank di Eropa. Bank tersebut memiliki permasalahan dimana secara tiba-tiba tingkat tingkat keluarnya nasabah (churn rate) meningkat drastis. Pada data tersebut memiliki 13 kolom feature serta 1 kolom label yaitu kolom exited. Berikut penjelasan dari tiap-tiap kolom.

  1. RowNumber menunjukkan ia baris ke berapa.
  2. CustomerId adalah identitas unik setiap costumer.
  3. Surname adalah nama belakang pelanggan.
  4. CreditScore adalah skor kredit yang diberikan oleh bank. Hanya bank yang tahu cara menghitung skor ini.
  5. Geography adalah negara domisili nasabah.
  6. Gender adalah jenis kelamin.
  7. Age adalah usia.
  8. Tenure adalah berapa lama (dalam tahun) mereka sudah menjadi nasabah bank.
  9. Balance adalah tabungan nasabah saat ini (atau saat terakhir sebelum keluar sebagai nasabah).
  10. NumberOfProduct adalah berapa banyak produk bank yang dimiliki oleh nasabah pada saat ini (atau saat terakhir).
  11. HasCrCard adalah kondisi apakah saat ini nasabah memiliki kartu kredit di bank ini (1) atau tidak (0).
  12. IsActiveMember adalah kondisi apakah pelanggan saat ini aktif (1) menjadi member aktif atau tidak (0). Hanya bank yang tahu cara membuat status ini, misal apakah nasabah aktif melakukan transaksi di bulan terakhir, apakah memiliki pinjaman di bulan terakhir, dan seterusnya.
  13. EstimatedSalary adalah estimasi gaji yang dibuat oleh bank. Tentu saja bank tidak tahu gaji asli dari nasabah, tapi bank sudah membuat perkiraan gaji berdasarkan pola keluar masuknya uang nasabah tersebut.
  14. Exited adalah status apakah nasabah ini tetap di bank (0) atau keluar dari bank (1).
      
Permasalahan tersebut akan diselesaikan menggunakan salah satu algoritma klasifikasi yaitu artificial neural network (ANN).
### Tahapan Pengerjaan
1. Import Library
2. Import Data
3. Memilih Variabel X dan Y
4. Encoding Data
5. Splitting Data
6. Feature Scaling
7. Inisialisasi Model ANN
8. Training Model ANN
9. Testing dan Melihat Akurasi Model ANN

    
## Poin 2
### ANN dan SVM
#### Deskripsi Dataset
Untuk melakukan klasifikasi menggunakan SVM dan ANN ini, saya menggunakan dataset rice (Cammeo and Osmancik). Pada dataset ini memiliki 8 kolom yaitu :

  1. Area : Jumlah piksel dalam batas butir beras
  2. Perimeter : Menghitung keliling dengan menghitung jarak antar piksel di sekitar batas butiran beras
  3. Major_Axis_Length : Garis terpanjang yang dapat ditarik pada butiran beras, yaitu jarak sumbu utama
  4. Minor_Axis_Length : Garis terpendek yang dapat digambar pada butiran beras, yaitu jarak sumbu yang kecil,
  5. Eccentricity : Mengukur seberapa bulat elips, yang memiliki momen yang sama dengan butiran beras
  6. Convex_Area : Jumlah piksel cangkang cembung terkecil di wilayah yang dibentuk oleh butiran beras
  7. Extent : Rasio wilayah yang dibentuk oleh butiran beras terhadap kotak pembatas
  8. Class : Label yaitu Cammeo dan Osmancik
     
Dataset tersebut memiliki label yaitu pada kolom Class sedangkan kolom lainnya akan digunakan sebagai atribut/feature. Dataset tersebut memiliki jumlah field sebanyak 3810.

Link sumber dataset : https://archive.ics.uci.edu/dataset/545/rice+cammeo+and+osmancik

#### Tahapan Pengerjaan
1. Import Library
2. Import Data
3. Data Preprocessing : Mengubah class menjadi numerik, handling missing value, handling outlier, handling imbalance data, dan feature scaling.
4. Memilih Variabel X dan Y
5. Splitting Data
6. Inisialisasi Model ANN
7. Training Model ANN
8. Testing dan Melihat Akurasi Model ANN
9. Training Model SVM
10. Testing dan Melihat Akurasi Model SVM
    
#### Perbandingan Hasil Akurasi 
Hasil akurasi menggunakan metric evaluasi akurasi setelah model selesai dibangun yaitu :

Model ANN yang dihasilkan memiiliki akurasi sebesar 0.9243

Model SVM Linear yang dihasilkan memiliki akurasi sebesar 0.9243

Model SVM Non-Linear yang dihasilkan memiliki akurasi sebesar 0.9251


Saat sedang berlangsungnya training model ANN terdapat beberapa perubahan akurasi yaitu

Epoch 7/100

306/306 [==============================] - 0s 1ms/step - loss: 0.2106 - accuracy: 0.9243

Epoch 8/100

306/306 [==============================] - 0s 2ms/step - loss: 0.2026 - accuracy: 0.9273

Epoch 9/100

306/306 [==============================] - 1s 2ms/step - loss: 0.1968 - accuracy: 0.9286

Epoch 10/100

306/306 [==============================] - 0s 999us/step - loss: 0.1932 - accuracy: 0.9276

Epoch 11/100

306/306 [==============================] - 0s 732us/step - loss: 0.1892 - accuracy: 0.9318

Epoch 12/100

306/306 [==============================] - 0s 858us/step - loss: 0.1878 - accuracy: 0.9299


Berdasarkan output tersebut dapat dilihat bahwa nilai akurasi cenderung diantara 0.93 sehingga dapat disimpulkan bahwa model ANN memberikan akurasi yang lebih baik dibandingkan dengan SVM.

### ANN dan SVR
#### Deskripsi Dataset
Untuk melakukan pemodelan regresi menggunakan ANN dan SVR, saya menggunakan dataset Stroke Prediction. Pada dataset ini memiliki 12 kolom yaitu :

  1. id : Identifier yang unik
  2. gender : Jenis Kelamin
  3. age : Umur
  4. hypertension : Menderita hipertensi atau tidak
  5. heart_disease : Mengidap penyakit jantung atau tidak
  6. ever_married : Status Pernikahan ( Ya atau Tidak)
  7. work_type : Tipe Pekerjaan
  8. residence_type : TIpe Tempat Tinggal
  9. avg_glucose_level : Rata-rata kadar glukosa dalam darah
  10. bmi : Body mass index / indeks massa tubuh
  11. smooking_status : Status merokok
  12. stroke : Terkena Stroke atau tidak

Dari keseluruhan kolom yang ada pada dataset tersebut saya hanya menggunakan tiga kolom yakni kolom age, BMI dan avg_glucose_level. Age dan avg_glucose_level merupakan variabel independen yang akan dilihat hubungannya dengan variabel dependen yaitu BMI. Dataset tersebut memiliki jumlah field sebanyak 5110.

Link Sumber Dataset : https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset

#### Tahapan Pengerjaan
1. Import Library
2. Import Data
3. Data Preprocessing : Handling missing value, handling imbalance data, dan feature scaling.
4. Memilih Variabel X dan Y
5. Splitting Data
6. Inisialisasi Model ANN
7. Training Model ANN
8. Testing dan Melihat MSE Model ANN
9. Training Model SVR
10. Testing dan Melihat MSE Model SVR
    
#### Perbandingan Hasil Akurasi 
Hasil akurasi menggunakan metric evaluasi MSE setelah model selesai dibangun yaitu :

Model ANN yang dihasilkan memiiliki MSE sebesar 0.007782708362124884

Model SVR Linear yang dihasilkan memiliki MSE sebesar 0.0069007297115937696

Model SVR Non-Linear yang dihasilkan memiliki MSE sebesar 0.005730613337438222


Berdasarkan output tersebut dapat dilihat bahwa model SVR menghasilkan model yang lebih baik daripada SVR. 
