# 📊 Ekstraksi Fitur & Klasifikasi Gender Berdasarkan Citra Wajah

## 📌 Deskripsi

Project ini bertujuan untuk melakukan **ekstraksi fitur citra wajah** menggunakan metode:

* Fitur warna (**HSV**)
* Fitur tekstur (**GLCM**)

Hasil ekstraksi kemudian digunakan untuk membangun dataset dan melakukan **klasifikasi gender (male/female)** menggunakan algoritma **K-Nearest Neighbor (KNN)**.

---

## 🧠 Metode yang Digunakan

1. **Ekstraksi Fitur Warna (HSV)**

   * Mengambil nilai rata-rata Hue, Saturation, dan Value

2. **Ekstraksi Fitur Tekstur (GLCM)**

   * Contrast
   * Correlation
   * Energy
   * Homogeneity

3. **Klasifikasi**

   * Algoritma: KNN (K-Nearest Neighbor)

---

## 📂 Struktur Dataset

Dataset yang digunakan berasal dari:
**Indonesian Public Figure Faces**

⚠️ **PENTING:**
Dataset asli berisi folder berdasarkan nama influencer, sehingga perlu dilakukan preprocessing manual.

### 🔧 Petunjuk Persiapan Dataset

Untuk menjalankan project ini, Anda perlu:

1. Mengambil dataset **Indonesian Public Figure Faces**
2. Memisahkan citra wajah ke dalam 2 folder:

   * `male/` → berisi citra wajah laki-laki
   * `female/` → berisi citra wajah perempuan
3. Pastikan struktur folder menjadi seperti berikut:

```
datasets/
└── citra-male-female/
    ├── male/
    │   ├── img1.jpg
    │   ├── img2.jpg
    │   └── ...
    ├── female/
    │   ├── img1.jpg
    │   ├── img2.jpg
    │   └── ...
    └── test/
        ├── 1.jpg
        ├── 2.jpg
        ├── 3.jpg
        └── 4.jpg
```

---

## ⚙️ Cara Menjalankan

### 1. Mount Google Drive (Google Colab)

```python
from google.colab import drive
drive.mount('/content/drive')
```

---

### 2. Jalankan Ekstraksi Fitur

* Jalankan notebook untuk:

  * membaca citra dari folder `male` dan `female`
  * melakukan ekstraksi fitur HSV & GLCM
  * menyimpan hasil ke file `.csv`

Output:

```
fitur_wajah.csv
```

---

### 3. Training Model

* Gunakan dataset CSV hasil ekstraksi
* Latih model menggunakan KNN

---

### 4. Testing

* Masukkan citra ke folder `test/`
* Sistem akan:

  * ekstraksi fitur
  * memprediksi gender

---

## 📊 Output

* Dataset fitur dalam format `.csv`
* Hasil klasifikasi gambar test

Contoh hasil:

```
nama_file | prediksi
---------------------
1.jpg     | male
2.jpg     | female
```

---

## ⚠️ Catatan

* Dataset kecil → akurasi belum optimal

---

## 👨‍💻 Author

Project ini dibuat untuk keperluan praktikum **Computer Vision – Ekstraksi Fitur**
