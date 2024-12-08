<h1 align="left">Rekomendasi Buku -- Yulia Pratiwi</h1>

## Domain Proyek
Sistem Rekomendasi Buku Berdasarkan Preferensi Pengguna dan Kategori Buku

### Latar Belakang
Perkembangan era digital telah mendorong masyarakat untuk semakin banyak memanfaatkan media digital dalam berbagai aspek kehidupan, termasuk dalam mencari dan membaca buku. Namun, dengan jumlah buku yang terus bertambah dan beragamnya pilihan, pengguna sering kali menghadapi kesulitan dalam menentukan buku yang sesuai dengan minat mereka (Widiastuti et al., 2022). Situasi ini dapat menjadi penghambat dalam upaya meningkatkan minat baca dan literasi di kalangan masyarakat. Selain itu, keterbatasan waktu serta kebutuhan akan akses yang praktis membuat pencarian buku secara manual, baik di toko fisik maupun di situs daring, menjadi kurang efisien (Al-Rosyid et al., 2021).

Untuk menjawab tantangan ini, sistem rekomendasi buku yang cerdas dan efektif menjadi solusi yang sangat dibutuhkan. Teknologi ini memungkinkan pengguna untuk menemukan buku yang sesuai dengan preferensi mereka dengan lebih cepat dan mudah, tanpa harus melalui proses pencarian yang memakan waktu. Dengan demikian, sistem rekomendasi ini diharapkan dapat meningkatkan minat baca dan memperluas aksesibilitas terhadap berbagai kategori buku, sekaligus memberikan dampak positif terhadap peningkatan literasi masyarakat secara umum (Nurpuzianah et al., 2023).

#### Urgensi Proyek
Meningkatkan minat baca dan mempermudah akses terhadap berbagai jenis buku berpotensi memberikan kontribusi signifikan dalam membangun budaya literasi yang lebih baik (Nurpuzianah et al., 2023). Kehadiran sistem rekomendasi buku ini diharapkan dapat membantu pengguna menemukan bacaan yang relevan dengan minat mereka secara lebih efektif dan efisien.

## Reference
[1] Widiastuti, Y., Lestari, O. W., & Ambarwati, A. (2022). Preferensi media bacaan sastra siswa SMAN 1 Kraksaan: Cetak atau digital?. KEMBARA: Jurnal Keilmuan Bahasa, Sastra, Dan Pengajarannya, 8(2), 272-287.

[2] Al-Rosyid, H., Purnama, B. E., & Uly, I. (2021). Sistem informasi penjualan buku berbasis website pada toko buku standard book seller pacitan. Menulis Buku Digital Modern, 33.

[3] Nurpuzianah, M., Naashir, F. A., & Fitriyah, M. (2023). Peranan Perpustakaan Taman Literasi Dalam Meningkatkan Budaya Cinta Membaca. Jurnal Literasi dan Pembelajaran Indonesia, 3(2), 282-288.

## Business Undertanding
Dalam mengembangkan sistem rekomendasi buku, diharapkan dapat memahami bahwa terdapat beberapa permasalahan yang perlu dipecahkan serta tujuan yang ingin dicapai untuk permasalahan yang telah dijelaskan di atas.

### Problem Statements
1. Bagaimana cara menyajikan rekomendasi buku yang sesuai dengan preferensi pengguna?
2. Bagaimana cara meningkatkan kolaborasi antar pengguna untuk memberikan rekomendasi buku yang relevan?
3. Bagaimana cara menghasilkan model rekomendasi menggunakan collaborative filtering dengan nilai metriks evaluasi precision > 0.80 dan mean squared error (mse) < 0.15?

### Goals
1. Menciptakan sistem rekomendasi buku yang dapat mempersonalisasi rekomendasi berdasarkan preferensi pengguna.
2. Meningkatkan interaksi dan kolaborasi antar pengguna dalam memberikan rekomendasi buku yang relevan.
3. Menghasilkan model rekomendasi menggunakan collaborative filtering dengan nilai metriks evaluasi precision > 0.80 dan mean squared error (mse) < 0.15.

### Solution Approach
1. Mengembangkan metode content-based filtering untuk memberikan rekomendasi buku yang sesuai dengan preferensi pengguna berdasarkan analisis konten buku yang telah mereka sukai sebelumnya.
2. Mengembangkan collaborative filtering untuk memfasilitasi kolaborasi antar pengguna dalam memberikan rekomendasi buku yang sesuai dengan minat dan kategori yang relevan.
3. Penggunaan teknik-teknik data preprocessing dalam membangun model collaborative filtering untuk meningkatkan nilai precision dan mengurangi mean squared error (mse) dari model.


