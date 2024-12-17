# Batik Besurek Bengkulu Image Classification Project

Proyek ini bertujuan untuk mengklasifikasikan jenis motif batik Besurek Bengkulu berdasarkan dataset yang terdiri dari beberapa kategori motif.

## Dataset

Dataset yang digunakan terdiri dari kategori berikut:

0: Kaligrafi Arab
1: Kaligrafi Arab-Kembang Cengkeh-Kembang Cempaka
2: Kaligrafi-Burung Kuau
3: Kaligrafi-Kembang Melati
4: Kaligrafi-Relung Paku-Burung Punai
5: Pohon Hayat-Burung Kuau-Kaligrafi Arab
6: Rafflesia
7: Rembulan Kaligrafi Arab
Dataset ini merupakan bagian dari studi tentang klasifikasi motif batik Besurek Bengkulu.


## Steps to Use the Inference Code

1. **Install Docker**

    Open your terminal, Command Prompt, or PowerShell and run the following command to pull the TensorFlow Serving Docker image:
    ```sh
    docker pull tensorflow/serving
    ```

2. **Run the Docker Container**

    Execute the following command to start the Docker container:
    ```sh
    docker run -it -v YOUR_PATH\saved_model:/models -p 8501:8501 --entrypoint /bin/bash tensorflow/serving
    ```

3. **Start the TensorFlow Model Server**

    Inside the Docker container, run:
    ```sh
    tensorflow_model_server --rest_api_port=8501 --model_name=animal_faces_model --model_base_path=/models/animal_faces_model/
    ```

Replace `YOUR_PATH` with the actual path to your saved model.
