# Analisis Sentimen Ulasan Aplikasi Shopee

Sebuah proyek untuk menganalisis sentimen dari ulasan pengguna aplikasi Shopee di Google Play Store menggunakan  *machine learning* . Proyek ini bertujuan untuk memahami opini dan perasaan pengguna (apakah positif, negatif, atau netral) terhadap aplikasi Shopee berdasarkan teks ulasan yang mereka berikan.

Masalah utama yang ingin diselesaikan adalah mengolah data ulasan yang tidak terstruktur menjadi sebuah kesimpulan sentimen yang terukur. Hasil analisis ini bisa sangat bermanfaat bagi tim produk,  *marketing* , atau siapa saja yang ingin memahami kelebihan dan kekurangan aplikasi dari sudut pandang pengguna.

## A. Fitur Utama

Proyek ini mencakup beberapa tahapan penting dalam analisis sentimen, antara lain:

* **Data Scraping** : Mengambil 5.000 ulasan terbaru dari aplikasi Shopee di Google Play Store secara otomatis.
* **Data Preprocessing** : Membersihkan dan mempersiapkan data teks ulasan melalui serangkaian proses:
* *Cleaning* : Menghapus URL, HTML, emoji, dan karakter yang tidak relevan.
* *Case Folding* : Menyeragamkan semua teks menjadi huruf kecil.
* *Word Normalization* : Mengubah kata-kata tidak baku (alay/slang) menjadi kata baku menggunakan kamus.
* *Stopword Removal* : Menghapus kata-kata umum yang tidak memiliki makna sentimen (seperti "yang", "di", "dan").
* *Stemming* : Mengubah kata-kata ke bentuk dasarnya (misalnya, "pelayanannya" menjadi "layan").
* **Ekstraksi Fitur** : Menggunakan metode **TF-IDF** ( *Term Frequency-Inverse Document Frequency* ) untuk mengubah data teks menjadi data numerik yang bisa diolah oleh model  *machine learning* .
* **Pemodelan Machine Learning** : Membangun model klasifikasi sentimen menggunakan algoritma  **Naive Bayes** .
* **Evaluasi Model** : Mengukur performa model dengan metrik akurasi dan menampilkannya dalam bentuk  *confusion matrix* .
* **Visualisasi Data** : Menampilkan data dalam bentuk visual yang mudah dipahami, seperti:
* *Word Cloud* untuk kata-kata yang paling sering muncul.
* Diagram batang untuk frekuensi kata.
* Diagram lingkaran untuk distribusi sentimen.

## B. Teknologi yang Digunakan

* **Bahasa** : Python
* **Library Utama** :
* `google_play_scraper`: Untuk proses *scraping* data ulasan.
* `pandas`: Untuk manipulasi dan analisis data.
* `scikit-learn`: Untuk implementasi TF-IDF dan model Naive Bayes.
* `nltk` & `Sastrawi`: Untuk *Natural Language Processing* (NLP) seperti *stopword removal* dan  *stemming* .
* `wordcloud` & `matplotlib`: Untuk visualisasi data.

## C. Instalasi dan Cara Menjalankan

Untuk menjalankan proyek ini di komputermu, ikuti langkah-langkah berikut:

1. Clone Repositori
   Buka terminal atau Git Bash, lalu jalankan perintah:
   **Bash**

   ```
   git clone [URL_REPOSITORI_ANDA]
   cd [NAMA_FOLDER_REPOSITORI]
   ```
2. Buat Virtual Environment (Sangat Direkomendasikan)
   Untuk menjaga dependensi proyek tetap terisolasi, buat sebuah virtual environment.
   **Bash**

   ```
   python -m venv venv
   ```

   Aktifkan:

   * Windows: `venv\Scripts\activate`
   * macOS/Linux: `source venv/bin/activate`
3. Instal Dependensi
   Semua library yang dibutuhkan sudah tercatat dalam file requirements.txt. Instal dengan perintah:

   > **Catatan** : Jika belum ada file `requirements.txt`, kamu bisa membuatnya dengan `pip freeze > requirements.txt` setelah menginstal semua *library* di bawah ini secara manual.
   >

   **Bash**

   ```
   pip install -r requirements.txt
   ```

   Atau, instal satu per satu:

   **Bash**

   ```
   pip install pandas google-play-scraper nltk sastrawi scikit-learn wordcloud matplotlib
   ```
4. Jalankan Jupyter Notebook
   Setelah semua dependensi terinstal, jalankan Jupyter Notebook:
   **Bash**

   ```
   jupyter notebook AnalisisSentimenAplikasiShopee.ipynb
   ```

   *Notebook* akan terbuka di  *browser* -mu, dan kamu bisa menjalankan setiap sel kode untuk melihat prosesnya.

## D. Struktur Folder

Proyek ini disusun dengan struktur berikut untuk memudahkan navigasi:

```
├── AnalisisSentimenAplikasiShopee.ipynb  # Notebook utama berisi semua proses
├── kamuskatabaku.xlsx                    # Kamus kata baku untuk normalisasi
├── hasil_scraping_aplikasi_Shopee.csv    # Data mentah hasil scraping
├── hasil_preprocessing_data_ulasan_aplikasi_Shopee.csv # Data setelah preprocessing
└── hasil_labelling_data_ulasan_aplikasi_Shopee.csv   # Data yang sudah diberi label
```
