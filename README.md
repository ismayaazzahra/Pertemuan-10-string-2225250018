# Pertemuan 10 String dan Pengolahan Teks

## Identitas

Nama: Ismaya Catur Dewi Azzahra  
NIM: 2225250018  
Kelas: 3A

## Tujuan

Tujuan dari tugas ini adalah mengolah dan menormalisasi data teks menggunakan string Python, memakai indeks, slicing, dan method string (`strip`, `lower`, `upper`, `title`, `replace`, `find`, `count`), memecah teks dengan `split()` dan menggabungkannya dengan `join()`, membuat fungsi untuk memproses teks, serta mengunggah hasil pengerjaan ke GitHub.

## Cara Menjalankan Program

Program dijalankan melalui VS Code menggunakan Python.

Langkah-langkah:

1. Buka folder `pertemuan-10-string-2225250018` di VS Code.
2. Buka file `tugas/normalisasi_data_mahasiswa.py`.
3. Jalankan program melalui terminal dengan perintah `python3 tugas/normalisasi_data_mahasiswa.py` (di Windows gunakan `python`).
4. Masukkan nama dan kode kelas saat diminta oleh program.
5. Periksa hasil program berdasarkan test case yang diberikan.

## Struktur Fungsi

| Fungsi                   | Parameter | Nilai return                               | Keterangan                                                             |
| ------------------------ | --------- | ------------------------------------------ | ---------------------------------------------------------------------- |
| `normalisasi_nama(nama)` | nama      | Nama dalam format title case               | Membuang spasi berlebih dengan `split()` dan `join()`, lalu `title()`. |
| `buat_inisial(nama)`     | nama      | Huruf awal setiap kata                     | Memakai nama yang sudah dinormalisasi lalu mengambil karakter pertama. |
| `normalisasi_kode(kode)` | kode      | Kode kelas huruf besar dengan tanda hubung | `strip()`, `upper()`, `split()`, lalu `join()` dengan `-`.             |

## Algoritma

1. Baca nama dan kode kelas sebagai string.
2. Normalisasi nama menggunakan `split()`, `join()`, dan `title()`.
3. Pecah nama menjadi list kata, lalu hitung jumlah kata dengan `len()`.
4. Bentuk inisial dari karakter pertama setiap kata.
5. Normalisasi kode kelas menggunakan `strip()`, `upper()`, `split()`, dan `join()`.
6. Tampilkan nama bersih, kode kelas, jumlah kata, dan inisial.

## Hasil Pengujian

| Input nama              | Input kode  | Diharapkan                                 | Aktual                                     | Status |
| ----------------------- | ----------- | ------------------------------------------ | ------------------------------------------ | ------ |
| ` aan hendrayana`       | pmat a 2026 | Aan Hendrayana, PMAT-A-2026, 2 kata, AH    | Aan Hendrayana, PMAT-A-2026, 2 kata, AH    | Lulus  |
| `fATHIYYAH mUTHMAINNAH` | kelas b     | Fathiyyah Muthmainnah, KELAS-B, 2 kata, FM | Fathiyyah Muthmainnah, KELAS-B, 2 kata, FM | Lulus  |
| `BUDI`                  | pmtk 01     | Budi, PMTK-01, 1 kata, B                   | Budi, PMTK-01, 1 kata, B                   | Lulus  |
| ` siti nur aisyah`      | kelas c     | Siti Nur Aisyah, KELAS-C, 3 kata, SNA      | Siti Nur Aisyah, KELAS-C, 3 kata, SNA      | Lulus  |

## Refleksi

Masalah teks yang saya temukan adalah nama dengan spasi berlebih dan kapitalisasi acak sehingga sulit dibandingkan. Perbaikannya adalah normalisasi dengan `strip()`, `split()`, `join()`, dan `title()`. `strip()` hanya menghapus spasi di awal dan akhir, jadi spasi di tengah ditangani dengan `split()` lalu `join()`.

Saya juga memahami bahwa string bersifat immutable, sehingga perubahan dilakukan dengan membuat string baru, bukan mengubah satu karakter. List dan string sama-sama urutan, sehingga indeks, slicing, dan perulangan dapat dipakai pada keduanya.