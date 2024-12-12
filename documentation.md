# 📘 Dokumentasi Proyek HR Analysis

## **1. Deskripsi Proyek**

Proyek ini bertujuan untuk menganalisis tingkat *attrition* (keluar masuk karyawan) di perusahaan menggunakan **Metabase** sebagai alat visualisasi. Data karyawan disimpan dalam database **Supabase**, yang memberikan fleksibilitas dalam pengelolaan data berbasis cloud.

Visualisasi data meliputi analisis tingkat keluar karyawan berdasarkan:

- **Gender (Jenis Kelamin)**
- **Marital Status (Status Pernikahan)**
- **Job Role (Posisi Pekerjaan)**
- **Department (Departemen)**
- **Overtime (Lembur)**
- **Job Satisfaction (Kepuasan Kerja)**
- **Age (Usia)**

---

## **2. Permasalahan Bisnis**

Jaya Jaya Maju merupakan perusahaan multinasional dengan lebih dari 1000 karyawan. Meskipun perusahaan berkembang pesat, mereka menghadapi tantangan dalam mempertahankan karyawan akibat tingginya *attrition rate* yang mencapai lebih dari 10%. Ini menyebabkan beberapa dampak negatif seperti:

- **Peningkatan Biaya Rekrutmen:** Biaya tambahan untuk merekrut, melatih, dan mengintegrasikan karyawan baru.
- **Penurunan Produktivitas:** Beban kerja meningkat bagi karyawan yang tersisa, mengurangi produktivitas.
- **Ketidakstabilan Operasional:** Pergantian karyawan yang tinggi dapat mengganggu kelancaran operasi bisnis.

**Urgensi & Risiko:** Jika masalah ini tidak diatasi, perusahaan berisiko kehilangan talenta terbaik, merusak citra perusahaan, dan menghadapi penurunan daya saing di pasar global.

**Pertanyaan Bisnis:**

1. Seberapa tinggi tingkat *attrition* di perusahaan ini?
2. Faktor-faktor apa saja yang memengaruhi keputusan karyawan untuk meninggalkan perusahaan?
3. Apakah ada perbedaan tingkat *attrition* berdasarkan role atau departemen tertentu di perusahaan?
4. Bagaimana pengaruh lembur (*overtime*) terhadap keputusan karyawan untuk keluar dari perusahaan?
5. Bagaimana memprediksi tingkat attrition di masa depan?

---

## **3. Tahapan Persiapan**

### **Sumber Data**

- File CSV berisi data karyawan seperti usia, gender, status pernikahan, status pekerjaan, dan tingkat kepuasan kerja yang diunggah ke Supabase.

### **Setup Environment**

- **Library Python:**
  - `pandas` untuk pengolahan data.
  - `matplotlib` dan `seaborn` untuk visualisasi.
  - `scikit-learn` untuk pelatihan model prediksi.
  - `joblib` untuk menyimpan dan memuat model.

- **Konfigurasi Supabase:**
  - Hubungkan Metabase dengan Supabase melalui konfigurasi koneksi database.
  - Impor file CSV ke Supabase dan pastikan data telah berhasil dimuat ke dalam database.

