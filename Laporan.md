# Laporan Proyek Machine Learning - Yulia Pratiwi
## Domain Proyek
Penyakit jantung merupakan salah satu penyebab utama kematian di seluruh dunia, dengan jutaan kasus baru dilaporkan setiap tahun. Deteksi dini dan penanganan yang tepat menjadi langkah krusial untuk menurunkan angka kematian akibat penyakit ini. Namun, proses diagnosa tradisional sering kali membutuhkan waktu yang lama, biaya yang besar, serta ketergantungan pada keahlian medis yang terbatas di beberapa daerah.

Di era digital ini, data medis pasien seperti usia, tekanan darah, kadar kolesterol, dan faktor risiko lainnya dapat dimanfaatkan secara optimal melalui teknologi kecerdasan buatan (AI) dan machine learning. Teknologi ini memungkinkan pembuatan model prediktif yang dapat membantu tenaga medis menganalisis risiko penyakit jantung secara lebih cepat, akurat, dan efisien.

Proyek ini bertujuan untuk mengembangkan model machine learning berbasis klasifikasi guna memprediksi risiko penyakit jantung. Dengan memanfaatkan dataset medis yang berisi berbagai parameter seperti usia, jenis kelamin, tekanan darah, kolesterol, dan hasil tes lainnya, model ini dapat membantu dalam pengambilan keputusan klinis. Diharapkan solusi ini tidak hanya meningkatkan akurasi prediksi, tetapi juga berkontribusi dalam mempercepat diagnosa serta mendukung upaya pencegahan penyakit jantung secara lebih luas.

### Referensi
- Shi, A., Tao, Z., Wei, P., & Zhao, J. (2016). Epidemiological aspects of heart diseases. Experimental and therapeutic medicine, 12(3), 1645-1650.
- Centers for Disease Control, Prevention (US), National Center for Health Statistics (US), & National Vital Statistics System (US). (1998). National Vital Statistics Reports: From the Centers for Disease Control and Prevention, National Center for Health Statistics, National Vital Statistics System (Vol. 49). National Center for Health Statistics.
- Chaki, D., Das, A., & Zaber, M. I. (2015). A comparison of three discrete methods for classification of heart disease data. Bangladesh Journal of Scientific and Industrial Research, 50(4), 293-296.
- Rani, K. U. (2011). Analysis of heart diseases dataset using neural network approach. arXiv preprint arXiv:1110.2626.
## Business Understanding
### Problem Statements
1. Penyakit jantung menjadi salah satu penyebab utama kematian global, namun metode diagnosa tradisional memerlukan waktu yang lama dan bergantung pada ketersediaan tenaga medis yang terampil.
2. Banyak dataset medis yang mengandung informasi penting, tetapi belum dimanfaatkan secara optimal untuk membantu prediksi penyakit menggunakan teknologi kecerdasan buatan.
3. Tingkat akurasi model prediksi penyakit jantung yang rendah dapat mengakibatkan diagnosa yang tidak akurat, sehingga membahayakan pasien.

### Goals:
1. Mengembangkan model machine learning berbasis klasifikasi yang mampu memprediksi risiko penyakit jantung secara cepat dan efisien, sehingga dapat membantu mempercepat diagnosa medis.
2. Memanfaatkan dataset medis yang berisi berbagai parameter pasien, seperti tekanan darah, kadar kolesterol, dan faktor risiko lainnya, untuk membuat model prediksi berbasis data.
3. Meningkatkan performa model prediksi melalui pengujian berbagai algoritma machine learning dan optimasi parameter untuk memastikan hasil prediksi yang akurat dan andal.

