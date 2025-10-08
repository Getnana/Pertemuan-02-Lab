# Pertemuan-02-Lab
Deskripsi:
Fuzzy logic untuk memodelkan risiko diabetes berdasarkan tiga variabel utama dari dataset: Glucose, BMI, dan Age. 

Langkah-langkah yang dilakukan:
1. Data Preparation:
   - Menggunakan dataset diabetes (subset 100 baris).
   - Dipilih tiga variabel: Glucose, BMI, dan Age.

2. Fuzzy Membership Functions:
   - Glucose: Low, Medium, High
   - BMI: Low, Medium, High
   - Age: Young, Middle, Old
   - Risk: Low, Medium, High

3. Rule Base Fuzzy:
   - Jika Glucose tinggi dan BMI tinggi atau Age tua → Risiko tinggi
   - Jika Glucose sedang dan BMI sedang → Risiko sedang
   - Jika Glucose rendah, BMI rendah, dan Age muda → Risiko rendah

4. Fuzzy Inference & Defuzzification:
   - Menghasilkan skor risiko (`FuzzyRiskScore`) untuk setiap pasien.
   - Skor ini diubah menjadi kategori risiko: Low, Medium, High.
   - Kolom baru `FuzzyRiskScore` ditambahkan ke dataset.

5. Visualization:
   - Membuat histogram distribusi `FuzzyRiskScore` menggunakan seaborn.
   - Visualisasi menunjukkan penyebaran skor risiko pada sampel pasien.

6. Machine Learning:
   - Menggunakan nilai membership (fuzzy features) sebagai input untuk model Support Vector Machine (SVM).
   - Target label menggunakan `Outcome` dari dataset asli.
   - Akurasi model SVM masih rendah karena hanya menggunakan tiga fitur fuzzy sederhana.
   - Insight: fuzzy logic membantu membuat fitur interpretable, namun prediksi lebih akurat bila fitur lain ikut digunakan.

Kesimpulan:
- Fuzzy logic dapat digunakan untuk membuat model risiko diabetes yang lebih mudah dipahami.
- Kolom baru `FuzzyRiskScore` berhasil memberikan insight tambahan tentang distribusi risiko.
- Implementasi SVM dengan fuzzy features memberikan gambaran awal, meskipun performa prediksi masih terbatas.
