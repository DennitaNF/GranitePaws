# Project-MeowInsight: Analisis Sentimen dan Klasifikasi Opini Terhadap Street Feeding Kucing Liar Menggunakan IBM Granite

**Capstone Project - Student Development Initiative** **Oleh: [NAMA LENGKAP ANDA]**

---

## 1. Project Overview

### Latar Belakang
*Street feeding* atau memberi makan hewan liar, khususnya kucing, telah menjadi fenomena sosial yang marak didiskusikan di platform digital seperti YouTube. Di satu sisi, tindakan ini didasari oleh rasa kasih sayang dan kepedulian terhadap hewan. Di sisi lain, muncul kekhawatiran terkait dampak negatif seperti overpopulasi, potensi penyebaran penyakit, dan masalah kebersihan lingkungan. Diskursus yang masif dan tidak terstruktur ini menciptakan lanskap opini yang kompleks.

### Permasalahan
Memahami sentimen dan argumen utama dari ribuan komentar di YouTube secara manual adalah pekerjaan yang tidak efisien dan rentan terhadap bias. Sulit untuk mengukur secara objektif bagaimana opini publik terdistribusi dan apa saja poin-poin krusial yang menjadi perhatian utama masyarakat.

### Tujuan Proyek
Proyek ini bertujuan untuk mengatasi masalah tersebut dengan:
1.  **Mengklasifikasikan** ribuan komentar YouTube secara otomatis ke dalam kategori sentimen (Positif, Negatif, Netral) dan topik spesifik (Contoh: Pro, Kontra, Edukasi, Pertanyaan).
2.  **Merangkum** argumen-argumen utama dari setiap kategori untuk memahami inti dari setiap sudut pandang.
3.  **Menghasilkan wawasan (insight)** yang bernilai dan rekomendasi yang dapat ditindaklanjuti bagi para pembuat konten, komunitas pecinta hewan, dan masyarakat umum.

### Pendekatan
Proyek ini menggunakan pendekatan analisis data kuantitatif dan kualitatif dengan dukungan *Natural Language Processing* (NLP). Alur kerja utama meliputi: pengumpulan data komentar, pembersihan teks, analisis menggunakan model AI *Large Language Model* (LLM) IBM Granite untuk klasifikasi dan peringkasan, visualisasi data, dan penarikan kesimpulan.

---

## 2. Link Raw Dataset

Dataset yang digunakan dalam analisis ini adalah kumpulan komentar publik yang diambil dari beberapa video YouTube populer bertema *street feeding* kucing liar.

* **[Link Menuju Dataset]([URL_RAW_DATASET_ANDA_DI_GITHUB_SINI])**
* **Sumber:** YouTube (Scraping)
* **Format:** CSV
* **Jumlah Data:** [CONTOH: 5,420 Komentar]

---

## 3. AI Support Explanation

Proyek ini memanfaatkan kecanggihan **IBM Granite**, sebuah *Large Language Model* (LLM) dari IBM, untuk melakukan tugas-tugas inti analisis teks. Model spesifik yang digunakan adalah `ibm/granite-13b-instruct-v2` yang diakses melalui API IBM Cloud dalam lingkungan Google Colab.

Penggunaan AI difokuskan pada dua fungsi utama:

1.  **Klasifikasi Teks (Zero-Shot Text Classification):**
    * Model AI diberikan *prompt* yang dirancang khusus untuk menginstruksikan agar mengklasifikasikan setiap komentar ke dalam kategori yang telah ditentukan tanpa perlu *fine-tuning* (latihan ulang).
    * **Kategori Sentimen:** `Positif`, `Negatif`, `Netral`.
    * **Kategori Topik:** `Pro-Streetfeeding`, `Kontra-Streetfeeding`, `Edukasi & Saran`, `Pertanyaan`, dan `Lainnya`.
    * Pendekatan ini memungkinkan analisis yang cepat dan scalabel terhadap data teks yang besar.

2.  **Peringkasan Generatif (Generative Summarization):**
    * Setelah komentar dikelompokkan berdasarkan kategorinya, AI digunakan untuk membaca semua komentar dalam satu kelompok (misalnya, semua komentar 'Kontra-Streetfeeding').
    * Selanjutnya, model diminta untuk membuat sebuah rangkuman yang koheren, mengidentifikasi dan menyajikan argumen-argumen utama, kekhawatiran, atau poin-poin yang paling sering muncul dari kelompok tersebut.

---

## 4. Insight & Findings

Analisis data menghasilkan beberapa temuan kunci yang memberikan gambaran mendalam tentang opini publik.

### Visualisasi Data

