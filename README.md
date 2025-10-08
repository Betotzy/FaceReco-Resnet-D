# Face Recognition using ResNet-D

Proyek ini bertujuan untuk membangun dan melatih model **pengenalan wajah (Face Recognition)** berbasis **ResNet-D**, sebuah arsitektur turunan dari ResNet50 yang dioptimalkan untuk ekstraksi fitur wajah dengan performa tinggi.

## 🧠 Deskripsi Singkat

Notebook ini melakukan seluruh pipeline deep learning untuk face recognition menggunakan **PyTorch**, mulai dari:

* Persiapan dan pemrosesan dataset wajah,
* Implementasi model **ResNet-D** untuk feature extraction,
* Pelatihan model menggunakan optimizer dan scheduler,
* Evaluasi performa model melalui akurasi, confusion matrix, dan classification report.

## 📂 Struktur Notebook

1. **Import Library**
   Memuat pustaka utama seperti `torch`, `torchvision`, `sklearn`, dan `PIL`.

2. **Data Preparation**

   * Dataset wajah diambil dari folder Google Drive (`/content/drive/MyDrive/FaceReco/Dataset`).
   * File `list_attribute.txt` digunakan untuk memetakan nama file gambar dengan atribut wajah.

3. **Preprocessing**

   * Gambar diproses menggunakan transformasi (`Resize`, `ToTensor`, `Normalize`).
   * Dataset dibagi menjadi **train**, **validation**, dan **test** menggunakan `train_test_split`.

4. **Architecture**

   * Model dasar menggunakan **ResNet50**, dimodifikasi menjadi **ResNet-D** untuk menyesuaikan kebutuhan face recognition.
   * Layer fully-connected akhir disesuaikan dengan jumlah kelas dalam dataset.

5. **Modeling**

   * Loss Function: `CrossEntropyLoss`
   * Optimizer: `Adam`
   * Scheduler opsional untuk penyesuaian learning rate.
   * Training loop menampilkan metrik `loss` dan `accuracy` per epoch.

6. **Evaluation**

   * Menghitung akurasi akhir pada data uji.
   * Menampilkan **Confusion Matrix** dan **Classification Report** untuk tiap kelas wajah.

## ⚙️ Requirements

Pastikan environment memiliki pustaka berikut:

```bash
torch
torchvision
pandas
scikit-learn
matplotlib
Pillow
```

## 🚀 Cara Menjalankan

1. Clone repository ini:

   ```bash
   git clone https://github.com/username/Facereco_Resnet_D.git
   cd Facereco_Resnet_D
   ```

2. Buka notebook di Google Colab atau Jupyter Notebook:

   ```bash
   Facereco_Resnet_D.ipynb
   ```

3. Pastikan path dataset diubah sesuai lokasi Anda:

   ```python
   data_path = '/path/to/your/dataset'
   ```

4. Jalankan seluruh cell untuk melatih dan mengevaluasi model.

## 📊 Hasil dan Evaluasi

Model menunjukkan hasil akurasi tinggi pada dataset wajah, dengan loss yang rendah dan visualisasi confusion matrix yang menggambarkan performa klasifikasi tiap kelas.

## 📚 Referensi

* He et al., “Deep Residual Learning for Image Recognition” (ResNet Paper)
* PyTorch Documentation: [https://pytorch.org/](https://pytorch.org/)
* Dataset wajah yang digunakan disertai atribut dari file `list_attribute.txt`.

---

📌 *Notebook ini cocok digunakan sebagai dasar pengembangan sistem face recognition berbasis deep learning dengan arsitektur modern seperti ResNet-D.*
