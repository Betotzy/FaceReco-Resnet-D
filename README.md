# FaceReco-Resnet-D
Ini adalah klasifikasi gender berdasarkan dataset foto menggunakan model ResNet D yang menghasilkan akurasi prediksi 97 %


Dataset yang digunakan adalah : CelebFaces Attributes A
Link :
Drive : https://drive.google.com/drive/folders/19YjaHthzSvqrGJ5Ye-ZEbdQsIUUW3jgT
Website : https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html


Langkah Langkah :
A. Data Preparation :
1. Mountkan ke Drive : Agar bisa mengakses data path di drive
2. Membuat variabel data_path : hubungkan variabel dengan path dataset
3. Identifikasi folder dan file dalam data_path menggunakan <code>os.listdir(data_path)
4. Membuat variabel image_list (untuk gambar) : <code>os.listdir(data_path+'/(Lokasi Folder image)')
5. 
