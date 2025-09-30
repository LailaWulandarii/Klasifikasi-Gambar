# *Rice Image Classification with CNN*

Proyek ini bertujuan untuk membangun model CNN yang dapat mengklasifikasikan gambar butir beras menjadi lima kategori: Arborio, Basmati, Ipsala, Jasmine, dan Karacadag. Proyek ini mencakup seluruh pipeline, mulai dari preprocessing data, pelatihan model CNN, evaluasi performa, hingga konversi model ke format yang sesuai untuk deployment.

---

## 🔍 *Insight*

### *Dataset*
- Dataset mencakup *75.025 gambar* yang dibagi menjadi:
  - *Train*: 52.525 gambar
  - *Validation*: 11.250 gambar
  - *Test*: 11.250 gambar
- Terdiri dari *5 kelas*: Arborio, Basmati, Ipsala, Jasmine, dan Karacadag.
- Gambar diresize menjadi *128x128 piksel* untuk standarisasi input model.

### *Modeling*
- Model CNN dikembangkan menggunakan arsitektur *Sequential* dengan *4 blok konvolusi*.
- Teknik *augmentasi data* digunakan untuk meningkatkan generalisasi model.
- Regularisasi termasuk *Batch Normalization* dan *Dropout* diterapkan untuk mengurangi overfitting.
- Pelatihan dilakukan dengan optimizer *Adam* dan loss function *categorical_crossentropy*.
- Callbacks seperti *EarlyStopping* dan *ModelCheckpoint* digunakan untuk mengontrol proses pelatihan.

### *Evaluasi & Visualisasi*
- Akurasi Test: Model mencapai akurasi **99.49%* dengan loss *0.0141* pada data uji.
- Grafik *akurasi* dan *loss* menunjukkan pelatihan yang stabil tanpa overfitting signifikan.
- *Confusion Matrix*: Mayoritas prediksi berada pada diagonal, menunjukkan akurasi tinggi untuk setiap kelas.
- *Classification Report*:
  - Semua metrik seperti precision, recall, dan f1-score rata-rata mendekati *1.00* untuk setiap kelas.

### *Konversi Model*
Model berhasil dikonversi ke berbagai format untuk deployment yang lebih fleksibel:
- *SavedModel*: Cocok untuk deployment di server atau lingkungan lokal.
- *TFLite*: Didesain untuk perangkat mobile atau embedded dengan efisiensi tinggi.
- *TensorFlow.js (TFJS)*: Memungkinkan model untuk berjalan langsung di browser, mendukung aplikasi berbasis web secara real-time.
  
### *Inference*
- Model dalam format SavedModel digunakan untuk inferensi gambar baru.
- Hasil inference menunjukkan akurasi konsisten:
  - *inference.jpg* → Arborio (100%)
  - *inference 2.jpg* → Karacadag (100%)

---

## 🚀 *Teknologi yang Digunakan*
- Python 3
- TensorFlow & Keras
- NumPy, Matplotlib, Seaborn
- scikit-learn
- Pillow (PIL)
- TensorFlow Lite Converter

---

## 📌 *Catatan*
- Augmentasi data memainkan peran penting dalam meningkatkan performa model.
- Regularisasi berhasil mengurangi overfitting, membuat model mampu menyamaratakan data baru dengan baik.
  
---

## 🙌 *Kesimpulan*
Proyek ini berhasil menghasilkan model klasifikasi dengan akurasi tinggi dan performa yang konsisten. Pipeline yang mencakup preprocessing hingga deployment memastikan model dapat diintegrasikan ke berbagai platform dengan efisien dan efektif untuk aplikasi nyata.
\
