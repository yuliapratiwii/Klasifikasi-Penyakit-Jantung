# Implementasi Chatbot Mahasiswa Baru UNIB

Proyek ini bertujuan untuk membangun chatbot berbasis deep learning untuk membantu mahasiswa baru Universitas Bengkulu (UNIB) mendapatkan informasi terkait registrasi mahasiswa baru dan juga informasi seputar unib.

### 1. **Business Understanding**
- **Tujuan:**
  - Membuat chatbot yang dapat menjawab berbagai pertanyaan mahasiswa baru terkait kampus, seperti jadwal, lokasi gedung, prosedur administrasi, dan lain-lain.
- **Manfaat:**
  - Mengurangi beban layanan informasi manual.
  - Menyediakan akses informasi 24/7 untuk mahasiswa baru.

---

### 2. **Data Understanding**
- **Dataset:**
  - Dataset berbentuk JSON yang dikumpulkan melalui informasi pada laman unib.ac.id
- **Fitur Utama Dataset:**
  - **Patterns:** Kalimat input dari pengguna.
  - **Tags:** Label kategori intent.
  - **Responses:** Jawaban chatbot untuk setiap intent.

---

### 3. **Data Preparation**

#### **Teknik Pemrosesan Data:**
1. **Pembersihan Data:** Menghapus tanda baca dan karakter khusus dari teks.
2. **Lematisasi:** Mengubah kata menjadi bentuk dasar untuk konsistensi.
3. **Tokenisasi & Padding:**
   - Memecah kalimat menjadi token.
   - Menggunakan padding agar setiap input memiliki panjang yang sama.
4. **Encoding:**
   - Mengonversi label teks menjadi format numerik untuk diproses oleh model deep learning.

---

### 4. **Modeling**

#### **Arsitektur Model:**
- **Embedding Layer:** Untuk merepresentasikan kata sebagai vektor numerik.
- **Bidirectional LSTM & GRU:**
  - Digunakan untuk menangkap konteks sekuensial dari teks input.
- **Dense Layer:**
  - Mengklasifikasikan intent ke dalam kategori output.

#### **Parameter Model:**
- Optimizer: Adam.
- Loss Function: Sparse Categorical Crossentropy.
- Dropout: 0.5 (untuk mencegah overfitting).

#### **Hasil Model:**
- **Akurasi Pelatihan:** 97.3% setelah 200 epoch.
- **Grafik Pelatihan:**
  - **Loss:** Menurun konsisten selama pelatihan.
  - **Akurasi:** Meningkat stabil hingga mendekati 1.

---

### 5. **Evaluation**


#### **Kelebihan Model:**
- Mampu mengklasifikasikan intent pengguna dengan akurasi tinggi.
- Menangkap konteks teks input dengan baik menggunakan LSTM dan GRU.

#### **Kekurangan Model:**
- Masih membutuhkan pengujian pada data real-world untuk memastikan kemampuan generalisasi.
- Belum dilakukan evaluasi mendalam menggunakan metrik seperti precision, recall, dan F1-score.

#### **Saran Evaluasi Lanjutan:**
- Uji model dengan pertanyaan dari mahasiswa baru secara langsung.
- Lakukan analisis tambahan dengan metrik evaluasi yang lebih detail.

---


## Kesimpulan
Proyek chatbot ini telah dirancang dan dikembangkan dengan mengikuti metodologi CRISP-DM, memastikan setiap tahapannya dilakukan secara sistematis. Model deep learning yang dibangun menunjukkan hasil akurasi tinggi dan memiliki potensi besar untuk diimplementasikan langsung di UNIB.

Jika ada masukan atau saran tambahan, silakan diskusikan! 😊