- **Akses Metabase:**
  1. Buka **[https://metabase.yourdomain.com](https://metabase.yourdomain.com)**.
  2. Buat akun admin dan tambahkan koneksi database Supabase.
  3. Impor file CSV ke Supabase dan integrasikan dengan Metabase.

---

## **4. Rekomendasi Action Items**

1. **Mengelola dan Mengurangi Lembur:**
   - **Evaluasi Beban Kerja:** Sesuaikan beban kerja agar karyawan tidak perlu sering lembur.
   - **Insentif Kinerja:** Berikan insentif berdasarkan kinerja, bukan waktu kerja.
   - **Batas Jam Lembur:** Tetapkan batas maksimal lembur per minggu (misal, 10 jam/minggu) untuk meningkatkan keseimbangan kerja dan kehidupan pribadi.

2. **Meningkatkan Kepuasan Kerja:**
   - **Program Peningkatan Kepuasan:** Adakan survei bulanan dan sesi *one-on-one* untuk mendengar masukan karyawan.
   - **Pengembangan Karir:** Sediakan pelatihan pengembangan keterampilan untuk meningkatkan motivasi.
   - **Peningkatan Lingkungan Kerja:** Sediakan fasilitas tambahan yang mendukung kenyamanan karyawan (misal, ruang relaksasi atau area rekreasi).

3. **Strategi Retensi di Departemen Kritis:**
   - **Fokus pada Departemen Bermasalah:** Buat program retensi yang mencakup insentif, pengakuan, dan jalur karir yang jelas untuk departemen dengan tingkat *attrition* tinggi.

4. **Penilaian Berkelanjutan:**
   - **Pemantauan Berkelanjutan:** Pantau metrik penting seperti lembur dan tingkat kepuasan melalui dashboard dan lakukan intervensi segera.
   
---

## **5. Cara Menjalankan Proyek**

### **1️⃣ Hubungkan Metabase dengan Supabase**

Konfigurasikan koneksi database di Metabase menggunakan detail dari Supabase.

### **2️⃣ Akses Metabase**

1. Buka browser dan kunjungi **[https://metabase.yourdomain.com](https://metabase.yourdomain.com)**.
2. Lakukan konfigurasi awal:
   - Buat akun admin.
   - Tambahkan koneksi database Supabase.

### **3️⃣ Impor Dataset**

1. Impor file CSV ke Supabase.
2. Buat **Dashboard** dengan visualisasi berikut:
   - Total Employee & Attrition Rate
   - Impact of Overtime on Attrition
   - Attrition Rate by Gender
   - Attrition by Marital Status
   - Attrition by Job Role
   - Attrition by Department
   - Attrition by Age Group
   - Job Satisfaction vs Attrition

---
## **6. Business Dashboard**

Dashboard ini dirancang untuk memberikan wawasan komprehensif kepada tim HR mengenai faktor-faktor yang berkontribusi terhadap keputusan karyawan untuk meninggalkan perusahaan. Dengan dashboard ini, tim HR dapat:

- Mengidentifikasi area atau departemen yang memiliki tingkat attrition tinggi.
- Menganalisis faktor-faktor seperti lembur, kepuasan kerja, dan kelompok demografis yang mungkin mempengaruhi attrition.
- Mengambil tindakan proaktif untuk meningkatkan retensi karyawan dan mengurangi biaya terkait dengan pergantian karyawan.

![Yulia Pratiwi - Dashboard](https://github.com/user-attachments/assets/9100312b-cb53-4c19-8052-061ca4d50812)

## Conclusion

1. Seberapa tinggi tingkat attrition di perusahaan ini?
    * Jawaban: Tingkat attrition di perusahaan ini adalah sekitar 17%. Ini berarti bahwa satu dari enam karyawan meninggalkan perusahaan dalam jangka waktu tertentu, menunjukkan bahwa tingkat keluar karyawan cukup signifikan.

2. Faktor-faktor apa saja yang mempengaruhi keputusan karyawan untuk meninggalkan perusahaan?
    * Jawaban: Beberapa faktor utama yang mempengaruhi keputusan karyawan untuk meninggalkan perusahaan meliputi:
        * Lembur (Overtime): Karyawan yang sering bekerja lembur cenderung memiliki kemungkinan lebih tinggi untuk keluar dari perusahaan.
        * Status Perkawinan: Karyawan yang belum menikah (single) menunjukkan tingkat attrition yang lebih tinggi, yang mungkin mencerminkan mobilitas yang lebih besar dan keinginan untuk mencari peluang baru.

3. Apakah ada perbedaan tingkat attrition berdasarkan role atau departemen tertentu di perusahaan?
    * Jawaban: Ya, terdapat perbedaan tingkat attrition berdasarkan role dan departemen. Misalnya, role seperti Sales Representative dan departemen seperti Sales menunjukkan tingkat attrition yang lebih tinggi dibandingkan role atau departemen lain. Hal ini menunjukkan bahwa beban kerja, tekanan, dan mungkin juga struktur kompensasi di departemen-departemen ini dapat berkontribusi pada keputusan karyawan untuk meninggalkan perusahaan.

4. Bagaimana pengaruh lembur (overtime) terhadap keputusan karyawan untuk keluar dari perusahaan?
    * Jawaban: Lembur memiliki pengaruh signifikan terhadap keputusan karyawan untuk meninggalkan perusahaan. Data menunjukkan bahwa karyawan yang sering bekerja lembur (overtime) memiliki tingkat attrition yang lebih tinggi. Ini mungkin terkait dengan tingkat stres yang lebih tinggi dan ketidakseimbangan antara kehidupan kerja dan pribadi.

### Rekomendasi Action Items

Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.

1. Mengelola dan Mengurangi Lembur:
    * Evaluasi dan sesuaikan beban kerja untuk mengurangi lembur berlebih yang dapat mempengaruhi keseimbangan kehidupan kerja dan meningkatkan tingkat attrition.
2. Meningkatkan Kepuasan Kerja dan Lingkungan Kerja:
    * Implementasikan program peningkatan kepuasan kerja dan ciptakan lingkungan kerja yang lebih mendukung untuk menjaga keterlibatan dan retensi karyawan.
3. Strategi Retensi di Departemen Kritis:
    * Fokuskan upaya retensi pada departemen dan role yang menunjukkan tingkat attrition tinggi, seperti `Sales`. Program retensi yang ditargetkan dapat mencakup insentif, pengakuan, dan jalur karir yang jelas.
4. Penilaian dan Tindakan Berkelanjutan:
    * Pantau terus faktor-faktor yang mempengaruhi attrition melalui dashboard dan lakukan tindakan cepat saat masalah mulai muncul.

Dengan mengikuti rekomendasi ini, perusahaan diharapkan dapat menurunkan tingkat attrition, meningkatkan retensi karyawan, dan memperkuat stabilitas serta efisiensi operasional secara keseluruhan.


Username: yuliapratiwi169@gmail.com

Password: Skylight169
