
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
| **No** | **Action Item**                | **Deskripsi**                                        | **Deadline**   | **Status** |
|-------|---------------------------------|-----------------------------------------------------|----------------|------------|
| 1     | Buat dan jalankan container Metabase | Menjalankan Metabase di Docker dengan volume lokal  | ✅ Selesai     | ✅ Selesai  |
| 2     | Impor dataset karyawan           | Memasukkan file CSV ke dalam Metabase                | 🕒 Sedang berlangsung | 🔄 Proses |
| 3     | Buat dashboard Metabase         | Buat dashboard berisi 8 visualisasi yang dibutuhkan | 📅 2 hari     | 🔄 Proses |
| 4     | Salin file `.db.mv.db` ke lokal | Pastikan file database `.db.mv.db` tersimpan di lokal| 📅 1 hari     | 🔄 Proses |
| 5     | Backup file database Metabase   | Backup file database secara manual                  | 📅 1 hari     | ⏳ Belum   |
| 6     | Dokumentasi proyek              | Menyusun dokumentasi proyek seperti ini             | 📅 1 hari     | ✅ Selesai  |

## **7. Risiko dan Mitigasi**
| **Risiko**                     | **Dampak**              | **Mitigasi**                                      |
|---------------------------------|------------------------|--------------------------------------------------|
| File `.db.mv.db` hilang         | Hilangnya database      | Backup file `.db.mv.db` ke direktori aman        |
| Docker container gagal berjalan | Metabase tidak bisa diakses | Gunakan perintah `docker logs hranalysis` untuk debug |
| Volume tidak terpasang dengan benar | Database hilang saat restart | Pastikan volume lokal dipetakan ke `/metabase.db`|

## **8. Kesimpulan**
- Proyek **HR Analysis** bertujuan untuk menganalisis tingkat keluar masuk karyawan di perusahaan.
- Menggunakan **Metabase** dengan database **H2** yang disimpan di folder lokal (`.db.mv.db`).
- Dashboard interaktif disusun untuk memberikan informasi kepada manajer dan tim SDM.
