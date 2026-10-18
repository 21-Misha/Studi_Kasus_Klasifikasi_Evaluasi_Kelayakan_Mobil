# Penerapan Data Mining untuk Klasifikasi Evaluasi Kelayakan Mobil

## Deskripsi Proyek

Proyek ini menerapkan teknik **Data Mining dengan metode klasifikasi** untuk mengidentifikasi pola hubungan antara karakteristik mobil dan kategori evaluasi kelayakannya. Algoritma yang digunakan adalah **Decision Tree Classifier** dari library Scikit-learn.

Model dibangun berdasarkan karakteristik mobil, meliputi harga pembelian, biaya perawatan, jumlah pintu, kapasitas penumpang, ukuran bagasi, dan tingkat keselamatan. Hasil klasifikasi digunakan untuk memprediksi kategori evaluasi mobil ke dalam empat kelas, yaitu `unacc`, `acc`, `good`, dan `vgood`.

## Dataset

Dataset yang digunakan adalah **Car Evaluation Dataset** dari UCI Machine Learning Repository.

- Sumber: [UCI Machine Learning Repository – Car Evaluation](https://archive.ics.uci.edu/dataset/19/car+evaluation)
- Jumlah observasi: 1.728 data
- Jumlah variabel prediktor: 6
- Variabel target: `class`
- Jenis data: Kategorikal

### Variabel Dataset

| Variabel | Keterangan |
|---|---|
| `buying` | Harga pembelian mobil |
| `maint` | Biaya perawatan mobil |
| `doors` | Jumlah pintu |
| `persons` | Kapasitas penumpang |
| `lug_boot` | Ukuran bagasi |
| `safety` | Tingkat keselamatan |
| `class` | Kategori evaluasi mobil |

## Metode

Algoritma yang digunakan adalah **Decision Tree Classifier** dengan kriteria pemisahan `Gini`.

Decision Tree membentuk struktur pohon keputusan berdasarkan atribut yang digunakan untuk memisahkan data ke dalam kategori tertentu. Algoritma ini dipilih karena dapat digunakan untuk klasifikasi data kategorikal serta menghasilkan aturan keputusan yang relatif mudah diinterpretasikan.

## Tahapan Analisis

1. **Pengumpulan Data**  
   Mengambil dataset Car Evaluation dari UCI Machine Learning Repository.

2. **Eksplorasi Data**  
   Memeriksa dimensi dataset, tipe data, nilai yang hilang, data duplikat, dan distribusi kategori evaluasi mobil.

3. **Preprocessing**  
   Mengubah variabel kategorikal menjadi representasi numerik menggunakan `OrdinalEncoder` dan `LabelEncoder`.

4. **Pembagian Data**  
   Membagi dataset menjadi data latih sebesar 80% dan data uji sebesar 20% dengan mempertahankan proporsi kelas menggunakan `stratify`.

5. **Pemodelan**  
   Melatih model Decision Tree Classifier menggunakan data latih.

6. **Evaluasi Model**  
   Mengukur kinerja klasifikasi menggunakan Accuracy, Precision, Recall, F1-score, dan Confusion Matrix.

## Hasil Analisis

Model Decision Tree Classifier menghasilkan nilai akurasi sebesar **98,55%** pada data uji yang terdiri dari 346 observasi.

Hasil evaluasi menunjukkan bahwa model mampu mengklasifikasikan kategori evaluasi mobil dengan tingkat ketepatan yang tinggi. Namun, performa pada kelas `vgood` memiliki nilai Recall sebesar 0,85, sehingga masih terdapat beberapa data pada kategori tersebut yang belum berhasil diklasifikasikan dengan tepat.

Hasil ini menunjukkan bahwa Decision Tree dapat digunakan untuk mengidentifikasi pola klasifikasi pada dataset Car Evaluation, meskipun kinerja model tetap perlu diperhatikan pada setiap kategori evaluasi.

## Teknologi yang Digunakan

- Python
- Google Colab
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- ucimlrepo

## Cara Menjalankan

1. Buka notebook Google Colab yang tersedia di repository ini.
2. Jalankan instalasi library yang diperlukan jika belum tersedia.
3. Jalankan setiap bagian notebook secara berurutan, mulai dari pengumpulan data hingga evaluasi model.
4. Perhatikan hasil klasifikasi, metrik evaluasi, dan visualisasi Decision Tree.

## Referensi

1. UCI Machine Learning Repository. [Car Evaluation Dataset](https://archive.ics.uci.edu/dataset/19/car+evaluation).
2. Scikit-learn. [DecisionTreeClassifier Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html).
3. Scikit-learn. [Model Evaluation Documentation](https://scikit-learn.org/stable/modules/model_evaluation.html).
4. Scikit-learn. [train_test_split Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html).
