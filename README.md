#  **E-Commerce Customer Churn Prediction — Capstone Module 3**

Proyek ini merupakan bagian dari **Capstone Module 3 – Data Science**, dengan tujuan membangun model machine learning yang mampu memprediksi apakah pelanggan e-commerce akan **churn** (berhenti berbelanja) atau tidak. Notebook memuat proses lengkap mulai dari *EDA*, *feature engineering*, pemodelan, interpretasi, hingga rekomendasi bisnis.

---

##  **1. Project Overview**

Platform e-commerce sering kehilangan pelanggan akibat pengalaman buruk, harga tidak kompetitif, atau layanan yang tidak konsisten. Prediksi churn membantu perusahaan:

* Mengidentifikasi pelanggan berisiko tinggi.
* Memahami faktor-faktor utama penyebab churn.
* Menyusun strategi retensi yang lebih tepat sasaran.
* Mengoptimalkan biaya marketing & promo.

Proyek ini membangun model prediksi churn end-to-end yang siap digunakan untuk deployment.

---

##  **2. Dataset**

Dataset berisi berbagai informasi transaksi dan perilaku pelanggan, meliputi (contoh berdasarkan notebook):

* Lama berlangganan
* Jumlah transaksi
* Total pembelian
* Total cashback & diskon
* Status akun & preferensi
* Pengalaman layanan (pengiriman, refund, dll.)
* Target: **Churn** (0 = Tidak Churn, 1 = Churn)

Notebook mencakup:

✔ Data Understanding
✔ Data Cleaning & Outlier Handling
✔ Feature Engineering
✔ Train–Test Split
✔ Feature Scaling / Encoding

---

##  **3. Exploratory Data Analysis (EDA)**

Beberapa insight dari hasil EDA:

* Pola pembelian cenderung menurun sebelum pelanggan churn.
* Pelanggan churn cenderung memiliki:

  * Lebih sedikit transaksi,
  * Pembelanjaan lebih rendah,
  * Penggunaan cashback/diskon yang tidak stabil,
  * Pengalaman pengiriman lebih buruk.
* Korelasi antar fitur dianalisis untuk mempersiapkan model yang stabil.

EDA menampilkan berbagai grafik distribusi, heatmap korelasi, hingga perbandingan grup churn vs non-churn.

---

##  **4. Preprocessing & Feature Engineering**

Notebook mencakup langkah-langkah:

* Treatment missing values
* Outlier handling
* Encoding kategori (One-Hot, Label Encoding)
* Scaling untuk model tertentu
* Pembentukan fitur baru berdasarkan perilaku pelanggan
* Train–Test Split dengan stratifikasi

---

##  **5. Machine Learning Modeling**

Beberapa model yang dibangun & dibandingkan:

* **Logistic Regression**
* **Random Forest**
* **XGBoost**
* **Gradient Boosting**
* **K-Nearest Neighbors**
* **Support Vector Machine**

Setiap model dievaluasi menggunakan:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

 **Model terbaik kemudian disimpan (pickle) untuk deployment.**

---

##  **6. Model Evaluation**

Notebook menampilkan:

* Classification report
* Confusion matrix
* ROC curve
* Feature importance per model
* SHAP Value Summary
* SHAP Dependence Plots

SHAP digunakan untuk menjelaskan fitur paling berpengaruh dalam menentukan churn.

Temuan utama SHAP (ringkasan):

* Fitur seperti **frequency of purchase**, **total spend**, dan **complaints/delivery issues** memiliki pengaruh terbesar terhadap churn.
* Pelanggan dengan keterlibatan rendah memiliki probabilitas churn yang jauh lebih tinggi.

---

##  **7. Model Explainability (SHAP)**

Notebook menyediakan dua visualisasi utama SHAP:

1. **Summary Plot**
   Menunjukkan fitur mana yang paling penting secara global.

2. **Beeswarm Plot**
   Menjelaskan bagaimana nilai tiap fitur mendorong prediksi churn naik/turun.

Interpretasi ini berguna bagi tim bisnis dan operasional.

---

##  **8. Business Recommendations**

Berdasarkan hasil pemodelan & analisis:

* Fokus pada pelanggan risiko tinggi dengan transaksi menurun.
* Tingkatkan pengalaman pengiriman untuk menekan keluhan.
* Optimalkan program promo/cashback agar lebih konsisten.
* Implementasikan *personalized retention strategies*.
* Integrasikan skor churn ke dalam CRM untuk notifikasi otomatis.

---

##  **9. Project Structure**

```text
├── Capstone Modul 3.ipynb
├── data/
│   ├── raw_dataset.csv
│   └── cleaned_dataset.csv
├── models/
│   └── best_model.pkl
├── images/
│   ├── shap_summary.png
│   ├── confusion_matrix.png
│   └── feature_importance.png
└── README.md
```

---

##  **10. How to Run the Project**

1. Clone repository
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Jalankan notebook:

   ```bash
   jupyter notebook "Capstone Modul 3.ipynb"
   ```
4. Model otomatis dilatih dan disimpan di folder **models/**.

---

##  **11. Next Steps**

* Deploy model sebagai API / dashboard.
* Tracking real-time churn probability.
* Uji A/B strategi retensi berdasarkan skor churn.

---
