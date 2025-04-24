## 🦎 Reptiles & Amphibians Image Classification

### 📁 Deskripsi  
Proyek ini mengklasifikasikan gambar hewan ke dalam dua kelompok besar: **Reptil** dan **Amfibi**, berdasarkan data visual dari 9 kelas spesies (Salamander, Turtle/Tortoise, Frog, Lizard, Toad,
           Crocodile/Alligator, Iguana, Snake, Chameleon, Gecko)
### 🧪 Metode Penelitian
- **Preprocessing**: Resize gambar, ubah ke RGB, dan ekstraksi fitur.
- **Ekstraksi Fitur**: 
  - **HOG (bentuk)**  
  - **Histogram warna (warna)**  
  - **Hu Moments (geometri)**
- **Model**: K-Nearest Neighbors (KNN), dipilih lewat Grid Search.
- **Evaluasi**: Confusion matrix, classification report (akurasi, precision, recall, f1-score).

### 🔧 Tools
- Python, OpenCV, scikit-image, scikit-learn, matplotlib, seaborn, Gradio.

### 🎯 Tujuan
- Membangun sistem klasifikasi gambar hewan berbasis fitur visual.
- Mengelompokkan hewan ke dalam kategori Reptil atau Amfibi secara otomatis.
- Memberikan visualisasi hasil prediksi dan interaksi langsung melalui antarmuka Gradio.

### ✅ Output
Model mampu mengenali jenis hewan dari gambar input dan menampilkannya dalam bentuk tabel prediksi serta visualisasi performa model.
