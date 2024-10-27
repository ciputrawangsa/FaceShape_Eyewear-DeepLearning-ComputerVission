# Klasifikasi Bentuk Wajah dan Pemilihan Kacamata 🕶️ - ![Deep Learning](https://img.shields.io/badge/Deep%20Learning-FF6F20?style=for-the-badge&logo=TensorFlow&logoColor=white)

Repositori ini berisi proyek segmentasi bentuk wajah dan pemilihan kacamata menggunakan teknik Deep Learning dan Computer Vision. Proyek ini bertujuan untuk menganalisis bentuk wajah pengguna dan merekomendasikan model kacamata yang sesuai berdasarkan analisis tersebut. Repositori ini mencakup file Jupyter Notebook yang menjelaskan proses secara menyeluruh, mulai dari eksplorasi data hingga penerapan model deep learning.

## Daftar Isi 🗒️
1. [Link Terkait Project](#link-terkait-project-)
2. [Project Overview](#project-overview-)
3. [Latar Belakang Masalah](#latar-belakang-masalah-)
4. [Problem Statement](#problem-statement-)
5. [Metode yang Digunakan](#metode-yang-digunakan-)
6. [Hasil dan Rekomendasi](#hasil-dan-rekomendasi-)
7. [File yang Tersedia](#file-yang-tersedia-)
8. [Cara Menggunakan Project Ini](#cara-menggunakan-project-ini-)
9. [Dependencies](#dependencies-)
10. [Libraries](#libraries-)
11. [Author](#author-)

## Link Terkait Project ⛓️‍💥

- [Dataset](https://www.kaggle.com/datasets/niten19/face-shape-dataset)
- [Deployment](https://huggingface.co/spaces/Ciputra/Faceshape)

## Project Overview 📝

Dalam proyek ini, saya menggunakan teknik Deep Learning untuk menganalisis bentuk wajah pengguna dan merekomendasikan kacamata yang sesuai. Beberapa langkah utama yang dicakup dalam proyek ini adalah:

1. **Import Libraries dan Eksplorasi Data**:
    - Memuat dataset dan melakukan eksplorasi awal untuk memahami struktur dan karakteristik data.

2. **Preprocessing Data**:
    - Melakukan pembersihan dan persiapan data, termasuk penanganan gambar dan normalisasi.

3. **Training Base Model**:
    - Membangun dan melatih model deep learning untuk mengidentifikasi bentuk wajah.

4. **Evaluasi Base Model**:
    - Menggunakan metrik evaluasi untuk menilai kinerja model.

5. **Tuning Model**:
    - Membangun dan melatih model deep learning dengan beberapa hyperparameter tuning untuk mengidentifikasi bentuk wajah.

6. **Evaluasi Model yang Dituning**:
    - Menggunakan metrik evaluasi untuk menilai kinerja model.

7. **Menggunakan Model Transfer Learning**:
    - Membangun dan melatih model deep learning dengan transfer learning untuk mengidentifikasi bentuk wajah.

8. **Evaluasi Model Hasil Transfer Learning**:
    - Menggunakan metrik evaluasi untuk menilai kinerja model.

9. **Pengambilan Keputusan**:
    - Mengambil keputusan terhadap performa model.

## Latar Belakang Masalah 🧐

Pemilihan kacamata yang tepat sering kali menjadi tantangan bagi banyak orang karena kacamata tidak hanya mempengaruhi penglihatan, tetapi juga penampilan. Bentuk wajah yang berbeda membutuhkan jenis kacamata yang berbeda agar terlihat proporsional dan dapat menonjolkan fitur wajah. Namun, sebagian besar orang tidak memiliki pengetahuan yang cukup tentang kacamata yang cocok untuk bentuk wajah mereka, yang akhirnya dapat mengurangi kepercayaan diri. Sehingga diperlukan solusi untuk dapat membantu memilih kacamata sesuai dengan bentuk wajah untuk meningkatkan penampilan dan kepercayaan diri agar customer merasa puas dan bisa meningkatkan penjualan.

## Problem Statement √

**Specific:**
Membantu pelanggan memilih kacamata yang tepat berdasarkan bentuk wajah mereka. Sehingga bisa meningkatkan penampilan, kepercayaan diri, kepuasan pelanggan, dan penjualan toko.

**Measurable:** Keberhasilan akan diukur melalui akurasi minimal 80% dalam pengenalan bentuk wajah, peningkatan kepuasan pelanggan hingga 80% terhadap rekomendasi kacamata yang dapat diperoleh melalui survei atau ulasan setelah penggunaan layanan, dan peningkatan revenue sebesar 20%.

**Achievable:** Solusi ini dapat dicapai dengan mengembangkan model CNN yang terlatih menggunakan dataset bentuk wajah, dan menerapkannya ke sistem toko eyewear untuk memberikan rekomendasi kacamata yang sesuai dengan pelanggan.

**Relevant:** Pengembangan model computer vision berbasis CNN relevan karena bisa membantu pelanggan dalam memilih kacamata yang sesuai dengan bentuk wajah mereka, meningkatkan kepuasan pelanggan, dan secara langsung berdampak pada peningkatan penjualan bagi toko eyewear dengan memberikan pengalaman belanja yang lebih personal dan efisien.

**Time-Bond:** Pengembangan, pelatihan, dan penerapan model ini akan diselesaikan dalam waktu 2 bulan.

**Problem Statement:**
Mengembangkan model CNN untuk membantu pelanggan memilih kacamata yang tepat berdasarkan bentuk wajah mereka, dengan target akurasi pengenalan 80% dan peningkatan kepuasan pelanggan hingga 80%, serta meningkatkan revenue toko sebesar 20% dalam waktu 2 bulan.

## Metode yang Digunakan 🛠️

- Deep Learning
- Computer Vision
- Klasifikasi Gambar
- Visualisasi Data

## Hasil dan Rekomendasi 💡

Berdasarkan beberapa model yang sudah diuji sebelumnya (base model, model improvement dan model dengan transfer learning), model yang akan dipilih adalah model dengan menggunakan transfer learning dari VGG16 dengan arsitektur sequential API. Walaupun kesalahan prediksi yang akan terjadi sebesar 30%, namun hal ini akan cukup membantu dalam pengembangan bisnis dan menyediakan fasilitas yang akan digunakan berdasarkan performa dari model ini.

**Rekomendasi:**
- Model sering salah dalam mengklasifikasikan Oval, dengan banyaknya prediksi yang keliru ke kelas lain seperti 0blong dan heart. Jadi harus memperbaiki representasi fitur atau menambah data pelatihan untuk oval guna meningkatkan akurasi prediksinya.
- Ada kesalahan prediksi signifikan antara kelas heart dan oblong, serta antara round dan square. Ini mungkin menunjukkan bahwa fitur yang dipakai kurang membedakan antara bentuk-bentuk ini. Mungkin perlu dilakukan eksplorasi lebih lanjut pada ekstraksi fitur atau penambahan fitur yang lebih relevan untuk membedakan kelas tersebut.
- Untuk kategori dengan banyak kesalahan prediksi, seperti oval dan round, penambahan data pelatihan atau melakukan augmentasi data sepertinya bisa meningkatkan performa model.
- Meskipun performa model cukup baik pada beberapa kategori, tuning hyperparameter tambahan atau eksperimen dengan arsitektur yang berbeda bisa meningkatkan akurasi keseluruhan.
- Model bisa melakukan prediksi dengan baik, tetapi aspect ratio foto disarankan 1:1 agar tidak terjadi stretching pada foto saat melakukan resize image, dan angle foto menghadap kedepan sejajar dengan kamera.

## File yang Tersedia 📂

- `CNN_computer_vision.ipynb`: Jupyter Notebook yang berisi langkah-langkah analisis data, pengembangan model deep learning, evaluasi model, dan wawasan yang diperoleh dari analisis.
- `data_inference.ipynb`: Jupyter Notebook yang berisi prediksi unseen data menggunakan model yang sudah dibuat sebelumnya
  
## Cara Menggunakan Project Ini 💻

1. Clone repositori ini ke dalam lokal Anda:
    ```bash
    git clone https://github.com/ciputrawangsa/FaceShape_Eyewear-DeepLearning-ComputerVision.git
    ```

2. Jalankan Jupyter Notebook untuk mengikuti alur analisis data:
    ```bash
    jupyter notebook P2G7_ciputra_wangsa.ipynb
    ```

## Dependencies ⚙️

- ![Jupyter Notebook](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)
- ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) 3.8.20
- ![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)

## Libraries 📚
- TensorFlow
- Keras
- OS
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

## Author ✍️
**Ciputra Wangsa**

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ciputra-wangsa/)