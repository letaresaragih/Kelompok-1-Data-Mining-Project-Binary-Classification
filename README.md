# Kelompok-1-Data-Mining-Project-Binary-Classification

## Fraud Detection of Badan Jaminan Kesehatan Masyarakat Hackathon Dataset Using Random Forest Classification 

### 1. BUSINESS UNDERSTANDING

##### Business Objective: 

Rumah sakit merupakan salah satu instansi yang bergerak sebagai pelayanan kesehatan bagi masyarakat. Dalam melaksanakan proses bisnisnya, peran BPJS cukup besar dalam mempengaruhi kualitas pelayanan bagi masyarakat. Namun dengan semakin banyak penggunaan BPJS Kesehatan, tidak jarang terjadi beberapa kecurangan (fraud) yang ditujukan untuk menguntungkan pihak tertentu. Pelaku yang terlibat bisa jadi adalah peserta BPJS Kesehatan, fasilitator kesehatan atau pembeli layanan kesehatan, penyedia obat dan alat kesehatan, dan pemangku kepentingan lainnya. Penanganan terkait masalah tersebut menjadi concern yang perlu untuk diatasi yang bertujuan untuk dapat mencegah dan mendeteksi berbagai indikasi potensi kecurangan sedini dan sesedikit mungkin. Sehingga dengan demikian biaya pelayanan kesehatan dapat dimanfaatkan semaksimal mungkin dalam memenuhi kepentingan dan pelayanan yang maksimal bagi masyarakat, serta untuk tetap menjaga sustainability BPJS Kesehatan.

##### Goal

Melakukan prediksi potensi terjadinya penyimpangan (fraud) pada klaim pelayanan Rumah Sakit.

##### Plan 

Melakukan tahapan data mining sesuai dengan metodologi data science CRISP-DM

![crisp-dm](https://user-images.githubusercontent.com/60679684/144963018-c82be1bc-6408-4b48-8f3f-2e024ddc0d4b.png)

### 2. DATA UNDERSTANDING

Memuat informasi BPJS Kesehatan yang merupakan data publik mengenai aturan penamaan dan kesehatan 
secara umum. Data yang digunakan berukuran 10611501 dimana terdiri dari 200217 observasi dan 53 variabel dan memiliki proporsi kelas label pada data seimbang. 

Visualisasi fitur dengan histogram: 

![histogram](https://user-images.githubusercontent.com/60679635/144964154-0c6798db-9a48-485c-9172-ff3978b58fed.jpeg)

Visualisasi heatmap untuk melihat korelasi setiap fitur:

![heatmap](https://user-images.githubusercontent.com/60679635/144964175-2faac2d3-e795-49e8-8ae2-56b314af3044.jpeg)

### 3. DATA PREPARATION
Data Preparation merupakan proses apa saja yang akan dilakukan untuk mempersiapkan data seperti sorting, cleaning, construction, binning dan normalization.
1. Sorting Data:
Fase sorting merupakan tahapan untuk melakukan pemilihan pada atribut yang akan digunakan. Atribut yang tidak digunakan akan di drop.

2. Cleaning Data:
Fase ini merupakan tahapan untuk melakukan pembersihan data. Pembersihan data yang dilakukan adalah menangani objek data yang kosong (missing value).

3. Construct Data:
Fase ini merupakan tahapan untuk melakukan konstruksi pada data. Adapun konstruksi yang dilakukan adalah transformasi atribut dengan tipe kategorik menjadi numerik.

4. Binning:
Tahapan ini merupakan proses transformasi data dengan menggunakan metode binning. Metode ini akan digunakan untuk mengelompokkan data numerik menjadi beberapa bin dengan tujuan memudahkan pemahaman pada persebaran data yang digunakan. 

5. Standardization:
Penerapan standarisasi berfokus pada mengubah data mentah menjadi informasi yang dapat digunakan sebelum dianalisis. Merupakan teknik yang menskalakan data sehingga memiliki mean = 0 dan standar deviasi =1.

Berdasarkan tahapan Data Preparation tersebut, kemudian dilakukan Feature Selection. Pemilihan fitur yang dilakukan berdasarkan kegunaan dan pengaruh fitur terhadap deteksi kecurangan data. Maka fitur yang akan dihapus pada saat pembentukan model adalah. 
1. visit_id
2. dati2
3. procv00_v89
4. dx2_u00_u99
5. dx2_koo_k93

### 4. MODELLING
4 cara pengujian untuk pemilihan model terbaik:
![image](https://user-images.githubusercontent.com/60679635/144964027-df714aca-e62b-40de-9b8c-c418be920efe.png)

Model yang dipilih: Tuning Hyperparameters Dengan kriteria:
- Membagi data latih 70%  dan data uji 30%
- Mendefinisikan 3 informasi utama dalam pembuatan keputusan
a. Parameter random_state=5, n_estimators=20
b. Algoritma Random Forest Classifier (RFC)
c. Hasil penilaian dengan akurasi dari data latih dan data uji

### 5. MODEL EVALUATION
Evaluasi Model dilakukan dengan melihat confusion matrix dan AUC Score. Untuk nilai akurasi pada data testing yang dilakukan adalah sebesar 68% 

![image](https://user-images.githubusercontent.com/60679635/144964233-ab3878e2-325d-4cbc-bac8-16484c6ae84c.png)

Hasil uji sebanyak 30% data uji (60.064 sampel). 
Terdapat sebanyak 49.245 data yang di prediksi akurat. Sedangkan terdapat  9.921 sampel yang tidak valid pada saat dilakukan pengujian. 

![image](https://user-images.githubusercontent.com/60679635/144964276-d5c7f7f9-f072-4283-a5b3-a5f34bd982c5.png)


### DEPLOYMENT
Model yang telah di deploy menggunakan aplikasi Heroku yaitu salah satu tools yang termasuk pada Platform As A Service (PaaS) dapat diakses pada link: https://fraud-detection-rfc-model.herokuapp.com/

Tampilan deployment yang dilakukan adalah sebagai berikut
![image](https://user-images.githubusercontent.com/60679635/144964360-e9afa726-6c06-4111-a712-51d9f62dec08.png)


Untuk informasi lebih lanjut mengenai instalisasi dapat dilihat pada [README.md](Deployment/README.md) di folder Deployment pada repositori ini.

### Team & Anggota
Anggota:
1. 12S18018 - Yohana Polin Simatupang
2. 12S18019 – Maria Puspita Sari Nababan    
3. 12S18064 – Letare Aiglien Saragih
