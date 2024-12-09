
# 📘 Dokumentasi Proyek HR Analysis

## **1. Deskripsi Proyek**
Proyek ini bertujuan untuk menganalisis tingkat attrition (keluar masuk karyawan) di perusahaan menggunakan **Metabase** sebagai alat visualisasi. Data karyawan disimpan dalam database **H2** secara default, tetapi dapat dipindahkan ke database eksternal seperti PostgreSQL atau MySQL untuk keperluan produksi. 

Visualisasi data meliputi analisis tingkat keluar karyawan berdasarkan:
- **Gender (Jenis Kelamin)**
- **Marital Status (Status Pernikahan)**
- **Job Role (Posisi Pekerjaan)**
- **Department (Departemen)**
- **Overtime (Lembur)**
- **Job Satisfaction (Kepuasan Kerja)**
- **Age (Usia)**

## **2. Tujuan Proyek**
1. **Menganalisis faktor-faktor yang memengaruhi tingkat attrition** di perusahaan.
2. **Menyediakan visualisasi berbasis dashboard** untuk mempermudah pemahaman pola data.
3. **Menyimpan database H2** di folder lokal dengan format `.db.mv.db` agar mudah untuk dibackup dan digunakan kembali.

## **3. Lingkup Proyek**
1. **Data Sumber**: 
   - File CSV yang berisi informasi karyawan seperti usia, gender, status pernikahan, dan status pekerjaan.
   
2. **Alat dan Teknologi**:
   - **Docker**: Menjalankan Metabase dalam container.
   - **Metabase**: Alat visualisasi data dan pembuatan dashboard.
   - **H2 Database**: Digunakan sebagai database default Metabase.

3. **Dashboard Visualisasi**:
   - **Total Employee & Overall Attrition Rate**: Menampilkan jumlah total karyawan dan tingkat attrition.
   - **Impact of Overtime on Attrition**: Menganalisis pengaruh lembur terhadap attrition.
   - **Attrition Rate by Gender**: Menampilkan tingkat attrition berdasarkan gender.
   - **Attrition by Marital Status**: Menampilkan tingkat attrition berdasarkan status pernikahan.
   - **Attrition by Job Role**: Menampilkan tingkat attrition berdasarkan peran pekerjaan.
   - **Attrition by Department**: Menampilkan tingkat attrition berdasarkan departemen.
   - **Attrition by Age Group**: Menampilkan tingkat attrition berdasarkan usia.
   - **Job Satisfaction vs Attrition**: Menganalisis pengaruh kepuasan kerja terhadap tingkat attrition.

## Business Understanding
Jaya Jaya Maju merupakan perusahaan multinasional yang berdiri sejak tahun 2000, dengan lebih dari 1000 karyawan yang tersebar di seluruh negeri. Meskipun perusahaan ini telah berkembang menjadi cukup besar, mereka masih menghadapi tantangan signifikan dalam mengelola karyawannya. Salah satu dampak utama dari tantangan ini adalah tingginya *attrition rate*, yaitu rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan, yang mencapai lebih dari 10%. Tingginya *attrition rate* ini mengindikasikan adanya masalah dalam mempertahankan karyawan, yang dapat berdampak negatif pada produktivitas, biaya rekrutmen, dan stabilitas operasional perusahaan.

### Permasalahan Bisnis

1. Seberapa tinggi tingkat attrition di perusahaan ini?
2. Faktor-faktor apa saja yang mempengaruhi keputusan karyawan untuk meninggalkan perusahaan?
3. Apakah ada perbedaan tingkat attrition berdasarkan role atau departemen tertentu di perusahaan?
4. Bagaimana pengaruh lembur (overtime) terhadap keputusan karyawan untuk keluar dari perusahaan?

### Cakupan Proyek

* Analisis Data: Menggunakan data karyawan yang ada untuk mengidentifikasi faktor-faktor utama yang mempengaruhi attrition.
* Visualisasi & Pelaporan: Mengembangkan dashboard bisnis yang dapat digunakan oleh manajer HR untuk memonitor dan menganalisis faktor-faktor tersebut secara visual.
* Rekomendasi & Intervensi: Berdasarkan hasil analisis, memberikan rekomendasi untuk intervensi yang dapat dilakukan untuk mengurangi attrition rate dan meningkatkan kepuasan karyawan.

## **4. Struktur Proyek**
```
project-root/
├── data/
│   └── employee_dataset.csv  # Dataset utama
├── metabase/
│   └── metabase.db.mv.db     # File database Metabase (dari H2)
├── docker-compose.yml        # Konfigurasi Docker untuk Metabase
├── documentation.md          # Dokumentasi proyek ini
└── README.md                 # Panduan utama proyek
```

## **5. Cara Menjalankan Proyek**

### **1️⃣ Jalankan Metabase dengan Docker**
Jalankan perintah berikut di terminal PowerShell atau Command Prompt:

```
docker run -d -p 3000:3000 --name hranalysis -v C:\Users\62859\Temporary:/metabase.db metabase/metabase
```

### **2️⃣ Akses Metabase**
1. Buka browser dan kunjungi **http://localhost:3000**.
2. Lakukan konfigurasi awal:
   - Buat akun admin.
   - Pilih **H2 Database** sebagai default database.
   
### **3️⃣ Impor Dataset**
1. Impor file CSV melalui Metabase.
2. Buat **Dashboard** dengan menggunakan question berikut:
   - Total Employee & Attrition Rate
   - Impact of Overtime on Attrition
   - Attrition Rate by Gender
   - Attrition by Marital Status
   - Attrition by Job Role
   - Attrition by Department
   - Attrition by Age Group
   - Job Satisfaction vs Attrition

## **6. Action Items (Tugas yang Harus Dilakukan)**
| **No** | **Action Item**                   | **Deskripsi**                                        | **Deadline** | **Status**   |
|--------|------------------------------------|------------------------------------------------------|---------------|--------------|
| 1      | Pembuatan Model Machine Learning   | Melatih model prediksi attrition di Google Colab    | ✅ Selesai    | ✅ Selesai   |
| 2      | Buat dan jalankan container Metabase | Menjalankan Metabase di Docker dengan volume lokal  | ✅ Selesai    | ✅ Selesai   |
| 3      | Impor dataset karyawan              | Memasukkan file CSV ke dalam Metabase                | ✅ Selesai    | ✅ Selesai   |
| 4      | Buat dashboard Metabase            | Buat dashboard berisi 8 visualisasi yang dibutuhkan | ✅ Selesai    | ✅ Selesai   |
| 5      | Salin file `.db.mv.db` ke lokal    | Pastikan file database `.db.mv.db` tersimpan di lokal| ✅ Selesai    | ✅ Selesai   |
| 6      | Backup file database Metabase      | Backup file database secara manual                   | ✅ Selesai    | ✅ Selesai   |
| 7      | Dokumentasi proyek                 | Menyusun dokumentasi proyek seperti ini              | ✅ Selesai    | ✅ Selesai   |

## **7. Risiko dan Mitigasi**
| **Risiko**                     | **Dampak**              | **Mitigasi**                                      |
|---------------------------------|------------------------|--------------------------------------------------|
| File `.db.mv.db` hilang         | Hilangnya database      | Backup file `.db.mv.db` ke direktori aman        |
| Docker container gagal berjalan | Metabase tidak bisa diakses | Gunakan perintah `docker logs hranalysis` untuk debug |
| Volume tidak terpasang dengan benar | Database hilang saat restart | Pastikan volume lokal dipetakan ke `/metabase.db`|

## **8. Business Dashboard**

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
