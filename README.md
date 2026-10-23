# pertemuan-09-list-2225250002

---

## Tujuan Repositori
Repositori ini dibuat untuk memenuhi tugas praktikum Pertemuan 9 mata kuliah Algoritma dan Pemrograman. Repositori ini berfokus pada penggunaan *list*, operasi manipulasi dan agregasi *list*, pemfilteran data, serta pembuatan fungsi untuk analisis statistik dan penentuan kelulusan nilai mahasiswa di Python.

---

## Algoritma Tugas
1. **Inisialisasi Data**: Siapkan sekumpulan nilai numerik mahasiswa di dalam *list*.
2. **Hitung Statistik Dasar**:
   - Hitung banyak data menggunakan fungsi `len()`.
   - Hitung nilai total menggunakan `sum()`, serta tentukan nilai minimum (`min()`) dan maksimum (`max()`).
   - Hitung rata-rata data (dengan penanganan khusus agar tidak terjadi error jika *list* kosong).
3. **Pemeriksaan Kelulusan**:
   - Penelusuran (*traversing*) setiap nilai di dalam *list* untuk memeriksa syarat batas kelulusan (nilai $\ge 60$).
   - Masukkan nilai yang memenuhi syarat lulus ke dalam *list* baru (`lulus`).
4. **Hitung Ringkasan Kelulusan**:
   - Hitung jumlah mahasiswa yang lulus berdasarkan panjang *list* lulus.
   - Hitung jumlah mahasiswa yang belum lulus dari selisih total data dan jumlah lulus.
5. **Output Data**: Tampilkan ringkasan statistik dan informasi kelulusan secara rapi dan terformat.

---

## Hasil Pengujian (Test Case Wajib)

| Data | Yang diperiksa | Hasil yang diharapkan | Status |
| :--- | :--- | :--- | :-: |
| `[60, 70, 80]` | Rata-rata | 70.00 | Sesuai |
| `[60, 70, 80]` | Minimum / maksimum | 60 / 80 | Sesuai |
| `[60, 70, 80]` | Jumlah lulus | 3 | Sesuai |
| `[59, 60, 61]` | Batas kelulusan | 2 lulus | Sesuai |
| `[]` | Penanganan list kosong pada fungsi rata-rata | Tidak error | Sesuai |

---

## Cara Menjalankan
Buka terminal di direktori utama repositori ini, lalu jalankan program utama menggunakan perintah berikut:

```bash
python3 tugas/analisis_nilai_mahasiswa.py
```

## Reflekasi
Kendala yang sempat ditemukan adalah potensi terjadinya error ZeroDivisionError saat menghitung nilai rata-rata apabila list data numerik dalam keadaan kosong ([]). Masalah ini berhasil diatasi dengan menambahkan validasi pemeriksaan panjang list (if len(data) == 0: return 0) di dalam fungsi rata_rata().
