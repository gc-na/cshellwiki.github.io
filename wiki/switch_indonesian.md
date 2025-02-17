# [Linux] Bash switch penggunaan: Mengubah opsi dalam skrip

## Overview
Perintah `switch` dalam konteks Bash tidak ada secara langsung. Namun, konsep `switch` sering kali diimplementasikan menggunakan pernyataan `case`, yang memungkinkan pengguna untuk memilih antara beberapa opsi berdasarkan nilai variabel. Ini sangat berguna dalam skrip untuk mengelola alur kontrol.

## Usage
Berikut adalah sintaks dasar untuk menggunakan pernyataan `case` yang berfungsi mirip dengan `switch`:

```bash
case [variable] in
    [pattern1])
        [commands1]
        ;;
    [pattern2])
        [commands2]
        ;;
    *)
        [default commands]
        ;;
esac
```

## Common Options
- **[variable]**: Variabel yang akan diperiksa nilainya.
- **[pattern]**: Pola yang akan dicocokkan dengan nilai variabel.
- **[commands]**: Perintah yang akan dijalankan jika pola cocok.
- **`*`**: Menangkap semua nilai yang tidak cocok dengan pola yang ditentukan.

## Common Examples

### Contoh 1: Menggunakan `case` untuk memilih opsi
```bash
read -p "Masukkan angka (1-3): " angka

case $angka in
    1)
        echo "Anda memilih satu."
        ;;
    2)
        echo "Anda memilih dua."
        ;;
    3)
        echo "Anda memilih tiga."
        ;;
    *)
        echo "Pilihan tidak valid."
        ;;
esac
```

### Contoh 2: Menentukan jenis file
```bash
read -p "Masukkan ekstensi file: " ekstensi

case $ekstensi in
    txt)
        echo "Ini adalah file teks."
        ;;
    jpg | jpeg)
        echo "Ini adalah file gambar."
        ;;
    pdf)
        echo "Ini adalah file PDF."
        ;;
    *)
        echo "Ekstensi tidak dikenali."
        ;;
esac
```

### Contoh 3: Menentukan hari dalam seminggu
```bash
read -p "Masukkan nama hari: " hari

case $hari in
    Senin)
        echo "Hari pertama dalam seminggu."
        ;;
    Rabu)
        echo "Hari ketiga dalam seminggu."
        ;;
    Jumat)
        echo "Hari kelima dalam seminggu."
        ;;
    *)
        echo "Hari tidak valid."
        ;;
esac
```

## Tips
- Selalu gunakan `;;` di akhir setiap blok perintah untuk menandai akhir dari pernyataan `case`.
- Gunakan `*` sebagai default untuk menangani kasus yang tidak terduga.
- Pastikan untuk memvalidasi input pengguna sebelum menggunakan pernyataan `case` untuk menghindari kesalahan.