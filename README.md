# pertemuan-09-list-2225250002

---

## Tujuan Repositori
Repositori ini dibuat untuk memenuhi tugas praktikum Pertemuan 9 mata kuliah Algoritma dan Pemrograman. Repositori ini berfokus pada pengolahan string, manipulasi teks, serta penerapan fungsi untuk melakukan normalisasi data mahasiswa dan kode kelas di Python.

---

## Algoritma Tugas
1. **Input Teks**: Membaca input nama lengkap dan kode kelas mahasiswa sebagai *string*.
2. **Pembersihan Spasi (Strip)**: Membuang spasi berlebih pada awal dan akhir string nama serta kode kelas.
3. **Normalisasi Nama (Title Case & Inisial)**:
   - Mengubah nama menjadi format *title case*.
   - Memecah nama menjadi *list* kata (*split*) untuk menghitung jumlah kata.
   - Mengambil huruf awal dari setiap kata untuk membentuk inisial mahasiswa.
4. **Normalisasi Kode Kelas**:
   - Mengubah seluruh huruf menjadi huruf besar (*upper*).
   - Mengganti spasi pada kode kelas dengan tanda hubung (`-`).
5. **Output Data**: Menampilkan hasil normalisasi nama, kode kelas, jumlah kata, dan inisial secara rapi.

---

## Hasil Pengujian (Test Case Wajib)

| Input Nama | Input Kode | Hasil Utama | Status |
| :--- | :--- | :--- | :-: |
| aan hendrayana | pmat a 2026 | Aan Hendrayana \| PMAT-A-2026 \| AH | Sesuai |
| fATHIYYAH mUTHMAINNAH | kelas b | Fathiyyah Muthmainnah \| KELAS-B \| FM | Sesuai |
| BUDI | pmtk 01 | Budi \| PMTK-01 \| B | Sesuai |
| siti nur aisyah | kelas c | Siti Nur Aisyah \| KELAS-C \| SNA | Sesuai |

---

## Cara Menjalankan
Buka terminal di direktori utama repositori ini, lalu jalankan program menggunakan perintah berikut:

```bash
python3 normalisasi_data_mahasiswa.py
```

---

## Refleksi
Kesalahan yang sempat ditemukan adalah penanganan spasi ganda atau berlebih di dalam kalimat yang membuat hasil split() menghasilkan elemen kosong, serta pemformatan kode kelas yang kurang konsisten apabila terdapat spasi berturut-turut. Masalah ini berhasil diatasi dengan memanfaatkan method .strip(), .upper(), serta pemecahan kata menggunakan .split() yang secara otomatis menangani whitespace berlebih sebelum digabungkan kembali menggunakan "-".join(). Hal ini memastikan bahwa nama lengkap, inisial, dan kode kelas terformat dengan rapi dan konsisten pada setiap pengujian.
