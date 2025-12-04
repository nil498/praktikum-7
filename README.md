# Program Daftar Nilai Mahasiswa (Python OOP)

Program ini dibuat untuk memenuhi **Tugas Praktikum** dengan menerapkan
konsep **class** pada Python. Program digunakan untuk mengelola daftar
nilai mahasiswa, seperti menambah data, menampilkan data, menghapus
data, dan mengubah data berdasarkan nama.

## Fitur Program

### 1. tambah()

Menambah data mahasiswa: - Nama - Nilai Tugas - Nilai UTS - Nilai UAS

Nilai akhir dihitung otomatis:

    Nilai Akhir = (Tugas * 0.30) + (UTS * 0.35) + (UAS * 0.35)

### 2. tampilkan()

Menampilkan seluruh data mahasiswa.

### 3. hapus(nama)

Menghapus data berdasarkan nama.

### 4. ubah(nama)

Mengubah data mahasiswa dan menghitung ulang nilai akhir.

## Struktur Kelas

    Class : DaftarNilaiMahasiswa
    --------------------------------
    - data : list

    + tambah()
    + tampilkan()
    + hapus(nama)
    + ubah(nama)



## Cara Menjalankan Program

1.  Simpan file sebagai `daftar_nilai.py`
2.  Jalankan:

```{=html}
<!-- -->
```
    python daftar_nilai.py

