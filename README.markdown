# Proyek Klasifikasi Gambar: Flowers Dataset

## Deskripsi
Proyek ini mengklasifikasikan gambar bunga (5 kelas: daisy, dandelion, rose, sunflower, tulip) menggunakan model Sequential dengan layer Conv2D, MaxPooling2D, dan MobileNetV2. Dataset Flowers (~4317 gambar) dibagi menjadi train (70%, 3019 gambar), validation (15%, 649 gambar), dan test (15%, 649 gambar). Model dilatih hingga akurasi ≥85%, diplot akurasi/loss, disimpan dalam format SavedModel, TF-Lite, dan TFJS, serta diuji dengan inference. Hasil akurasi akhir: training 91.92%, validation 86.29%, test 88.29%.

## Struktur Submisi
```
submission/
├── tfjs_model/
│   ├── group1-shard1of1.bin
│   └── model.json
├── tflite/
│   ├── model.tflite
│   └── label.txt
├── saved_model/
│   ├── saved_model.pb
│   └── variables/
```

## Cara Menjalankan
1. Unggah `flowers.zip` ke Google Colab.
2. Jalankan semua sel di `submission_notebook.ipynb` (aktifkan GPU untuk training lebih cepat).
3. File `submission.zip` akan dibuat di `/content/submission.zip`.

## Dependensi
Lihat `requirements.txt`.

## Kontak
- Nama: M. Hafis Afrizal
- Email: hafisafrizal10@gmail.com
- ID Dicoding: hafisafrizal