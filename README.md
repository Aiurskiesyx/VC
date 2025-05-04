## 🧠 **Image Classification of Animal Species (Reptiles, Amphibians, Sea Animals)**

### 📁 **Deskripsi Umum**

Proyek ini mengembangkan dua sistem klasifikasi gambar hewan berbasis pembelajaran mesin dan deep learning. Sistem pertama mengklasifikasikan gambar spesies ke dalam dua kelompok besar: **Reptil** dan **Amfibi**, sementara sistem kedua mengklasifikasikan berbagai **hewan laut** ke dalam beberapa kelas visual berdasarkan dataset citra. Keduanya mengandalkan pendekatan yang berbeda.

### 📊 **Studi Kasus 1: Reptiles & Amphibians**

Klasifikasi dilakukan terhadap 10 kelas hewan: *Salamander, Turtle/Tortoise, Frog, Lizard, Toad, Crocodile/Alligator, Iguana, Snake, Chameleon, dan Gecko*. Proses meliputi:

* **Preprocessing**: Konversi gambar ke format standar (RGB, resize).
* **Ekstraksi Fitur**:

  * **HOG** untuk bentuk
  * **Histogram warna** untuk informasi warna
  * **Hu Moments** untuk karakteristik bentuk geometri
* **Model**: K-Nearest Neighbors (KNN), dioptimalkan melalui Grid Search.
* **Evaluasi**: Confusion matrix dan classification report (akurasi, precision, recall, f1-score).
* **Output**: Sistem mampu mengelompokkan hewan ke dalam dua kategori utama (Reptil atau Amfibi), lengkap dengan visualisasi hasil prediksi dan antarmuka interaktif menggunakan Gradio.

---

### 🌊 **Studi Kasus 2: Sea Animal Classification (ResNet50)**

Dataset berisi gambar hewan laut dari berbagai kelas, diklasifikasikan menggunakan deep learning berbasis **transfer learning** dengan arsitektur ResNet50. Kelas-kelas dalam dataset ini mencakup 23 jenis hewan laut, antara lain: *Clams, Corals, Crabs, Dolphin, Eel, Fish, Jelly Fish, Lobster, Nudibranchs, Octopus, Otter, Penguin, Puffers, Sea Rays, Sea Urchins, Seahorse, Seal, Sharks, Shrimp, Squid, Starfish, Turtle_Tortoise, dan Whale*.  Prosesnya mencakup:

* **Preprocessing & Split Data**: Dataset dibagi 80:20 (train/validation), dengan ukuran gambar distandarkan ke 224x224 piksel.
* **Augmentasi**: Rotasi acak, zoom, dan flipping untuk memperkaya data latih.
* **Model**:

  * Pretrained ResNet50 (tanpa top layer)
  * Tambahan GlobalAveragePooling, Dense layer, dan output softmax.
* **Training**:

  * Optimasi dengan *Adam Optimizer*
  * Callback *EarlyStopping* dan *ReduceLROnPlateau*
* **Evaluasi**:

  * Visualisasi akurasi dan loss per epoch
  * Classification report dan confusion matrix
  * Visualisasi prediksi gambar acak
* **Output**: Sistem mampu mengenali berbagai spesies hewan laut dan menampilkan prediksi secara visual.


### 🛠 **Tools dan Teknologi**

* Python, OpenCV, Scikit-learn, TensorFlow/Keras, Scikit-image, Matplotlib, Seaborn, Gradio.


### 🎯 **Tujuan Umum**

* Membangun sistem klasifikasi gambar hewan dengan pendekatan fitur dan deep learning.
* Menghasilkan model yang mampu mengenali spesies berdasarkan ciri visual.
* Menyediakan visualisasi evaluasi model dan antarmuka pengguna untuk interaksi langsung.
