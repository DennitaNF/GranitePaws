# Capstone Project: Analisis Komentar YouTube tentang Streetfeeding dengan Bantuan AI

## 📌 Project Overview
Streetfeeding adalah isu sosial yang sering menimbulkan pro-kontra di masyarakat. Melalui proyek ini, dilakukan analisis komentar YouTube terkait streetfeeding untuk memahami persepsi publik. Dengan bantuan AI (IBM Granite Models via Replicate API), komentar diklasifikasikan ke dalam beberapa kategori, lalu dirangkum untuk menemukan insight yang bermakna.

**Tujuan:**
- Mengklasifikasikan komentar ke dalam kategori: Pro-Streetfeeding, Kontra-Streetfeeding, Edukasi, Pertanyaan, atau Lainnya.
- Merangkum argumen utama tiap kategori.
- Memberikan rekomendasi berdasarkan insight hasil analisis.

## 📂 Dataset
- **Sumber:** Komentar YouTube yang diunduh (format CSV).
- **Jumlah data:** ±9.000 komentar.
- **Contoh kolom:** `video_id`, `authorDisplayName`, `textDisplay`.

[🔗 Link Dataset](https://github.com/DennitaNF/GranitePaws/blob/main/youtube_comments_simple.csv)  <!-- ganti sesuai lokasi repo kamu -->

## ⚙️ Analysis Process
1. **Preprocessing**
   - Membersihkan komentar (hapus HTML tag, mention, URL, karakter non-alfanumerik).
   - Menggunakan 10 komentar sampel (dapat diperluas ke seluruh dataset).
2. **Klasifikasi dengan AI (IBM Granite)**
   - Prompt diarahkan agar model hanya memilih kategori tertentu.
   - Hasil dikembalikan ke dataframe.
3. **Rangkuman**
   - Komentar dalam tiap kategori digabung.
   - AI merangkum poin/argumen utama tiap kategori.
4. **Output**
   - CSV hasil klasifikasi.
   - Ringkasan insight per kategori.

## 📊 Insight & Findings
- **Pro-Streetfeeding:** Komentar banyak menekankan kepedulian dan empati terhadap hewan jalanan.
- **Kontra-Streetfeeding:** Beberapa menyoroti dampak negatif (kotor, mengundang penyakit, ketergantungan hewan).
- **Edukasi:** Ada komentar yang menginformasikan solusi alternatif seperti adopsi, steril gratis, atau shelter.
- **Pertanyaan:** Publik menunjukkan ketertarikan dengan bertanya cara terlibat atau solusi praktis.

## ✅ Recommendations
- **Kampanye edukasi:** Tekankan solusi jangka panjang seperti adopsi & steril.
- **Kolaborasi komunitas:** Ajak organisasi pecinta hewan untuk fasilitasi streetfeeding lebih terstruktur.
- **Kebijakan lokal:** Mendorong pemerintah daerah mendukung shelter/klinik hewan gratis.

## 🤖 AI Support Explanation
- **Model:** IBM Granite 3.3 8B Instruct (via Replicate API).
- **Peran AI:**
  - *Klasifikasi* komentar ke kategori spesifik.
  - *Summarization* untuk merangkum argumen utama per kategori.
- **Platform:** Google Colab dengan Python (pandas + replicate API).
- AI mempercepat proses analisis teks ribuan komentar yang sulit dilakukan manual.

---
