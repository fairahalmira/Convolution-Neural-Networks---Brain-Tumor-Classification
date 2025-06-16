# Proyek Klasifikasi Tumor Otak dengan Convolutional Neural Networks (CNN)

## 📌 Pendahuluan
Proyek ini bertujuan untuk mengembangkan sistem klasifikasi tumor otak menggunakan teknologi pembelajaran mendalam, khususnya arsitektur Convolutional Neural Networks (CNN). Dengan menggunakan dataset gambar MRI otak, sistem ini mampu mengidentifikasi apakah sebuah gambar menunjukkan adanya tumor otak atau tidak.

---

# Proyek Klasifikasi Tumor Otak dengan Convolutional Neural Networks (CNN)

## 🛠️ Teknologi yang Digunakan

1. **Python**:
   Digunakan sebagai bahasa pemrograman utama untuk mengimplementasikan sistem klasifikasi.

2. **TensorFlow dan Keras**:
   Framework deep learning untuk membangun, melatih, dan mengevaluasi model klasifikasi.

3. **OpenCV dan PIL (Python Imaging Library)**:
   Digunakan untuk preprocessing gambar, seperti resizing, augmentasi, dan normalisasi.

4. **Matplotlib**:
   Untuk visualisasi hasil pelatihan dan evaluasi model.

5. **Kaggle API**:
   Untuk mengunduh dataset dari Kaggle secara langsung.

---

## 🧩 Arsitektur Model

### Komponen Utama

1. **Preprocessing Input**:
   - Gambar MRI diproses untuk memastikan ukuran konsisten (misalnya, 224x224 piksel).
   - Augmentasi gambar dilakukan untuk meningkatkan variasi data pelatihan.
   - Normalisasi nilai piksel ke rentang [0, 1].

2. **Model CNN**:
   - **Convolutional Layers**:
     Ekstraksi fitur spasial dari gambar input.
   - **Pooling Layers**:
     Reduksi dimensi data untuk mengurangi kompleksitas.
   - **Dropout Layers**:
     Mencegah overfitting selama pelatihan.
   - **Fully Connected Layers**:
     Pengambilan keputusan berdasarkan fitur yang diekstraksi.
   - **Output Layer**:
     Menghasilkan probabilitas untuk setiap kelas (tumor atau non-tumor).

3. **Postprocessing Output**:
   - Klasifikasi gambar berdasarkan probabilitas tertinggi.
   - Visualisasi hasil prediksi dengan label.

---

## 🧠 Cara Kerja Sistem Klasifikasi

1. **Mengunduh Dataset**:
   - Dataset diunduh dari Kaggle menggunakan pustaka Kaggle API.

2. **Preprocessing**:
   - Gambar diresize ke ukuran 224x224 piksel.
   - Augmentasi dilakukan untuk menambah variasi data pelatihan.
   - Data dinormalisasi untuk memastikan efisiensi pelatihan.

3. **Pelatihan Model**:
   - Dataset dibagi menjadi data pelatihan, validasi, dan pengujian.
   - Model CNN dilatih menggunakan data pelatihan dengan callback untuk early stopping dan checkpointing.

4. **Evaluasi Model**:
   - Model dievaluasi menggunakan data validasi dan pengujian untuk mengukur akurasi dan performa loss.

5. **Prediksi**:
   - Gambar baru dimasukkan ke model untuk mendapatkan hasil prediksi (tumor/non-tumor).

---

## 🎯 Hasil Prediksi

### Contoh Output

#### Tidak Ada Tumor:
![Contoh Hasil Deteksi Non-Tumor](assets/no_tumor_example.png)

---

Hasil evaluasi menunjukkan bahwa model mencapai akurasi tinggi pada data pengujian, menunjukkan efektivitas arsitektur CNN untuk klasifikasi tumor otak.