### Solution Statement:
1. Menggunakan algoritma klasifikasi seperti Logistic Regression, Random Forest, dan Support Vector Machine (SVM) untuk membangun model baseline, kemudian membandingkan kinerjanya berdasarkan metrik evaluasi seperti akurasi, precision, recall, dan F1-score.
2. Melakukan improvement pada model terbaik melalui hyperparameter tuning (misalnya, menggunakan GridSearchCV atau RandomizedSearchCV) untuk mendapatkan parameter optimal yang meningkatkan kinerja model.
3. Menerapkan metode pengurangan dimensi seperti PCA (Principal Component Analysis) jika diperlukan, untuk meningkatkan efisiensi model pada dataset dengan fitur yang tinggi.
4. Menggunakan teknik validasi silang (cross-validation) untuk memastikan model yang dikembangkan memiliki performa yang stabil pada data yang berbeda.
## Business Understanding
### Dataset
Dataset yang digunakan dalam proyek ini berasal dari [Kaggle - Heart Disease Prediction Dataset](https://www.kaggle.com/datasets/mfarhaannazirkhan/heart-dataset?select=raw_merged_heart_dataset.csv)

### Informasi Dataset
Informasi dataset diberikan menggunakan fungsi `data.info()`. Berikut adalah hasilnya:
### **Gambaran Dataset**
| Nama Fitur  | Jumlah Non-Null | Tipe Data | Deskripsi |
|-------------|-----------------|-----------|-----------|
| `age`       | 2181           | int64     | Usia pasien (numerik). |
| `sex`       | 2181           | int64     | Jenis kelamin pasien (1 = laki-laki, 0 = perempuan). |
| `cp`        | 2181           | int64     | Jenis nyeri dada (0: angina tipikal, 1: angina atipikal, 2: nyeri non-angina, 3: asimptomatik). |
| `trestbps`  | 2181           | object    | Tekanan darah saat istirahat (dalam mm Hg). |
| `chol`      | 2181           | object    | Tingkat kolesterol serum (dalam mg/dl). |
| `fbs`       | 2181           | object    | Gula darah puasa > 120 mg/dl (1 = ya, 0 = tidak). |
| `restecg`   | 2181           | object    | Hasil elektrokardiografi saat istirahat (0: normal, 1: abnormalitas gelombang ST-T, 2: hipertrofi ventrikel kiri). |
| `thalachh`  | 2181           | object    | Detak jantung maksimum yang dicapai. |
| `exang`     | 2181           | object    | Angina yang diinduksi oleh olahraga (1 = ya, 0 = tidak). |
| `oldpeak`   | 2181           | float64   | Depresi segmen ST yang diinduksi oleh olahraga dibandingkan saat istirahat. |
| `slope`     | 2181           | object    | Kemiringan segmen ST puncak selama olahraga (0: naik, 1: datar, 2: turun). |
| `ca`        | 2181           | object    | Jumlah pembuluh besar (0-3) yang terlihat melalui fluoroskopi. |
| `thal`      | 2181           | object    | Jenis thalasemia (1: normal, 2: cacat tetap, 3: cacat reversibel). |
| `target`    | 2181           | int64     | Variabel target (1 = risiko lebih tinggi serangan jantung, 0 = risiko lebih rendah). |

### **Statistik Deskriptif**

| Fitur      | Jumlah | Rata-rata | Standar Deviasi | Min | 25%   | 50%   | 75%   | Max  |
|------------|--------|-----------|-----------------|-----|-------|-------|-------|------|
| `age`      | 2181   | 53.48     | 9.19            | 28  | 46.00 | 54.00 | 60.00 | 77   |
| `sex`      | 2181   | 0.69      | 0.46            | 0   | 0.00  | 1.00  | 1.00  | 1    |
| `cp`       | 2181   | 1.51      | 1.37            | 0   | 0.00  | 2.00  | 2.00  | 4    |
| `oldpeak`  | 2181   | 0.99      | 1.14            | 0.0 | 0.00  | 0.60  | 1.60  | 6.20 |
| `target`   | 2181   | 0.50      | 0.50            | 0   | 0.00  | 0.00  | 1.00  | 1    |


## Kesimpulan Data Understanding

1. **Informasi Dataset**:
   - Dataset terdiri dari **2181 baris** dan **14 kolom**, dengan beberapa kolom numerik dan kategorikal.
   - Kolom target (`target`) adalah variabel dependen yang ingin diprediksi, dengan nilai:
     - **0**: Risiko rendah penyakit jantung.
     - **1**: Risiko tinggi penyakit jantung.

2. **Distribusi Variabel Target**:
   - Distribusi target menunjukkan bahwa data relatif seimbang antara risiko rendah dan tinggi, sehingga cocok untuk model klasifikasi.

3. **Distribusi Umur**:
   - Usia pasien berkisar antara **28 hingga 77 tahun**.
   - Sebagian besar pasien berada dalam rentang usia **46 hingga 60 tahun**, menunjukkan kelompok usia yang lebih rentan terhadap risiko penyakit jantung.

4. **Proporsi Jenis Kelamin**:
   - Mayoritas pasien adalah **laki-laki** (69%), sedangkan pasien perempuan mencakup 31%.

5. **Korelasi Antar Variabel**:
   - Variabel numerik seperti `age`, `trestbps`, `chol`, `thalachh`, dan `oldpeak` memiliki korelasi yang bervariasi dengan variabel target.
   - `thalachh` (detak jantung maksimum) dan `oldpeak` menunjukkan korelasi signifikan dengan target.

6. **Distribusi Nyeri Dada**:
   - Tipe nyeri dada kategori **2 (Non-anginal pain)** dan **3 (Asymptomatic)** mendominasi dataset, menunjukkan keterkaitan dengan risiko penyakit jantung.

7. **Kondisi Tekanan Darah dan Oldpeak**:
   - Pasien dengan tekanan darah lebih tinggi (`trestbps`) dan `oldpeak` cenderung memiliki risiko lebih tinggi terkena penyakit jantung.


**Catatan Penting**:
Hasil dari tahap data understanding ini memberikan wawasan awal untuk menentukan variabel penting, menangani data outlier, dan mengarahkan langkah preprocessing serta pemilihan model yang optimal.

## Data Preparation

Pada tahap ini, dilakukan beberapa proses untuk mempersiapkan data agar siap digunakan dalam pelatihan model machine learning. Berikut adalah langkah-langkah yang diterapkan:

### 1. Mengganti Nilai `?` dengan NaN
- **Proses**: Nilai `?` dalam dataset diubah menjadi `NaN` menggunakan fungsi `replace`.
- **Alasan**: Nilai `?` dianggap sebagai data yang hilang (missing value) sehingga perlu diubah menjadi format yang dapat dikenali oleh library Python.

### 2. Menghapus Baris dengan Missing Values
- **Proses**: Baris yang mengandung nilai `NaN` dihapus menggunakan fungsi `dropna`.
- **Alasan**: Baris dengan missing values dapat memengaruhi hasil analisis dan pelatihan model, sehingga dihapus untuk menjaga kualitas data.

### 3. Memisahkan Fitur dan Target
- **Proses**: Data dipisahkan menjadi fitur (X) dan target (y) menggunakan `drop` untuk fitur dan indexing untuk target.
- **Alasan**: Proses ini diperlukan untuk mempersiapkan data dalam format yang sesuai untuk pelatihan model.

### 4. Normalisasi Data Numerik
- **Proses**: Data numerik dinormalisasi menggunakan teknik Min-Max Scaling atau Standard Scaling agar setiap fitur memiliki skala yang sama.
- **Alasan**: Normalisasi diperlukan untuk mencegah bias pada fitur tertentu yang memiliki skala lebih besar dibandingkan fitur lainnya.

### 5. Mengonversi Data Kategorikal menjadi Variabel Dummy
- **Proses**: Data kategorikal diubah menjadi variabel dummy menggunakan fungsi `pd.get_dummies` dengan opsi `drop_first=True`.
- **Alasan**: Model machine learning memerlukan data dalam format numerik, sehingga data kategorikal perlu dikonversi ke format ini.

### 6. Membagi Dataset menjadi Data Latih dan Uji
- **Proses**: Data dibagi menjadi data latih (80%) dan data uji (20%) menggunakan fungsi `train_test_split`.
- **Alasan**: Pembagian ini diperlukan untuk mengevaluasi performa model secara objektif pada data yang belum pernah dilihat model sebelumnya.

---
## Modeling

Pada tahap ini, dilakukan pemodelan data menggunakan berbagai algoritma machine learning untuk memprediksi penyakit jantung. Model yang digunakan meliputi Logistic Regression, Random Forest, Support Vector Machine (SVM), dan Deep Learning. Setiap model dievaluasi berdasarkan metrik akurasi, precision, recall, dan F1-score.

---

### 1. Logistic Regression
Logistic Regression adalah model sederhana namun efektif untuk masalah klasifikasi biner. Model ini memprediksi probabilitas data termasuk dalam kelas tertentu menggunakan fungsi logistik.

- **Hasil Evaluasi**:
  - **Akurasi**: 0.716931
  - **Precision**: 0.684444
  - **Recall**: 0.810526
  - **F1 Score**: 0.742169

**Kelebihan**:
- Cepat dalam pelatihan dan prediksi.
- Mudah diinterpretasikan dan sederhana.

**Kekurangan**:
- Tidak optimal pada data dengan pola yang kompleks atau non-linear.

#### **Cara Kerja**:
1. Model mempelajari hubungan antara fitur dan target selama pelatihan.
2. Probabilitas diprediksi untuk setiap data.
3. Jika probabilitas lebih dari 0.5, data diklasifikasikan sebagai positif (risiko serangan jantung). Jika tidak, diklasifikasikan sebagai negatif.

---

### 2. Random Forest
Random Forest adalah model ensemble yang menggabungkan banyak pohon keputusan untuk menghasilkan prediksi yang akurat dan stabil.

- **Hasil Evaluasi**:
  - **Akurasi**: 0.965608
  - **Precision**: 0.973262
  - **Recall**: 0.957895
  - **F1 Score**: 0.965517

**Kelebihan**:
- Menangani fitur tidak seimbang dengan baik.
- Resisten terhadap overfitting dibandingkan pohon keputusan tunggal.

**Kekurangan**:
- Membutuhkan lebih banyak sumber daya komputasi.

#### **Cara Kerja**:
1. Dataset dibagi menjadi subset acak.
2. Setiap subset digunakan untuk melatih pohon keputusan independen.
3. Prediksi ditentukan melalui voting mayoritas dari semua pohon.

---

### 3. Support Vector Machine (SVM)
SVM mencoba memisahkan data dengan hyperplane optimal di ruang fitur.

- **Hasil Evaluasi**:
  - **Akurasi**: 0.865079
  - **Precision**: 0.845771
  - **Recall**: 0.894737
  - **F1 Score**: 0.869565

**Kelebihan**:
- Baik untuk data berskala kecil dengan banyak fitur.
- Memiliki margin yang jelas antara kelas.

**Kekurangan**:
- Tidak efisien untuk dataset besar.
- Membutuhkan tuning parameter yang lebih kompleks.

#### **Cara Kerja**:
1. SVM mencari hyperplane dengan margin maksimum antara dua kelas.
2. Jika data tidak dapat dipisahkan langsung, kernel digunakan untuk mentransformasi data ke dimensi lebih tinggi.

---

### 4. Deep Learning
Deep Learning menggunakan Neural Network dengan beberapa lapisan untuk menangkap pola data yang kompleks.

- **Arsitektur**:
  - Input layer: Menggunakan jumlah fitur dalam dataset.
  - Hidden layers: Dua hidden layer dengan 64 dan 32 neuron.
  - Output layer: Satu neuron dengan fungsi aktivasi sigmoid.

- **Hasil Evaluasi**:
  - **Akurasi**: 0.814815
  - **Precision**: 0.785714
  - **Recall**: 0.868421
  - **F1 Score**: 0.825000

**Kelebihan**:
- Mampu menangkap pola kompleks dalam data.
- Skalabilitas tinggi untuk dataset besar.

**Kekurangan**:
- Membutuhkan waktu pelatihan lebih lama.
- Sulit diinterpretasikan dibandingkan model lainnya.

#### **Cara Kerja**:
1. Data diproses melalui beberapa lapisan tersembunyi.
2. Setiap lapisan menerapkan fungsi aktivasi untuk menangkap pola non-linear.
3. Output layer memprediksi probabilitas target.
4. Model dilatih secara iteratif untuk meminimalkan kesalahan prediksi.

---

### Tabel Hasil Evaluasi

| Model               | Akurasi  | Precision | Recall   | F1 Score |
|---------------------|----------|-----------|----------|----------|
| Logistic Regression  | 0.716931 | 0.684444  | 0.810526 | 0.742169 |
| Random Forest        | 0.965608 | 0.973262  | 0.957895 | 0.965517 |
| Support Vector Machine (SVM) | 0.865079 | 0.845771  | 0.894737 | 0.869565 |
| Deep Learning        | 0.814815 | 0.785714  | 0.868421 | 0.825000 |

## Analisis Confusion Matrix


## 1. Logistic Regression:
- **True Positives (TP)**: 154 (Heart Disease yang diprediksi dengan benar sebagai Heart Disease).
- **True Negatives (TN)**: 117 (No Heart Disease yang diprediksi dengan benar sebagai No Heart Disease).
- **False Positives (FP)**: 71 (No Heart Disease yang diprediksi sebagai Heart Disease).
- **False Negatives (FN)**: 36 (Heart Disease yang diprediksi sebagai No Heart Disease).

Model ini memiliki cukup banyak **False Positives** dan **False Negatives**, yang menunjukkan bahwa model ini kurang optimal dalam membedakan kelas *Heart Disease* dan *No Heart Disease*.

## 2. Random Forest:
- **True Positives (TP)**: 182 (Heart Disease yang diprediksi dengan benar sebagai Heart Disease).
- **True Negatives (TN)**: 183 (No Heart Disease yang diprediksi dengan benar sebagai No Heart Disease).
- **False Positives (FP)**: 5 (No Heart Disease yang diprediksi sebagai Heart Disease).
- **False Negatives (FN)**: 8 (Heart Disease yang diprediksi sebagai No Heart Disease).

Model **Random Forest** menunjukkan hasil yang sangat baik dengan sedikit kesalahan (**FP** dan **FN** sangat rendah). Ini menunjukkan bahwa model ini sangat baik dalam klasifikasi kedua kelas, dengan tingkat akurasi yang tinggi.

## 3. Support Vector Machine (SVM):
- **True Positives (TP)**: 170 (Heart Disease yang diprediksi dengan benar sebagai Heart Disease).
- **True Negatives (TN)**: 157 (No Heart Disease yang diprediksi dengan benar sebagai No Heart Disease).
- **False Positives (FP)**: 31 (No Heart Disease yang diprediksi sebagai Heart Disease).
- **False Negatives (FN)**: 20 (Heart Disease yang diprediksi sebagai No Heart Disease).

Model **SVM** memiliki performa yang baik, tetapi masih ada beberapa kesalahan klasifikasi (**FP** dan **FN**). Meskipun demikian, model ini cukup seimbang dalam memprediksi kedua kelas.

## 4. Deep Learning:
- **True Positives (TP)**: 165 (Heart Disease yang diprediksi dengan benar sebagai Heart Disease).
- **True Negatives (TN)**: 143 (No Heart Disease yang diprediksi dengan benar sebagai No Heart Disease).
- **False Positives (FP)**: 45 (No Heart Disease yang diprediksi sebagai Heart Disease).
- **False Negatives (FN)**: 25 (Heart Disease yang diprediksi sebagai No Heart Disease).

Model **Deep Learning** menunjukkan hasil yang baik meskipun masih ada beberapa **False Positives** dan **False Negatives**. Model ini menunjukkan kemampuan yang baik dalam memprediksi penyakit jantung, tetapi masih ada ruang untuk perbaikan dalam klasifikasi.

## Kesimpulan:
- **Random Forest** menunjukkan performa terbaik dengan sedikit kesalahan dalam klasifikasi (**FP** dan **FN** rendah).
- **Logistic Regression** menunjukkan kinerja yang lebih buruk, dengan lebih banyak kesalahan dalam klasifikasi.
- **SVM** dan **Deep Learning** memiliki hasil yang lebih seimbang, dengan **SVM** sedikit lebih baik daripada **Deep Learning** dalam hal jumlah kesalahan.

Penting untuk mencatat bahwa metrik-metrik lain seperti **Precision**, **Recall**, dan **F1-Score** dapat memberikan gambaran lebih lengkap tentang performa masing-masing model dalam klasifikasi.


