# UAS_AI

# NAMA : KEVIN GLENANDA ADITIYA

# NIM : 171011401384


Memprediksi jenis kelamin dari nama bahasa Indonesia menggunakan Metode Random Forest Classifier dan Machine Learning.

Data set yang digunakan berasal dari data pemilih tetap Komisi Pemilihan Umum (KPU) yang bisa didapat [disini](https://pilkada2017.kpu.go.id/pemilih/dps/DKI%20JAKARTA). Saya telah menyiapkan data set yang telah di scrape dalam bentuk csv, terdiri dari 2 kolom, nama dan jenis kelamin [disini](./data/data-pemilih-kpu.csv).

Tampilan dataset, teridiri dari 13.137 nama

| Nama | Jenis Kelamin |
|------|---------------|
|ERWIN TJAHJONO|Laki-Laki|
|DAVIANDRIE ANDIKA BAHROENY|Laki-Laki|
|ELAN KURNIAWAN|Laki-Laki|
|AYU DWI CAHYANING MUKTI|Perempuan|
|SITA.HJ|Perempuan|


Metode klasifikasi yang digunakan adalah Logistic Regression, Naive Bayes dan Random Forest Tree dengan bantuan library Python [Scikit Learn](http://scikit-learn.org).  

### Setup program
1. Clone repository ini https://github.com/kevachiko23/UAS-AI.git`
2. Masuk ke direktori project `cd Jenis-Kelamin`
3. Buat Python virtual environment `python3 -m venv venv`
4. Aktifkan virtual environment `source venv/bin/activate`
5. Install dependency `pip3 install -r requirements.txt`

### Menjalankan program

```bash
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
```

Tebak jenis kelamin kevin ? 
```bash
python jenis-kelamin.py kevin
Prediksi jenis kelamin dengan Naive Bayes :
kevin  :  Pria
```

Menjalankan program dengan metode Logistic Regression dan dataset yg ditentukan ulang
```bash
python jenis-kelamin.py -t "./data/data-pemilih-kpu.csv" -ml LG "mawar melati"
Akurasi : 93.5135135135 %
Prediksi jenis kelamin dengan Logistic Regression :
mawar melati  :  Wanita
```

Untuk mengubah prediksi nama dari nama bahasa negara lain atau bahasa daerah tertentu, dataset nya silahkan diganti sesuai kebutuhan



