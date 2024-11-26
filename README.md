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

### Univariate Exploratory Data Analysis
Selanjutnya adalah menampilkan 10 data teratas dan terbawah menurut jumlah kemunculan data pada fitur `Category` yang dapat dilihat pada Gambar 1.

![top_10_category](https://github.com/user-attachments/assets/4cfd070d-80ce-4b65-8fb2-5bb74fad08d6)

 *10 data category teratas*

![top_10_category_2](https://github.com/user-attachments/assets/360f34d9-5338-4cc8-9eda-fe9e53395e6d)

*10 data category terbawah*


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


## Evaluation

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

    Dengan demikian, berdasarkan penjelasan di atas, dapat disimpulkan bahwa model memiliki performa yang baik dalam mengenali kasus positif yang sebenarnya ada, dan recall yang tinggi menunjukkan sensitivitas yang baik dari model terhadap kasus positif.

Berdasarkan analisis di atas, model tersebut cenderung merupakan **good fit**. Hal ini ditandai dengan performa yang baik dan stabil pada kedua data train dan val, serta tren yang menunjukkan peningkatan secara bertahap dari waktu ke waktu. Tidak terlihat gejala overfitting (perbedaan performa yang signifikan antara data train dan val), ataupun underfitting (performa yang rendah baik pada data train maupun val).


## Conclusion
Setelah melalui proses pelatihan model dan evaluasi, dapat disimpulkan bahwa sistem rekomendasi buku yang dikembangkan mampu memberikan rekomendasi yang relevan kepada pengguna. Model menunjukkan performa yang stabil dengan penurunan mean squared error (MSE) secara konsisten dari 0.181 pada awal pelatihan hingga 0.097 pada akhir pelatihan, yang berada di bawah batas toleransi yang ditetapkan (< 0.15).

Pencapaian lain yang signifikan adalah nilai precision sebesar 0.91 pada data latih dan 0.66 pada data validasi. Hal ini menunjukkan bahwa model mampu memberikan rekomendasi yang relevan, meskipun masih ada ruang untuk peningkatan pada generalisasi di data baru. Di sisi lain, nilai recall yang mencapai 0.40 pada data validasi menunjukkan bahwa model cukup inklusif dalam menangkap berbagai rekomendasi yang relevan.

Secara keseluruhan, model yang dibangun menunjukkan potensi yang baik dalam memberikan rekomendasi. Namun, untuk meningkatkan akurasi dan cakupan, beberapa langkah pengembangan di masa depan dapat dipertimbangkan, seperti tuning hyperparameter, augmentasi data, dan evaluasi dengan metrik tambahan seperti F1-score untuk memberikan gambaran performa yang lebih seimbang.

Proyek ini telah berhasil mencapai tujuannya dengan menghasilkan model rekomendasi yang andal serta memberikan landasan yang kuat untuk pengembangan lebih lanjut. Integrasi pendekatan tambahan, seperti hybrid filtering, berpotensi meningkatkan performa model secara keseluruhan dan memberikan rekomendasi yang lebih personal dan akurat kepada pengguna.



