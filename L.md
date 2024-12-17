# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding
Jaya Jaya Institut adalah institusi pendidikan tinggi yang telah berdiri sejak tahun 2000 dan berhasil mencetak lulusan dengan reputasi baik di berbagai bidang. Namun, salah satu tantangan utama yang dihadapi oleh Jaya Jaya Institut adalah tingginya tingkat siswa yang tidak menyelesaikan pendidikannya alias dropout.

Masalah ini menjadi serius karena:
1. Tingkat dropout yang tinggi memengaruhi citra institusi dan daya tarik calon siswa.
2. Dropout dapat menjadi indikasi adanya permasalahan dalam penerimaan siswa, kualitas pengajaran, atau dukungan akademik.
3. Tingkat kelulusan yang rendah berdampak pada evaluasi performa institusi secara keseluruhan.

Dengan memahami permasalahan ini, Jaya Jaya Institut berusaha untuk mendeteksi siswa yang berpotensi dropout sejak dini dan merancang intervensi yang tepat.

## Permasalahan Bisnis
Permasalahan yang akan diselesaikan dalam proyek ini adalah:
1. Bagaimana cara mengidentifikasi siswa-siswa yang berpotensi mengalami dropout sejak dini?
2. Faktor-faktor apa saja yang paling berpengaruh terhadap keputusan siswa untuk dropout?
3. Apa yang dapat dilakukan untuk meningkatkan tingkat retensi siswa dan memastikan lebih banyak siswa menyelesaikan pendidikan mereka?

## Cakupan Proyek
Proyek ini mencakup tahapan sebagai berikut:
1. **Analisis Data**: Menganalisis data untuk mengidentifikasi faktor-faktor utama yang memengaruhi dropout siswa.
2. **Visualisasi & Pelaporan**: Mengembangkan dashboard interaktif untuk memonitor data dan memahami tren.
3. **Rekomendasi & Intervensi**: Menyediakan rekomendasi strategis berbasis data untuk mengurangi angka dropout.
4. **Pengembangan Sistem Prediksi**: Membangun prototype machine learning untuk memprediksi risiko dropout siswa.

## Persiapan
### Sumber Data
Dataset yang digunakan dalam proyek ini disediakan oleh Jaya Jaya Institut, yang mencakup informasi tentang:
- Status siswa (Dropout, Enrolled, Graduate)
- Nilai akademik (semester 1 dan 2)
- Biaya pendidikan
- Penerimaan beasiswa
- Nilai ujian masuk siswa

### Setup Environment
Langkah-langkah persiapan environment adalah sebagai berikut:

#### 1. Buat Environment Python
```bash
conda create --name proyek-institusi-pendidikan python==3.9.15
conda activate proyek-institusi-pendidikan
```

#### 2. Install Library yang Dibutuhkan
```bash
pip install -r requirements.txt
```

#### 3. Setup Metabase
Menggunakan Metabase untuk pembuatan dashboard:
```bash
docker pull metabase/metabase:v0.46.4
docker run -p 3000:3000 --name metabase metabase/metabase
```
Akses Metabase melalui [http://localhost:3000/setup](http://localhost:3000/setup).

#### 4. Setup Database Supabase
- Buat akun di [Supabase](https://supabase.com/dashboard/sign-in).
- Buat project baru dan salin URI database.
- Kirim dataset ke database menggunakan SQLAlchemy:

```python
from sqlalchemy import create_engine
URL = "DATABASE_URL"  # Ganti dengan URL database Supabase Anda
engine = create_engine(URL)
df.to_sql('dataset', engine)
```

## Business Dashboard
Dashboard ini dirancang untuk membantu Jaya Jaya Institut dalam memantau dan menganalisis faktor-faktor yang memengaruhi status siswa. Fitur-fitur utama dari dashboard meliputi:
1. **Tingkat Persentase Dropout Mahasiswa**: Visualisasi persentase siswa dengan status Dropout, Enrolled, dan Graduate.
2. **Pengaruh Biaya Pendidikan terhadap Status Mahasiswa**: Menganalisis jumlah siswa berdasarkan status biaya pendidikan.
3. **Pengaruh Nilai Akademik terhadap Status**: Menunjukkan hubungan antara nilai akademik siswa dengan status pendidikan mereka.
4. **Beasiswa terhadap Status Pendidikan**: Mengidentifikasi pengaruh beasiswa terhadap tingkat kelulusan siswa.
5. **Pengaruh Nilai Masuk terhadap Status**: Mengetahui bagaimana nilai ujian masuk memengaruhi status siswa.

![Yulia Pratiwi_Dashboard](https://github.com/user-attachments/assets/bb9b95dd-97ad-4572-913c-0a847c6b072e)

Dengan dashboard ini, tim Jaya Jaya Institut dapat memonitor tingkat dropout secara real-time dan melakukan intervensi jika diperlukan.

## Conclusion
Proyek ini berhasil memberikan solusi terhadap permasalahan utama yang dihadapi oleh Jaya Jaya Institut, yaitu tingginya tingkat dropout siswa. 

### Jawaban atas Permasalahan Bisnis:
1. **Mengidentifikasi Siswa yang Berpotensi Dropout**:
   - Dengan menggunakan model machine learning seperti Random Forest, siswa berpotensi dropout dapat diidentifikasi sejak dini dengan tingkat akurasi yang memadai.

2. **Faktor-Faktor yang Berpengaruh terhadap Dropout**:
   - Faktor nilai akademik rendah, beban biaya pendidikan, dan tidak menerima beasiswa berkontribusi besar terhadap risiko dropout.

3. **Strategi untuk Meningkatkan Retensi Siswa**:
   - Dukungan akademik dan finansial yang lebih baik, bimbingan intensif, serta evaluasi kurikulum dapat membantu meningkatkan tingkat kelulusan siswa.

## Rekomendasi Action Items
Untuk mengatasi masalah dropout dan mencapai target retensi siswa, berikut beberapa langkah yang direkomendasikan:

### 1. Implementasi Sistem Pemantauan Siswa Berbasis Data
- Menerapkan model prediktif untuk memonitor risiko dropout siswa secara berkala.
- Memberikan intervensi dini bagi siswa yang terdeteksi berisiko tinggi.

### 2. Pengembangan Program Dukungan Akademik dan Psikologis
- Menyediakan sesi bimbingan belajar tambahan untuk siswa dengan nilai akademik rendah.
- Membuka layanan konseling psikologis bagi siswa yang menghadapi tekanan belajar.

### 3. Optimalisasi Program Beasiswa
- Meningkatkan akses beasiswa bagi siswa yang mengalami kesulitan finansial untuk mencegah dropout.

### 4. Evaluasi dan Penyesuaian Kurikulum
- Mengurangi beban akademik pada semester awal dan meningkatkan fleksibilitas program studi.

Dengan implementasi action items ini, Jaya Jaya Institut diharapkan dapat mengurangi tingkat dropout, meningkatkan retensi siswa, dan menjaga reputasi institusi sebagai penyedia pendidikan berkualitas tinggi.
