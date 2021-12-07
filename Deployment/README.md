# RE-DEPLOYMENT MODEL. 

## Model dapat di unduh pada link berikut :
1. simpan model di folder deployment. 
https://drive.google.com/file/d/1CBVHEZijJT4iqz2CV-Do-rKIet079M6K/view?usp=sharing. 
2. Kemudian simpan kedalam folder deployment. 

## Testing Aplikasi di Lokal komputer anda. 
1. Pastikan Anda sudah menginstall Anaconda
2. Buka terminal/command prompt/power shell
3. Buat virtual environment dengan 
    conda create -n <nama-environment> python=3.9
4. Aktifkan virtual environment dengan 
    conda activate <nama-environment>
5. Install semua dependency/package Python dengan
    pip install -r requirements.txt
6. Jalankan API menggunakan perintah
    python app.py
7. Akses web di localhost:5000/
  
Buka URL dengan browser, coba masukkan data yang ingin di prediksi
Anda akan diberikan estimasi biaya asuransi pada sisi kanan halaman website. 
 
**## Deployment menggunakan heroku:**
1. Bukalah aplikasi heroku.com 
2. Kemudian buatlah app pada halaman dashboard. 
3. Setelah itu, login dengan heroku cli. 
    heroku login
4. Kemudian ikuti perintah dibawah ini 
    heroku git:clone -a <App name>
    git add .
    git commit -am "make it better"
    git push heroku master
    
