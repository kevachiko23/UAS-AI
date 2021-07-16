UAS AI

NAMA  : KEVIN GLENANDA ADITIYA
NIM   : 171011401384

Memprediksi jenis kelamin dari nama bahasa Indonesia menggunakan Machine Learning.

Data set yang digunakan berasal dari data pemilih tetap Komisi Pemilihan Umum (KPU) yang bisa didapat disini. Saya telah menyiapkan data set yang telah di scrape dalam bentuk csv, terdiri dari 2 kolom, nama dan jenis kelamin disini.

Tampilan dataset, teridiri dari 13.137 nama

Nama	Jenis Kelamin
ERWIN TJAHJONO	Laki-Laki
DAVIANDRIE ANDIKA BAHROENY	Laki-Laki
ELAN KURNIAWAN	Laki-Laki
AYU DWI CAHYANING MUKTI	Perempuan
SITA.HJ	Perempuan
Metode klasifikasi yang digunakan adalah Logistic Regression, Naive Bayes dan Random Forest Tree dengan bantuan library Python Scikit Learn.

Setup program
Clone repository ini git clone git@github.com:irfani/Jenis-Kelamin.git
Masuk ke direktori project cd Jenis-Kelamin
Buat Python virtual environment python3 -m venv venv
Aktifkan virtual environment source venv/bin/activate
Install dependency pip3 install -r requirements.txt
Menjalankan program
python jenis-kelamin.py -h
usage: jenis-kelamin.py [-h] [-ml {NB,LG,RF}] [-t TRAIN] nama

Menentukan jenis kelamin berdasarkan nama Bahasa Indoensia

positional arguments:
  nama                  Nama

optional arguments:
  -h, --help            show this help message and exit
  -ml {NB,LG,RF}        NB=Naive Bayes(default); LG=Logistic Regression;
                        RF=Random Forest
  -t TRAIN, --train TRAIN
                        Training ulang dengan dataset yang ditentukan
Tebak jenis kelamin irfani ?

python jenis-kelamin.py irfani
Prediksi jenis kelamin dengan Naive Bayes :
irfani  :  Pria
Menjalankan program dengan metode Logistic Regression dan dataset yg ditentukan ulang

python jenis-kelamin.py -t "./data/data-pemilih-kpu.csv" -ml LG "niky felina"
Akurasi : 93.5135135135 %
Prediksi jenis kelamin dengan Logistic Regression :
niky felina  :  Wanita
Untuk mengubah prediksi nama dari nama bahasa negara lain atau bahasa daerah tertentu, dataset nya silahkan diganti sesuai kebutuhan
