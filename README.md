# 🧠 Analisis Sentimen Ulasan Aplikasi PINTU CRYPTO Pada Google Play Store Menggunakan Support Vector Machine

Proyek ini bertujuan untuk melakukan **analisis sentimen terhadap ulasan pengguna aplikasi PINTU Crypto** yang diambil dari **Google Play Store**.  
Metode yang digunakan adalah **Support Vector Machine (SVM)** untuk mengklasifikasikan ulasan menjadi **sentimen positif dan negatif** berdasarkan teks ulasan pengguna.

---

## 📂 Dataset

Dataset diperoleh menggunakan **Google-Play-Scraper**, yang digunakan untuk mengekstrak ulasan aplikasi **PINTU Crypto** dari Google Play Store.  
Dataset terdiri dari dua label utama:

- 🟢 **Positif** — ulasan dengan kesan baik terhadap aplikasi  
- 🔴 **Negatif** — ulasan yang berisi keluhan atau ketidakpuasan pengguna  

File tambahan:
- `kamuskatabaku.csv` — digunakan dalam proses **normalisasi kata tidak baku**.

---

## ⚙️ Alur Analisis

1. **Data Cleaning**  
   Menghapus karakter khusus, angka, dan tanda baca yang tidak relevan.  

2. **Case Folding**  
   Mengubah seluruh teks menjadi huruf kecil (lowercase).  

3. **Tokenizing**  
   Memecah kalimat menjadi kata-kata.  

4. **Stopword Removal**  
   Menghapus kata umum yang tidak berpengaruh terhadap makna kalimat (contoh: “yang”, “dan”, “di”).  

5. **Normalisasi**  
   Mengubah kata tidak baku menjadi bentuk baku menggunakan `kamuskatabaku.csv` (contoh: “gk” → “tidak”).  

6. **Stemming**  
   Mengembalikan kata ke bentuk dasarnya menggunakan library **Sastrawi**.  

7. **Ekstraksi Fitur**  
   Menggunakan **TF-IDF Vectorizer** untuk mengubah teks menjadi vektor numerik.  

8. **Klasifikasi Sentimen**  
   Menggunakan **Support Vector Machine (SVM)** untuk membedakan sentimen positif dan negatif.  

9. **Evaluasi Model**  
   Metrik yang digunakan:
   - Akurasi  
   - Presisi  
   - Recall  
   - F1-score  

---

## 🧠 Model yang Digunakan

| Model | Fitur Ekstraksi | Akurasi |
|-------|------------------|----------|
| Skenario 1 | TF-IDF + SVM | **92.20%** |
| Skenario 2 | TF-IDF + SVM | **91.62%** |
| Skenario 3 | TF-IDF + SVM | **91.48%** |

---

## 💻 Cara Menjalankan Program

1. **Clone repositori ini**
   ```bash
   git clone https://github.com/username/analisis-sentimen-pintu-crypto.git
2. **Masuk ke direktori proyek**
   cd analisis-sentimen-pintu-crypto
3. **Instal semua dependensi yang diperlukan**
   pip install -r requirements.txt
4. **Jalankan program utama**
   python Analisis_Sentimen_Pintu_Crypto.py

---

## 🧩 Library yang Digunakan

- pandas

- numpy

- scikit-learn

- Sastrawi

- deep_translator

- TextBlob

- matplotlib

- seaborn

---

## Penulis

Nama: Muhamad Sebastian Nugraha
Judul: Analisis Sentimen Ulasan Aplikasi PINTU CRYPTO Pada Google Play Store Menggunakan Support Vector Machine
Bahasa Pemrograman: Python
File Utama: Analisis_Sentimen_Pintu_Crypto.py
File Pendukung: kamuskatabaku.csv

---

## Lisensi

Proyek ini dibuat untuk tujuan pembelajaran dan penelitian.
Silakan gunakan atau modifikasi dengan tetap mencantumkan sumber.