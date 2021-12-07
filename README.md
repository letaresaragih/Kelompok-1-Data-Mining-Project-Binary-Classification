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

![histogram](https://user-images.githubusercontent.com/60679684/144963055-fada5440-0c73-41e2-9d64-d795883b6b73.jpeg)

Visualisasi heatmap untuk melihat korelasi setiap fitur:

![heatmap](https://user-images.githubusercontent.com/60679684/144963116-7a92732c-b277-4225-9c44-0172eacc06d2.jpeg)

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