## Data Understanding
Proyek ini akan memanfaatkan salah satu dataset yang bersifat open-source dari situs [Kaggle](https://www.kaggle.com/datasets). Dataset yang digunakan di upload dan diperbarui oleh Ruchi Bhatia dengan judul dataset *Book-Crossing: User Review Ratings* yang dapat diakses melalui [link ini](https://www.kaggle.com/datasets/ruchi798/bookcrossing-dataset). Dataset ini terdiri atas 4 file berekstensi `.csv` dengan nama `BX-Book-Ratings.csv`, `BX-Users.csv`, `BX_Books.csv`, dan `Preprocessed_data.csv`.

Dataset ini merupakan kumpulan data dari judul buku, penulis/pencipta buku, penerbit, tahun terbit, kategori buku, hingga rating dari setiap user yang tersebar dari 4 file yang sebelumnya telah disebutkan. Dengan demikian, dataset ini dapat digunakan untuk berbagai analisis dan tugas pembelajaran mesin, termasuk tetapi tidak terbatas pada analisis perilaku pembaca berdasarkan peringkat buku yang diberikan, analisis tren dalam preferensi pembaca terhadap genre tertentu atau penulis tertentu, ataupun yang akan diangkat pada proyek kali ini, yaitu membangun sistem rekomendasi berdasarkan kategori buku.

### Deskripsi Dataset
Dataset yang digunakan adalah [Book-Crossing Dataset](https://www.kaggle.com/datasets/ruchi798/bookcrossing-dataset), terdiri dari:
- **BX-Book-Ratings.csv:** Data rating buku.
- **BX-Users.csv:** Informasi pengguna.
- **BX-Books.csv:** Informasi buku.
- **Preprocessed_data.csv:** Data gabungan hasil preprocessing.


---

Fitur pada keempat Dataset akan dipaparkan dalam beberapa tabel berikut:

*Tabel 1. Fitur pada `BX-Book-Ratings.csv`*

| Nama fitur | Deskripsi |
| ---------- | --------- |
| User-ID | id untuk mengidentifikasi pengguna |
| ISBN | nomor isbn atau kode identifikasi unik dari setiap buku |
| Book-Rating | rating buku dari setiap pengguna |

*Tabel 2. Fitur pada `BX-Users.csv`*

| Nama fitur | Deskripsi |
| ---------- | --------- |
| User-ID | id untuk mengidentifikasi pengguna |
| Location | lokasi dari pengguna |
| Age | umur pengguna |

*Tabel 3. Fitur pada `BX_Books.csv`*

| Nama fitur | Deskripsi |
| ---------- | --------- |
| ISBN | nomor isbn atau kode identifikasi unik dari setiap buku |
| Book_Title | judul buku |
| Book_Author | penulis/pencipta buku |
| Year-Of-Publication | tahun terbit buku |
| Publisher | lembaga/penerbit buku | 
| Image-URL-S | sampul buku berukuran kecil |
| Image-URL-M | sampul buku berukuran sedang |
| Image-URL-L | sampul buku berukuran besar |
| Book-Rating | rating buku dari setiap pengguna |

*Tabel 4. Fitur pada `Preprocessed_data.csv`*

| Nama fitur           | Deskripsi                                       |
|----------------------|-------------------------------------------------|
| Unnamed: 0           | index dari baris                                |
| user_id              | id untuk mengidentifikasi pengguna              |
| location             | lokasi dari pengguna                            |
| age                  | umur pengguna                                   |
| isbn                 | kode identifikasi unik dari setiap buku         |
| rating               | rating buku                                     |
| book_title           | judul buku                                      |
| book_author          | penulis/pencipta buku                           |
| year_of_publication  | tahun terbit buku                               |
| publisher            | lembaga/penerbit buku                           |
| img_s                | sampul buku berukuran kecil                     |
| img_m                | sampul buku berukuran sedang                    |
| img_l                | sampul buku berukuran besar                     |
| Summary              | deskripsi singkat terkait judul buku            |
| Language             | bahasa yang digunakan pada buku                 |
| Category             | kategori buku                                   |
| city                 | kota dari pengguna                              |
| state                | negara bagian dari pengguna                     |
| country              | negara dari pengguna                            |


Berdasarkan tabel-tabel di atas, maka pada proyek kali ini akan menggunakan salah satu data saja dengan nama `Preprocessed_data.csv`. Sebab pada file tersebut, informasi yang diberikan lengkap dan ada beberapa fitur yang tidak ada pada file lain seperti yang dapat dilihat pula pada tabel 1-3. Proses selanjutnya adalah mengecek jumlah nilai unik yang terkandung dari setiap kolom atau fitur yang ada, yang dapat dilihat pada tabel 5.

*Tabel 5. Jumlah Nilai Unik pada `Preprocessed_data.csv`*

| Nama fitur             | Deskripsi            |
|------------------------|----------------------|
| Unnamed: 0             | 1031175              |
| user_id                | 92107                |
| location               | 22480                |
| age                    | 93                   |
| isbn                   | 270170               |
| rating                 | 11                   |
| book_title             | 241090               |
| book_author            | 101594               |
| year_of_publication    | 104                  |
| publisher              | 16729                |
| img_s                  | 269861               |
| img_m                  | 269861               |
| img_l                  | 269861               |
| Summary                | 136911               |
| Language               | 33                   |
| Category               | 6448                 |
| city                   | 14767                |
| state                  | 2123                 |
| country                | 414                  |

Setelah melakukan observasi pada dataset yang diunduh pada kaggle, didapat informasi sebagai berikut:
- Terdapat 1031175 baris dalam _dataset_
- Terdapat 19 kolom yaitu 'Unnamed: 0', 'user_id', 'location', 'age', 'isbn', 'rating', 'book_title', 'book_author', 'year_of_publication', 'publisher', 'img_s', 'img_m', 'img_l', 'Summary', 'Language', 'Category', 'city', 'state', 'country'.  

Untuk penjelasan mengenai 19 kolom yaitu sebagai berikut:  
- `user_id` : id dari pengguna
- `location` : lokasi/alamat pengguna
- `age` : umur pengguna
- `isbn` : kode ISBN (International Standard Book Number) buku
- `rating` : rating dari buku
- `book_title` : judul buku
- `book_author` : penulis buku
- `year_of_publication` : tahun terbit buku
- `publisher` : penerbit buku
- `img_s` : gambar sampul buku (ukuran kecil)
- `img_m` : gambar sampul buku (ukuran sedang)
- `img_l` : gambar sampul buku (ukuran besar)
- `Summary` : ringkasan/sinopsis buku
- `Language` : bahasa yang digunakan buku
- `Category` : kategori buku
- `city` : kota pengguna
- `state` : negara bagian penguna
- `country` : negara pengguna
***

### Sample Data

| Unnamed: 0 | user_id | location | age | isbn | rating | book_title | book_author | year_of_publication | publisher | img_s | img_m | img_l | summary | language | category | city | state | country |  
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | 
| 0 | 0 | 2 | stockton, california, usa | 18 | 0195153448 | 0 | Classical Mythology | 2002 | Oxford University Press | http://images.amazon.com/images/P/0195153448.0... | http://images.amazon.com/images/P/0195153448.0... | http://images.amazon.com/images/P/0195153448.0...  | Provides an introduction to classical myths pl... | en | ['Social Science'] | stockton | california | usa  


Tabel 3. informasi singkat mengenai data  

| #  | Column       		| Non-Null Count | Dtype  |
| -- | -------------------- | -------------- | ------ |
| 0  | Unnamed: 0  			| 1031175  		 | int64  |
| 1  | user_id      		| 1031175  		 | int64  |
| 2  | location  			| 1031175  		 | object |
| 3  | age  				| 1031175  		 | float64|
| 4  | isbn  				| 1031175  		 | object |
| 5  | rating  				| 1031175  		 | int64  |
| 6  | book_title   		| 1031175  		 | object |
| 7  | book_author 			| 1031175  		 | object |
| 8  | year_of_publication  | 1031175  		 | float64|
| 9  | publisher 			|  1031175 		 | object |
| 10 | img_s				| 1031175  		 | object |
| 11 | img_m				| 1031175  		 | object |
| 12 | img_l				| 1031175  		 | object |
| 13 | Summary				| 1031175  		 | object |
| 14 | Language				| 1031175  		 | object |
| 15 | Category				| 1031175  		 | object |
| 16 | city					| 1017072  		 | object |
| 17 | state				| 1008377  		 | object |
| 18 | country 				| 995801   		 | object |

Tabel 4. Distribusi variabel rating

| rating | count |
|--------|-------|
|0       |647323 |
|1       |1481   |
|2       |2375   |
|3       |5118   |
|4       |7617   |
|5       |45355  |
|6       |31689  |
|7       |66404  |
|8       |91806  |
|9       |60780  |
|10      |71227  |

Dari tabel 2 dan 3, dapat dilihat ada beberapa kolom yang tidak akan digunakan dan akan lebih baik jika di hapus. Dari tabel 4 dapat dilihat bahwa 0 ada rating artinya pengguna pernah membaca buku, tetapi tidak memberikan rating, sehingga akan lebih baik jika rating 0 di hapus, menyisakan 1 s.d. 10.


### Univariate Exploratory Data Analysis
Selanjutnya adalah menampilkan 10 data teratas dan terbawah menurut jumlah kemunculan data pada fitur `Category` yang dapat dilihat pada Gambar 1.

![top_10_category](https://github.com/user-attachments/assets/4cfd070d-80ce-4b65-8fb2-5bb74fad08d6)

 *10 data category teratas*

![top_10_category_2](https://github.com/user-attachments/assets/360f34d9-5338-4cc8-9eda-fe9e53395e6d)

*10 data category terbawah*


#### Distribusi Rating
Grafik distribusi rating menunjukkan sebagian besar pengguna memberikan rating antara 7-10.

#### Kategori Buku Populer
Visualisasi kategori buku menunjukkan bahwa kategori *Fiction* mendominasi dataset, diikuti *Juvenile Fiction* dan *Science*.

#### Distribusi Usia Pengguna
Sebagian besar pengguna berada di rentang usia 20-35 tahun, menunjukkan audiens utama untuk rekomendasi ini.

## Data Preprocessing
1. Mengecek ukuran dari dataset yang digunakan pada proyek ini, antara lain:

*Tabel 6. Ukuran dataset*

| Keterangan    |     Jumlah    |
|---------------|---------------|
| shape         | (1031175, 19) |

2. Mengidentifikasi nilai-nilai non-string dan mengambil tindakan yang sesuai untuk membersihkannya, seperti yang ditemukan pada fitur `Category` di mana terdapat nilai-nilai non-string dari data tersebut seperti '[', ']', dan 'petik'. Maka dari itu perlunya untuk dihilangkan supaya data dapat lebih siap digunakan.

*Tabel 7. Kondisi data pada proses 2*

| Sebelum    |     Sesudah    |
|---------------|---------------|
| ['Actresses'], ['Social Science'] | Actresses, Social Science |

3. Mengidentifikasi nilai yang bukan huruf pada fitur `Category` dan melakukan tindakan yang sesuai. Karena sebelumnya terdeteksi ada beberapa data yang bernilai bukan huruf, sedangkan pada umumnya fitur `Category` menyimpan data berupa huruf maka akan dilakukan filter untuk menghapus baris data yang memiliki data selain huruf kecuali jika memiliki nilai '&' atau ','.

*Tabel 8. Kondisi data pada proses 3*

| Sebelum    |     Sesudah    |
|---------------|---------------|
| Social Science; Actresses; Body, Mind & Spirit; 9; 1940-1949 | Social Science; Actresses; Body, Mind & Spirit; |

Setelah melakukan beberapa tahapan di atas, selanjutnya adalah mengecek ukuran dari data setelah pre-processing yang disimpan pada variabel **data_cleaned** antara lain:

*Tabel 9. Ukuran dataframe 'data_cleaned' setelah Pre-processing*

| Keterangan    |     Jumlah    |
|---------------|---------------|
| shape         | (607758, 19)  |


## Data Preparation

***
### Langkah-langkah pra-pemrosesan data
1. Membaca _dataset_ menggunakan _pandas_
2. _Drop_ data kosong (_NaN_)
3. _Drop_ kolom yang tidak akan digunakan
4. _Drop_ nilai yang _invalid_ pada kolom
5. Pemilihan _Category_
#### Membaca _dataset_
Pada bagian ini akan digunakan _library pandas_ untuk dapat membaca dan merubah _dataset_ menjadi _DataFrame_,  dari berkas yang diunduh akan ada 2 _file_, diproyek ini digunakan file dengan nama _Books Data with Category Language and Summary_ yang didalam file akan ditemukan berkas csv yang datanya sudah di proses terlebih dahulu. _Sample dari _dataset_ ini dapat dilihat pada tabel 2.

#### Drop data kosong
Pada bagian ini kita dapat melihat tabel 3 bahwa kolom `city, state, dan country` jumlahnya tidak sama dengan kolom lainnya. Untuk proyek ini, akan digunakan fungsi `dropna()`, dengan fungsi ini jika ada data kosong dalam bagian baris _DataFrame_ maka seluruh baris akan dihapus. Untuk melihat _count_ dari tiap kolom setelah dihapus dapat dilihat di tabel 5. 

Tabel 5. Informasi tentang data setelah _preprocess_  

| #  | Column               | Non-Null Count | Dtype  |
| -- | -------------------- | -------------- | ------ |
| 0  | user_id              | 217314         | int64  |
| 1  | rating               | 217314         | int64  |
| 2  | book_title           | 217314         | object |
| 3  | book_author          | 217314         | object |
| 4  | publisher            | 217314         | object |
| 5  | Category             | 217314         | object |

#### Drop kolom/nilai 
Pada bagian ini akan di hapus kolom yang tidak akan digunakan, tujuan penghapusan ini adalah untuk mengurangi dimensi yang dibutuhkan, berikut adalah kolom yang dihapus `'Unnamed: 0','location','isbn', 'img_s','img_m', 'img_l', 'city','age','state','Language','country', 'year_of_publication', 'Summary'`. Selain kolom akan dihapus nilai yang tidak sesuai dengan konteks seperti pada kolom Category `'9'` dan 0 pada rating. Hasil akhir dapat dilihat pada tabel 5.

### Pemilihan _Category_
Pada bagian ini akan dipilih dari _category_ secara spesifik, pemilihan ini dilakukan dikarenakan sumber daya yang dimiliki untuk menghitung tidak memadai untuk menggunakan seluruh _category_. _Category_ yang akan dipakai adalah `'Religion', 'Body Mind Spirit', 'Juvenile Nonfiction', 'Social Science', 'Business Economics', 'Family Relationships', 'Self Help', 'Health Fitness', 'Cooking', 'Travel', 'Poetry', 'True Crime', 'Psychology', 'Science', 'Computers'`.

1. Dikarenakan terlalu banyak baris dan data yang berbeda pada fitur 'Category', maka pada studi kasus kali ini akan menggunakan 100 data category dengan jumlah data teratas saja, serta hanya mengambil 15 judul dengan index teratas untuk setiap 'Category'-nya.

*Tabel 10. Ukuran dataset dengan 100 data unik Category*

| Keterangan    |     Jumlah    |
|---------------|---------------|
| shape         |  (23555, 19)  |

2. Memasukkan dataframe 'data_cleaned' ke dalam variabel **data_books**, dengan kondisi memasukkan beberapa fitur yang penting saja seperti `user_id`, `isbn`, `rating`, `book_title`, `book_author`, `year_of_publication`, `publisher`, `Summary`, dan `Category` serta melakukan perubahan gaya pada header yang diganti menjadi *lowercase* dan untuk datanya diganti menjadi *proper_case*.

*Tabel 11. Kondisi dataframe dan sample data setelah proses perubahan gaya penulisan*

| Nama fitur             | Deskripsi               |
|------------------------|-------------------------|
| user_id                | 11676                   |
| isbn                   | 0399135782              |
| rating                 | 9                       |
| book_title             | The Kitchen God'S Wife  |
| book_author            | Amy Tan	               |
| year_of_publication    | 1991                    |
| publisher              | Putnam Pub Group        |
| summary                | A Chinese Immigrant Who Is Convinced She Is Dy... |
| category               | Fiction                 |

### Data Preparation: Content Based Filtering
1. Memasukkan dataframe data_books ke dalam variabel data_cbf dengan melakukan drop pada fitur `user_id`.

2. Mencari rata-rata rating dari setiap judul buku dan menghilangkan data duplikat pada fitur `book_title` dan `isbn`, supaya hanya ada 1 judul buku dengan rata-rata dari nilai rating yang diberikan dari banyaknya user.

Sehingga dataframe untuk **Modelling Content Based Filtering** memiliki panjang atau ukuran data sebesar yang tertera pada Tabel 12.

*Tabel 12. Ukuran dataframe Content Based Filtering*

| Keterangan    |     Jumlah    |
|---------------|---------------|
| shape         |   (1448, 8)   |

### Data Preparation: Collaborative Filtering
1. Membuat dataframe dengan nama `data_rating` yang menyimpan fitur 'user_id', 'isbn', dan 'rating' dari setiap user terhadap isbn suatu buku.

2. Mengubah user_id dan isbn menjadi list tanpa nilai yang sama, serta melakukan proses encoding

    ```
    user_to_user_encoded = {x: i for i, x in enumerate(user_ids)}
    user_encoded_to_user = {i: x for i, x in enumerate(user_ids)}
    ```

3. Melakukan pemetaan user_id dan isbn ke dataframe yang berkaitan.

4. Membuat variabel x untuk mencocokkan data user dan isbn menjadi satu value.

5. Membuat variabel y untuk membuat rating dari hasil

    ```
    y = data_cll['rating'].apply(lambda x: (x - min_rating) / (max_rating - min_rating)).values
    ```

6. Melakukan Splitting dataset
    Dataset akan dibagi menjadi beberapa beberapa folder yang memiliki kegunaan yang berbeda-beda yaitu data pelatihan dan data validasi. Dataset akan dibagi menjadi 80% data train dan 20% data validasi.
### Kesimpulan

Berdasarkan tahapan **Data Preprocessing** dan **Data Preparation** yang dilakukan untuk membangun sistem rekomendasi berbasis **Content-Based Filtering** dan **Collaborative Filtering**, berikut kesimpulan yang dapat diambil:

#### **Data Preprocessing**
1. **Pembersihan Data**  
   - Dataset awal yang memiliki lebih dari satu juta baris telah melalui proses pembersihan untuk memastikan kualitas data yang optimal.  
   - Proses ini melibatkan penghapusan nilai non-string dan simbol yang tidak diperlukan pada fitur `Category` agar fitur tersebut konsisten dan sesuai untuk analisis.  
   - Nilai kategori yang bukan berupa huruf juga telah difilter, dengan pengecualian simbol '&' dan ',' untuk memastikan data tetap bermakna.  

2. **Efek pada Ukuran Dataset**  
   - Setelah pre-processing, jumlah data berkurang signifikan menjadi **607,758 baris**, menunjukkan efisiensi proses pembersihan dan penghapusan data yang tidak relevan.  

#### **Data Preparation**
1. **Penyederhanaan Dataset**  
   - Dari dataset yang sudah dibersihkan, hanya 100 kategori teratas berdasarkan jumlah data yang dipilih untuk meningkatkan efisiensi proses dan fokus pada kategori yang dominan.  
   - Setiap kategori diambil 15 judul teratas berdasarkan jumlah data, menghasilkan dataset akhir dengan **23,555 baris**.

2. **Penyesuaian Format Data**  
   - Dataset `data_books` hanya menyimpan fitur penting seperti `user_id`, `isbn`, `rating`, `book_title`, dan lainnya.  
   - Header diubah menjadi lowercase dan data ditulis dalam proper case untuk memastikan konsistensi dan keterbacaan.

3. **Data Preparation untuk Modelling**  
   - Untuk **Content-Based Filtering**, dataset disesuaikan dengan rata-rata rating setiap buku dan penghapusan duplikat pada `book_title` dan `isbn`, menghasilkan ukuran akhir **1,448 baris**.
   - Untuk **Collaborative Filtering**, fitur `user_id`, `isbn`, dan `rating` digunakan untuk membuat model interaksi pengguna, di mana data di-split menjadi **80% data pelatihan** dan **20% data validasi**.

### Langkah Preprocessing
1. Menghapus kolom tidak relevan seperti `Unnamed: 0` dan `img_*`.
2. Membersihkan nilai kategori yang tidak valid.
3. Menghapus rating 0 untuk meningkatkan akurasi analisis.

### Content-Based Filtering
1. Membuat representasi TF-IDF dari kategori buku.
2. Menghitung kesamaan antar buku menggunakan cosine similarity.

### Collaborative Filtering
1. Encoding data `user_id` dan `isbn`.
2. Membagi data menjadi 80% data pelatihan dan 20% validasi.

---
## Modelling
Sama seperti hal nya yang telah dilakukan pada proses **Data Preparation**, proses **Modelling** akan dilakukan menggunakan 2 metode yaitu Content Based Filtering dan Collaborative Filtering.

### Modelling: Content Based Filtering
1. Melakukan perhitungan bobot atau IDF pada data di fitur `category`, sekaligus melakukan mapping array dari fitur index integer ke fitur nama

2. Melakukan fit transform pada data `category` dan ditransformasikan ke bentuk matrik

    ```
    tfidf_matrix = tf.fit_transform(data_cbf.category)
    ```

3. Mengubah vektor tf-idf dalam bentuk matriks yang berguna untuk mengoptimalkan pencarian agar lebih cepat dan efisien dalam dokumen berdasarkan relevansi dengan kueri yang diberikan.

    ```
    tfidf_matrix.todense()
    ```

4. Mengidentifikasi korelasi antara antara judul buku dengan kategorinya

    ```
    from sklearn.metrics.pairwise import cosine_similarity
    cosine_sim = cosine_similarity(tfidf_matrix)
    ```

5. Membangun fungsi dengan nama `book_recommendations`, di mana memiliki beberapa parameter yaitu `book_title`, `k`, `similarity_data`, dan `items`.

*Tabel 13. parameter pada 'book_recommendations'*

| Nama parameter    | Value            | Keterangan |
|-------------------|------------------|------------|
| book_title        | input user       | input user berupa judul buku |
| k                 | input user       | input user berupa jumlah buku yang ingin direkomendasikan
| similarity_data   | data yang digunakan untuk menghitung kesamaan antara buku-buku | 
| items             | ['book_title', 'summary', 'book_author', 'rating', 'category']  | Dataframe yang akan ditampilkan kepada user |

Sebagai contoh user akan memasukkan input judul `Dave Barry In Cyberspace` dengan jumlah buku yang ingin direkomendasikan sebanyak `7`. Maka dapat dituliskan sebagai berikut:

```
book_recommendations('Dave Barry In Cyberspace', 7)
```

Dengan demikian sistem akan menampilkan data yang dapat dilihat pada Gambar 3, di mana akan ditampilkan 7 judul buku yang memiliki kemiripan dengan 'Dave Barry In Cyberspace' dan diurutkan berdasarkan rating tertinggi yang diberikan oleh pengguna-pengguna lain.

*Tabel 14. Hasil rekomendasi buku yang tampil dengan Content Based Filtering*

| book_title                                         | summary                                               | book_author               | rating | category       |
|----------------------------------------------------|-------------------------------------------------------|---------------------------|--------|----------------|
| Miles Of Smiles                                    | Humorous Poems Divided Into Catagories Such As...    | Bruce Lansky              | 8.5    | American Poetry|
| Jim Morrison: Lords And New Creatures              | Jim Morrison Was One Of The Most Erudite And W...    | James Morrison            | 7.0    | American Poetry|
| Sing A Song Of Popcorn: Every Child'S Book Of ... | A Collection Of 128 Poems By A Variety Of Well...    | Beatrice Schenk De Regniers| 8.0    | American Poetry|
| The Collected Poems Of Weldon Kees                 | Of The Three Volumes Of Poetry Published By We...    | Donald Justice            | 6.0    | American Poetry|
| Walt Whitman: The Complete Poems (Penguin Clas... | A Collection Of Many Of Whitman's Works.             | Francis Murphy            | 3.3    | American Poetry|
| Robert Frost (The Great American Poets)            | From The Great Poets Series--Exquisite Small-F...    | Peter Porter              | 6.7    | American Poetry|
| Its Thanksgiving                                   | From The First Thanksgiving Feast To Daddys Fo...    | Jack Prelutsky            | 4.0    | American Poetry|

### Kesimpulan

Berdasarkan penerapan model **Content-Based Filtering** untuk merekomendasikan buku, berikut kesimpulan yang dapat diambil:

1. **Pemanfaatan Fitur Kategori**  
   Model memanfaatkan fitur **kategori buku** untuk menghitung kemiripan antar buku dengan pendekatan **TF-IDF (Term Frequency-Inverse Document Frequency)**.  
   - Teknik ini mengukur pentingnya suatu kategori dalam setiap buku, sehingga menghasilkan representasi fitur yang optimal untuk menentukan relevansi.  
   - Matriks TF-IDF kemudian digunakan untuk menghitung kesamaan antar buku menggunakan metrik **cosine similarity**, yang memastikan kemiripan dihitung secara efisien dalam ruang multidimensi.

2. **Proses Rekomendasi**  
   Sistem dirancang untuk menerima input berupa judul buku, seperti *"Dave Barry In Cyberspace"*, dan jumlah rekomendasi (*k*) yang diinginkan oleh pengguna.  
   - Dengan fungsi `book_recommendations`, sistem mencari buku dengan kategori yang serupa dan menampilkan daftar rekomendasi berdasarkan **rating tertinggi** dari pengguna lain.  
   - Output tidak hanya mencakup judul buku, tetapi juga informasi tambahan seperti ringkasan, penulis, rating, dan kategori.

3. **Hasil Rekomendasi**  
   Rekomendasi yang dihasilkan menunjukkan relevansi kategori buku yang tinggi dengan buku input, yaitu *American Poetry*.  
   - Buku seperti *"Miles Of Smiles"* dan *"Sing A Song Of Popcorn"* memiliki rating tinggi, menunjukkan kualitas rekomendasi yang baik.  
   - Namun, sistem juga mencantumkan buku dengan rating lebih rendah seperti *"Walt Whitman: The Complete Poems"*, yang menunjukkan model tidak hanya mengandalkan rating tetapi juga mempertimbangkan kesamaan kategori.

4. **Kekuatan Model**  
   - **Personalization**: Sistem sangat personal karena hanya memanfaatkan fitur buku (konten) tanpa memerlukan data dari pengguna lain, sehingga cocok untuk pengguna baru dengan preferensi spesifik.  
   - **Kemudahan Implementasi**: Pendekatan TF-IDF dan cosine similarity mudah diterapkan dan memproses data dengan efisien.  

5. **Keterbatasan Model**  
   - **Cold Start Item**: Model bergantung pada deskripsi kategori buku. Jika kategori tidak terdefinisi dengan baik, kualitas rekomendasi dapat menurun.  
   - **Lack of Diversity**: Rekomendasi cenderung terbatas pada kategori serupa, sehingga dapat kurang bervariasi bagi pengguna dengan minat yang luas.

### Rekomendasi  
1. **Integrasi Metadata Tambahan**  
   Selain kategori, model dapat ditingkatkan dengan memanfaatkan metadata lain, seperti popularitas buku atau ulasan pengguna, untuk memberikan rekomendasi yang lebih kaya.  
2. **Hybrid Approach**  
   Menggabungkan pendekatan **Content-Based Filtering** dengan **Collaborative Filtering** untuk meningkatkan keberagaman rekomendasi sekaligus mempertahankan personalisasi yang tinggi.  
3. **Peningkatan Visualisasi**  
   Memberikan antarmuka yang menampilkan rekomendasi dengan lebih menarik, seperti menambahkan sampul buku atau rating visual untuk meningkatkan pengalaman pengguna.  

Secara keseluruhan, model **Content-Based Filtering** yang diterapkan memiliki performa baik dalam merekomendasikan buku dengan kategori relevan dan menghasilkan pengalaman personal bagi pengguna.

### Modelling: Collaborative Filtering
1. Pembangunan Model

    Kelas RecommenderNet adalah sebuah model jaringan saraf tiruan (neural network) yang digunakan untuk merekomendasikan item kepada pengguna.

    * `num_users`: Jumlah pengguna dalam dataset.
    * `num_isbn_n`: Jumlah item (dalam konteks ini, mungkin jumlah buku dengan ISBN) dalam dataset.
    * `embedding_size`: Ukuran embedding yang digunakan untuk merepresentasikan pengguna dan item dalam ruang laten. Ini adalah ukuran dimensi yang digunakan untuk menyandikan pengguna dan item sebagai vektor fitur.
    * `**kwargs`: Parameter tambahan yang dapat diberikan ke konstruktor kelas. Ini adalah konvensi dalam Python untuk menerima argumen yang tidak ditentukan sebelumnya dalam bentuk kata kunci.

    Selanjutnya, dalam metode `__init__`, layer-layer embedding digunakan untuk menyandikan pengguna dan item ke dalam vektor representasi. Setiap layer embedding memiliki inisialisasi vektor berukuran `embedding_size` dan menerapkan regularisasi L2 pada vektor embedding untuk mencegah overfitting.

    Dalam metode `call`, model mengambil input berupa pasangan pengguna dan item. Kemudian, ia mengambil vektor embedding untuk pengguna dan item yang sesuai. Dot product (produk titik) antara vektor pengguna dan vektor item digunakan untuk memperkirakan rating yang diberikan pengguna pada item tertentu. Dengan menambahkan bias dari pengguna dan item, serta dot product tersebut, model menghasilkan output yang merupakan prediksi rating yang telah dinormalisasi menggunakan fungsi aktivasi sigmoid untuk memastikan nilai berada dalam rentang [0, 1].

2. Compile Model

    ```
    model.compile(
        loss=BinaryCrossentropy(),
        optimizer=Adam(learning_rate=0.001),
        metrics=[
            MeanSquaredError(), Precision(), Recall()
        ]
    )
    ```

    Keterangan:
    * loss: Fungsi kerugian (loss function) yang digunakan selama pelatihan. Dalam kasus ini, digunakan Binary Crossentropy. Fungsi ini umumnya digunakan untuk tugas klasifikasi biner, di mana model mencoba memprediksi probabilitas label biner.
    * Optimizer: Algoritma optimasi yang digunakan untuk menyesuaikan bobot model selama pelatihan guna meminimalkan fungsi kerugian. Dalam kode ini, digunakan Adam optimizer. Adam adalah algoritma optimasi yang populer dan efisien dalam menyesuaikan learning rate secara adaptif selama pelatihan. Learning rate yang digunakan adalah 0.001.
    * Metrics: Daftar metrik evaluasi yang digunakan untuk mengevaluasi kinerja model selama dan setelah pelatihan. Dalam kode ini, digunakan tiga metrik:
        * MeanSquaredError: Metrik untuk mengukur rata-rata dari kuadrat perbedaan antara nilai yang diprediksi oleh model dan nilai sebenarnya. Metrik ini biasanya digunakan dalam tugas regresi.
        * Precision: Metrik untuk mengukur seberapa banyak dari label positif yang diprediksi oleh model adalah benar. Hal ini berguna dalam tugas klasifikasi ketika perlu untuk memprioritaskan jumlah positif yang diprediksi dengan benar.
        * Recall: Metrik untuk mengukur seberapa banyak dari keseluruhan jumlah label positif yang berhasil ditemukan oleh model. Metrik ini berguna dalam tugas klasifikasi, terutama ketika fokus pada mengidentifikasi sebanyak mungkin label positif yang ada.

3. Training Model

    ```
    history = model.fit(
        x = x_train,
        y = y_train,
        epochs = 20,
        validation_data = (x_val, y_val),
    )
    ```
    Menggunakan jumlah epochs atau iterasi sebanyak 20 kali, menggunakan data x_train dan y_train untuk proses training dan x_val dan y_val untuk data validasi. 

Berikut menunjukkan buku yang telah di rating tinggi oleh user lain dan memberikan 10 rekomendasi buku berdasarkan preferensi pengguna dengan user_id = 233579.

*Tabel 15. Hasil rekomendasi buku yang tampil dengan Collaborative Filtering*

| Showing recommendations for users |
| --- |
| 233579 |

| Book with high ratings from user |
|---|
| Wild Animus : Fiction |

| Top 10 Book Recommendations  |
|---|

| No | Book Title | Category Book |
| -- | ---- | ---- |
| 1 | The Little Prince            | Juvenile Fiction       |
| 2 | Falling Up                   | Juvenile Nonfiction    |
| 3 | Child Is Born, A             | Family & Relationships |
| 4 | Westward The Tide            | Fiction                | 
| 5 | La Sonrisa Etrusca           | Drama                  |
| 6 | The Control Of Nature        | Nature                 |
| 7 | El Principito                | Fantasy                |
| 8 | The Secret Life Of Bees      | African American Women |
| 9 | The Last Day Of Summer       | Photography            |
| 10 | Native Son                  | African American Men   |

### Kesimpulan

Berdasarkan penerapan model **Collaborative Filtering** menggunakan arsitektur neural network, berikut adalah kesimpulan yang dapat diambil:

1. **Pembangunan Model**  
   Model berbasis embedding telah dirancang untuk memprediksi rating buku oleh pengguna dengan memanfaatkan representasi laten dari pengguna dan buku.  
   - **Vektor embedding** memungkinkan model untuk memahami hubungan laten antara pengguna dan buku.  
   - Penggunaan fungsi aktivasi sigmoid memastikan output prediksi berada pada rentang [0,1], memungkinkan normalisasi prediksi.

2. **Evaluasi Model**  
   Model dikompilasi dengan fungsi loss **Binary Crossentropy** untuk meminimalkan kesalahan prediksi dan menggunakan optimizer **Adam** dengan learning rate 0.001 untuk pembelajaran yang efisien.  
   - Metrik evaluasi seperti **Mean Squared Error (MSE)**, **Precision**, dan **Recall** menunjukkan performa model dalam menghasilkan prediksi yang akurat dan relevan.
   - Tren precision dan recall yang baik menunjukkan model mampu meminimalkan hasil prediksi palsu dan mengenali hubungan relevan antara pengguna dan buku.

3. **Training Model**  
   Pelatihan model dilakukan selama 20 epoch dengan data training dan validasi yang disediakan.  
   - Data validasi menunjukkan performa yang stabil, mencerminkan bahwa model tidak overfitting dan memiliki generalisasi yang baik.

4. **Rekomendasi Buku**  
   Berdasarkan preferensi pengguna tertentu (contohnya pengguna dengan ID `233579`), model mampu memberikan rekomendasi buku yang relevan dan berkualitas tinggi:  
   - Buku seperti *"The Little Prince"* dan *"Falling Up"* yang masuk dalam kategori *Juvenile Fiction* dan *Juvenile Nonfiction* menunjukkan bahwa model berhasil menangkap minat pengguna dalam buku fiksi untuk pembaca muda.  
   - Rekomendasi buku mencakup kategori yang beragam, seperti *Drama*, *Fantasy*, hingga *Photography*, yang mencerminkan kekayaan data yang dimanfaatkan oleh model untuk menghasilkan rekomendasi yang beragam.

5. **Keseluruhan Performa**  
   Model **Collaborative Filtering** yang dirancang berhasil memberikan rekomendasi yang personal dan akurat berdasarkan preferensi pengguna, seperti yang terlihat dari hasil rekomendasi untuk pengguna tertentu.  
   - Model menunjukkan generalisasi yang baik, menjadikannya alat yang efektif untuk sistem rekomendasi buku di masa mendatang.  
   - Berbagai kategori yang direkomendasikan juga menunjukkan bahwa model mampu menangkap dan mengintegrasikan variasi minat pengguna secara baik.
   - 
### Content-Based Filtering
1. **Pendekatan:** Menggunakan kategori buku untuk menentukan kemiripan antar buku.
2. **Output:** Rekomendasi berdasarkan kategori dan rating tertinggi.

**Contoh Output:**
| Book Title                 | Summary               | Rating |
|----------------------------|-----------------------|--------|
| The Little Prince          | Classic for children | 9.1    |
| Falling Up                 | Poetry for kids      | 8.8    |

### Collaborative Filtering
1. **Pendekatan:** Menggunakan neural network dengan embedding.
2. **Evaluasi:** 
   - Precision: 0.91 (train), 0.66 (validation)
   - Recall: 0.40 (validation)
   - MSE: 0.097 (di bawah batas 0.15).

**Contoh Output Rekomendasi:**
| No | Book Title           | Category            |
|----|----------------------|---------------------|
| 1  | The Little Prince    | Juvenile Fiction    |
| 2  | Falling Up           | Juvenile Nonfiction |
| 3  | Child Is Born, A     | Family Relationships|

---

## Evaluation
### Metrik Evaluasi
 ![Metrik Evaluasi](https://github.com/user-attachments/assets/c7f48575-e34a-4d35-9e05-6e05285ecc13).

### Insight Evaluasi
1. **Precision Tinggi:** Menunjukkan sistem menghasilkan rekomendasi yang relevan.
2. **Recall Rendah:** Masih ada buku relevan yang terlewat.

---
1. Mean Squared Error (MSE)
    MSE adalah singkatan dari "Mean Squared Error" atau "Rata-rata Kesalahan Kuadrat". Ini adalah salah satu metrik evaluasi yang umum digunakan dalam statistik, ilmu data, dan machine learning untuk mengukur seberapa baik model memprediksi nilai target pada data yang diberikan. MSE mengukur rata-rata dari kuadrat perbedaan antara nilai aktual dan nilai yang diprediksi oleh model. Dengan demikian, semakin rendah nilai MSE, semakin baik model dalam memprediksi nilai target.

    ![visuliasasi-mse](https://github.com/user-attachments/assets/cf93287f-41f8-4897-bdc0-ad6bf36e6b82)

    Hasil Mean Squared Error*

    Tren MSE pada data train dan val menurun seiring dengan waktu, namun mereka tetap berada pada tingkat yang relatif rendah. Hal ini menunjukkan bahwa model mampu mengurangi kesalahan baik pada data train maupun val, yang merupakan indikasi baik.

2. Precision
    Presisi mengukur seberapa banyak dari prediksi positif yang sebenarnya benar. Ini memberikan pemahaman tentang seberapa baik model dalam menghindari memberikan hasil positif palsu. Presisi dihitung dengan membagi jumlah prediksi positif yang benar dengan total prediksi positif yang dilakukan.


    ![precision](https://github.com/user-attachments/assets/a6f57fdd-985f-42dd-9e7b-7fdc2afa1da0)

    *Hasil Precision*

    Gambar diatas menunjukkan visualisasi hasil dari metrik precision pada data train dan data validation. Dari visualisasi tersebut, terlihat bahwa precision pada data train cenderung meningkat seiring waktu, yang menunjukkan bahwa model memiliki performa yang semakin baik dalam mengidentifikasi hasil positif yang benar pada data train seiring dengan proses pelatihan. Namun, pada data validation, precision terlihat lebih fluktuatif, yang dapat disebabkan oleh berbagai faktor seperti perubahan dalam distribusi data atau kompleksitas model. Meskipun fluktuatif, secara keseluruhan, precision pada kedua data relatif tinggi, yang menunjukkan bahwa model memiliki kemampuan yang baik untuk mengidentifikasi hasil positif yang benar, terlepas dari variasi dalam data validation.

    Dengan demikian, berdasarkan analisis tersebut, dapat disimpulkan bahwa model memiliki performa yang baik dalam menghasilkan prediksi positif yang benar, dan precision yang tinggi menunjukkan kemampuan yang baik dalam menghindari hasil false positive.

3. Recall
    Recall, juga dikenal sebagai sensitivitas, mengukur seberapa banyak dari kelas yang sebenarnya positif yang telah diidentifikasi dengan benar oleh model. Ini memberikan pemahaman tentang seberapa baik model dapat mengenali semua contoh yang positif.   

   ![recall](https://github.com/user-attachments/assets/6f675037-c856-4f89-8022-1507276b17f4)

    *. Hasil Recall*

    Gambar diatas menunjukkan visualisasi hasil dari metrik recall pada data train dan data validation. Dari visualisasi tersebut, terlihat bahwa recall pada data train cenderung meningkat seiring waktu, menunjukkan bahwa model mampu mengenali sebagian besar kasus positif yang sebenarnya ada pada data train seiring dengan proses pelatihan. Namun, pada data validation, recall terlihat lebih stabil, yang menunjukkan bahwa model memiliki performa yang konsisten dalam mengenali kasus positif pada data validation.
    
    Secara keseluruhan, recall pada kedua data juga relatif tinggi, menunjukkan bahwa model memiliki kemampuan yang baik dalam menangkap sebagian besar kasus positif yang sebenarnya ada. Hal ini menunjukkan bahwa model memiliki sensitivitas yang baik terhadap kasus positif.

### Kesimpulan

Berdasarkan evaluasi menggunakan tiga metrik utama, yaitu **Mean Squared Error (MSE)**, **Precision**, dan **Recall**, dapat disimpulkan bahwa model memiliki performa yang baik secara keseluruhan dalam menangani data train maupun validation. Berikut adalah poin-poin utama dari kesimpulan ini:

1. **Mean Squared Error (MSE)**  
   Tren MSE yang menurun pada data train dan validation menunjukkan bahwa model mampu mengurangi kesalahan prediksi seiring waktu. Nilai MSE yang relatif rendah menunjukkan bahwa model berhasil memprediksi nilai target dengan tingkat kesalahan yang kecil, mencerminkan kualitas model yang baik.

2. **Precision**  
   Precision yang meningkat pada data train menunjukkan bahwa model semakin baik dalam menghindari prediksi positif palsu selama pelatihan. Meskipun terdapat sedikit fluktuasi pada data validation, precision tetap berada pada tingkat yang relatif tinggi, yang menunjukkan kemampuan model dalam memberikan hasil positif yang benar secara konsisten.

3. **Recall**  
   Recall yang tinggi pada data train dan validation menunjukkan bahwa model memiliki sensitivitas yang baik terhadap kelas positif. Model mampu mengenali sebagian besar kasus positif yang sebenarnya ada pada kedua data, yang mencerminkan konsistensi performa model.

4. **Stabilitas dan Tren Performa**  
   Tidak ada indikasi overfitting, karena performa model pada data train dan validation tidak menunjukkan perbedaan yang signifikan. Sebaliknya, tren positif yang stabil menunjukkan bahwa model memiliki kemampuan generalisasi yang baik tanpa kehilangan performa pada data yang belum pernah dilihat.

Secara keseluruhan, model ini dapat dikategorikan sebagai **good fit**, karena memiliki performa yang stabil, akurat, dan mampu menjaga keseimbangan antara train dan validation. Model dapat digunakan dengan percaya diri untuk tugas prediksi pada domain terkait, dengan potensi optimasi lebih lanjut jika diperlukan.


## Conclusion
Setelah melalui proses pelatihan model dan evaluasi, dapat disimpulkan bahwa sistem rekomendasi buku yang dikembangkan mampu memberikan rekomendasi yang relevan kepada pengguna. Model menunjukkan performa yang stabil dengan penurunan mean squared error (MSE) secara konsisten dari 0.181 pada awal pelatihan hingga 0.097 pada akhir pelatihan, yang berada di bawah batas toleransi yang ditetapkan (< 0.15).

Pencapaian lain yang signifikan adalah nilai precision sebesar 0.91 pada data latih dan 0.66 pada data validasi. Hal ini menunjukkan bahwa model mampu memberikan rekomendasi yang relevan, meskipun masih ada ruang untuk peningkatan pada generalisasi di data baru. Di sisi lain, nilai recall yang mencapai 0.40 pada data validasi menunjukkan bahwa model cukup inklusif dalam menangkap berbagai rekomendasi yang relevan.

Secara keseluruhan, model yang dibangun menunjukkan potensi yang baik dalam memberikan rekomendasi. Namun, untuk meningkatkan akurasi dan cakupan, beberapa langkah pengembangan di masa depan dapat dipertimbangkan, seperti tuning hyperparameter, augmentasi data, dan evaluasi dengan metrik tambahan seperti F1-score untuk memberikan gambaran performa yang lebih seimbang.

Proyek ini telah berhasil mencapai tujuannya dengan menghasilkan model rekomendasi yang andal serta memberikan landasan yang kuat untuk pengembangan lebih lanjut. Integrasi pendekatan tambahan, seperti hybrid filtering, berpotensi meningkatkan performa model secara keseluruhan dan memberikan rekomendasi yang lebih personal dan akurat kepada pengguna.



