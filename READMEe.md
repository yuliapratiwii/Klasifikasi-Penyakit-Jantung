# Submission 1: Machine Learning Pipeline - Spam SMS Detection
Nama: Yulia Pratiwi

Username dicoding: yuliapratiwi

| | Deskripsi |
| ----------- | ----------- |
| Dataset | [SMS Spam Collection (Text Classification)](https://www.kaggle.com/datasets/thedevastator/sms-spam-collection-a-more-diverse-dataset) |
| Masalah | Pesan spam menimbulkan tantangan yang signifikan dalam ranah komunikasi SMS dengan mengganggu aktivitas harian pengguna dan berpotensi menimbulkan risiko keamanan. Pesan-pesan yang tidak diinginkan ini sering kali mengacaukan kotak masuk pengguna, memaksa mereka menghabiskan waktu yang berharga untuk memilah-milah konten yang tidak relevan. Yang lebih mengkhawatirkan lagi, pesan spam sering kali menyertakan elemen berbahaya seperti tautan phishing atau lampiran berbahaya, yang dapat menyebabkan pembobolan data atau kerusakan sistem. Oleh karena itu, mengembangkan model deteksi spam SMS yang tangguh menjadi sangat penting untuk melindungi pengguna dari ancaman-ancaman ini, meningkatkan produktivitas, dan melindungi informasi pribadi.|
| Solusi machine learning | Pengembangan model klasifikasi untuk mendeteksi pesan spam sangat penting dalam membantu pengguna menyaring pesan masuk. Model ini akan memisahkan pesan spam dari pesan yang sah, sehingga pengguna tidak perlu menghabiskan waktu berlebihan untuk memilah pesan yang tidak diinginkan. Selain itu, model ini juga dapat melindungi pengguna dari potensi risiko keamanan, seperti phishing dan malware, dengan secara otomatis menandai pesan yang mencurigakan. Dengan demikian, model ini dapat meningkatkan efisiensi dan keamanan dalam mengelola pesan masuk. |
| Metode pengolahan | Pemrosesan data dilakukan pada Transform dengan menormalkan konversi huruf besar ke huruf kecil dan Trainer dengan menstandarkan 'lower_and_strip_punctuation' untuk menghapus tanda baca. Label juga dikonversi menjadi angka 0 (pesan ham) dan 1 (pesan spam). |
| Arsitektur model | Model ini terdiri dari beberapa lapisan yang berfungsi untuk memproses data teks menjadi klasifikasi spam atau bukan. Lapisan pertama adalah **input** yang menerima data teks. Kemudian, lapisan **TextVectorisation** mengubah teks menjadi bentuk numerik yang dapat dipahami oleh model. Selanjutnya, lapisan **Embedding** membuat representasi sekuensial dari data tersebut. **GlobalAveragePooling** digunakan untuk mereduksi dimensi sekuens menjadi lebih ringkas. Setelah itu, lapisan **Dense** memproses fitur yang telah diolah, dan akhirnya, lapisan **output** menghasilkan klasifikasi yang menentukan apakah pesan termasuk spam atau bukan. |
| Metrik evaluasi | Metrik yang digunakan dalam proyek ini mencakup beberapa ukuran penting untuk evaluasi model. **Area Under Curve (AUC)** digunakan untuk menghitung luas di bawah kurva **Receiver Operating Characteristic (ROC)**, yang mengukur kemampuan model dalam membedakan antara kelas. **False Positive** menghitung jumlah data negatif yang salah diklasifikasikan sebagai positif, sementara **False Negative** menghitung jumlah data positif yang salah diklasifikasikan sebagai negatif. **True Positive** menunjukkan jumlah klasifikasi yang benar untuk data positif, dan **True Negative** menunjukkan klasifikasi yang benar untuk data negatif. **Akurasi Biner** mengukur proporsi prediksi yang benar dari keseluruhan prediksi yang dibuat oleh model dalam masalah klasifikasi biner. |
| Performa model | Selama proses pelatihan, model mencapai nilai **val_binary_accuracy** sebesar 0.9735, menunjukkan akurasi yang sangat tinggi. Pada tahap evaluasi, performa model juga sangat baik, dengan **overall binary_accuracy** sebesar 0.97347, **AUC** 0.97428, **False Negative** 30, **False Positive**0, **True Negative** 984, dan **True Positive** 117. Berdasarkan hasil ini, dapat disimpulkan bahwa model telah bekerja dengan sangat efektif dan memiliki akurasi yang sangat tinggi dalam memprediksi pesan spam dan non-spam. |