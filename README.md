## 1.9 Pernyataan urutan kerja

Ini salah satu luaran yang dinilai. Salin paragraf berikut ke `README.md`, **periksa kebenarannya terhadap yang benar-benar Anda jalankan**, lalu sesuaikan bila berbeda.

> Pada cabang klastering tidak ada pemisahan data latih dan data uji, karena tidak ada label yang diuji. Pembersihan dilakukan sekali atas seluruh data: buang duplikat, pisahkan kolom identitas, buang kolom non-numerik, imputasi median, lalu pembatasan pencilan dengan IQR 1,5. Hasilnya disimpan sebagai `data_bersih.csv` dan dipakai ketiga varian apa adanya. Penskalaan tidak dilakukan pada tahap pembersihan, melainkan di dalam tiap varian dan sekali lagi saat model final dilatih: `StandardScaler` di-fit satu kali pada data bersih, lalu disimpan sebagai `scaler.pkl` dan dipakai aplikasi web dengan `transform`, bukan `fit_transform`. Pengodean kategori tidak dipakai, karena pada K-Means hanya fitur numerik yang dipakai.

**Mengapa berbeda dari cabang klasifikasi.** Pada k-NN urutan wajibnya adalah bersihkan, pisahkan data, baru skalakan — penskalaan sebelum pemisahan membuat statistik data uji bocor ke pelatihan. Pada klastering tidak ada pemisahan, sehingga yang dijaga bukan kebocoran antar-himpunan, melainkan **kesamaan skala antara notebook dan aplikasi web**.

## Checklist Bagian 1

- [✔️] `data/raw.csv` ada dan tidak pernah diubah lagi
- [✔️] `data/data_bersih.csv` ada sebagai berkas di repositori, bukan hanya sel notebook
- [✔️] `gambar/eda_distribusi.png` dan `gambar/eda_korelasi.png` ter-commit
- [✔️] Empat jawaban di 1.6 sudah ditulis sendiri
- [ ] Pernyataan urutan kerja sudah masuk `README.md` dan sudah diperiksa
- [✔️] Kedua anggota lain sudah menerima `data_bersih.csv`
- [ ] Mulai sekarang tidak ada lagi yang membersihkan data sendiri-sendiri