**Distribusi Sentimen Publik**
[MASUKKAN GAMBAR GRAFIK PIE CHART SENTIMEN DI SINI]
*Gambar 1: Persentase komentar berdasarkan sentimen Positif, Negatif, dan Netral.*

**Distribusi Topik Diskusi**
[MASUKKAN GAMBAR GRAFIK BAR CHART TOPIK DI SINI]
*Gambar 2: Jumlah komentar untuk setiap topik yang didiskusikan.*

### Temuan Utama

* **Insight 1: Dominasi Dukungan Emosional, Namun Kritik Bersifat Spesifik.**
    * **Temuan:** Sekitar **[Contoh: 65%]** komentar menunjukkan sentimen positif dan masuk kategori 'Pro-Streetfeeding'. Argumen yang paling umum bersifat emosional seperti "kasihan", "kucing juga makhluk Tuhan", dan "terima kasih orang baik".
    * **Wawasan:** Meskipun kalah jumlah, komentar 'Kontra-Streetfeeding' **[Contoh: 20%]** menyajikan argumen yang jauh lebih spesifik dan berbasis kekhawatiran nyata, seperti risiko penyebaran virus *panleukopenia*, masalah cacingan pada anak-anak, dan kebersihan lingkungan akibat sisa makanan. Ini menunjukkan adanya *gap* antara niat baik dan pemahaman risiko.

* **Insight 2: Peran Vital Audiens sebagai Agen Edukasi.**
    * **Temuan:** Kategori 'Edukasi & Saran' memiliki porsi yang signifikan **[Contoh: 15%]**. Komentar dalam kategori ini tidak hanya mendukung, tetapi juga memberikan saran praktis seperti "jangan kasih makanan sisa", "taruh air minum juga", atau "yang terpenting adalah steril (TNVR)".
    * **Wawasan:** Terdapat kesadaran kolektif di antara sebagian audiens bahwa *street feeding* harus dilakukan dengan cara yang benar. Komunitas secara organik saling mengedukasi, menunjukkan adanya peluang untuk menyebarkan praktik terbaik secara lebih luas.

* **Insight 3: [TULIS INSIGHT UNIK KETIGA DARI HASIL ANALISIS ANDA]**
    * **Temuan:** [Jelaskan data atau fakta yang kamu temukan dari hasil klasifikasi].
    * **Wawasan:** [Jelaskan makna di balik data tersebut. Apa artinya? Kenapa ini penting?].

---

## 5. Conclusion & Recommendations

### Kesimpulan
Analisis komentar YouTube menggunakan IBM Granite berhasil memetakan lanskap opini publik mengenai *street feeding* kucing liar. Ditemukan bahwa meskipun dukungan moral sangat tinggi, terdapat kekhawatiran yang valid dan kurang teratasi terkait dampak kesehatan dan lingkungan. Selain itu, ada potensi besar dalam komunitas itu sendiri untuk menyebarkan praktik *street feeding* yang bertanggung jawab.

### Rekomendasi
Berdasarkan temuan di atas, berikut adalah beberapa rekomendasi yang dapat ditindaklanjuti:

1.  **Untuk Pembuat Konten Edukasi Hewan:**
    * Membuat konten video yang secara spesifik membahas dan memberikan solusi atas kekhawatiran yang muncul di komentar 'Kontra' (misalnya, "Cara Street Feeding Higienis" atau "Pentingnya Sterilisasi untuk Kesejahteraan Kucing Liar").

2.  **Untuk Komunitas dan Organisasi Animal Welfare:**
    * Memanfaatkan argumen dari kategori 'Edukasi & Saran' sebagai bahan untuk kampanye di media sosial. Buat infografis atau video pendek dari saran-saran terbaik yang diberikan oleh audiens.

3.  **Untuk Masyarakat Umum:**
    * Sebelum melakukan *street feeding*, cari informasi mengenai praktik yang bertanggung jawab untuk memastikan niat baik tidak menimbulkan masalah baru bagi lingkungan maupun hewan itu sendiri.

---

## Cara Menjalankan Proyek Ini

1.  **Clone repository ini:**
    ```bash
    git clone [https://github.com/username/Project-MeowInsight.git](https://github.com/username/Project-MeowInsight.git)
    ```
2.  **Install dependensi yang dibutuhkan:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Buka file notebook `[NAMA_FILE_NOTEBOOK_ANDA].ipynb` di Google Colab atau Jupyter.**
4.  **Masukkan kredensial Anda:** Ganti placeholder `YOUR_IBM_CLOUD_API_KEY` dan `YOUR_WATSONX_PROJECT_ID` dengan kredensial Anda sendiri.
5.  **Jalankan semua sel secara berurutan.**
