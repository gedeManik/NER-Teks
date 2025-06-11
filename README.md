# Named Entity Recognition dengan CRF pada Dataset CoNLL-2002
Proyek ini melakukan Named Entity Recognition (NER) pada teks berbahasa Spanyol menggunakan dataset CoNLL-2002 dan algoritma Conditional Random Fields (CRF) melalui pustaka sklearn-crfsuite.

## 📂 Dataset
Dataset yang digunakan adalah bagian bahasa Spanyol dari CoNLL-2002, yang tersedia melalui NLTK:
esp.train: Data pelatihan
esp.testb: Data pengujian
Setiap kalimat diberi anotasi dalam format IOB (Inside, Outside, Beginning), yang umum digunakan dalam tugas NER untuk menandai entitas seperti nama orang, organisasi, lokasi, dll.

## ⚙️ Fitur
Setiap kata diekstrak menjadi vektor fitur, meliputi:
- Bentuk kata dan huruf kapital
- Prefiks dan sufiks
- Posisi dalam kalimat
- Kata sebelum dan sesudahnya
- Pola bentuk kata (apakah mengandung angka, huruf besar, dll)

## 🧠 Model
Model yang digunakan:
- Conditional Random Fields (CRF) dari sklearn_crfsuite.CRF
- Dilatih menggunakan data esp.train
- Diuji menggunakan esp.testb

## 📊 Evaluasi
Evaluasi model dilakukan dengan:
- F1-score
- Precision & Recall
- Classification report dari sklearn_crfsuite.metrics
- (Opsional) Tuning hyperparameter dengan RandomizedSearchCV

## 🚀 Cara Menjalankan

Instal dependensi:
```
pip install nltk sklearn sklearn-crfsuite scipy matplotlib
```

Unduh dataset NLTK:
```
import nltk
nltk.download('conll2002')
```

Buka Jupyter Notebook dan jalankan semua sel.

## 📈 Visualisasi
Notebook juga menyertakan visualisasi sederhana menggunakan matplotlib untuk membantu memahami performa model dan pentingnya fitur.
