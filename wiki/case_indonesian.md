# [Linux] Bash case penggunaan: Menangani pola string

## Overview
Perintah `case` dalam Bash digunakan untuk membandingkan nilai variabel dengan pola yang ditentukan. Ini sangat berguna untuk pengambilan keputusan dalam skrip, memungkinkan pengguna untuk mengeksekusi blok kode tertentu berdasarkan nilai variabel.

## Usage
Sintaks dasar dari perintah `case` adalah sebagai berikut:

```bash
case [variabel] in
    [pola1])
        # perintah jika pola1 cocok
        ;;
    [pola2])
        # perintah jika pola2 cocok
        ;;
    *)
        # perintah jika tidak ada pola yang cocok
        ;;
esac
```

## Common Options
- Tidak ada opsi khusus untuk `case`, tetapi pola dapat menggunakan wildcard seperti `*` dan `?` untuk mencocokkan karakter.

## Common Examples

### Contoh 1: Menentukan hari dalam seminggu
```bash
hari="Senin"

case $hari in
    "Senin")
        echo "Hari ini adalah Senin."
        ;;
    "Selasa")
        echo "Hari ini adalah Selasa."
        ;;
    "Rabu")
        echo "Hari ini adalah Rabu."
        ;;
    *)
        echo "Hari tidak dikenal."
        ;;
esac
```

### Contoh 2: Menangani input pengguna
```bash
read -p "Masukkan pilihan (a/b/c): " pilihan

case $pilihan in
    "a")
        echo "Anda memilih A."
        ;;
    "b")
        echo "Anda memilih B."
        ;;
    "c")
        echo "Anda memilih C."
        ;;
    *)
        echo "Pilihan tidak valid."
        ;;
esac
```

### Contoh 3: Menggunakan wildcard
```bash
file="laporan_2023.txt"

case $file in
    laporan_*)
        echo "Ini adalah file laporan."
        ;;
    *.txt)
        echo "Ini adalah file teks."
        ;;
    *)
        echo "Tipe file tidak dikenal."
        ;;
esac
```

## Tips
- Gunakan `*` untuk mencocokkan banyak karakter dan `?` untuk mencocokkan satu karakter dalam pola.
- Pastikan untuk menutup setiap blok dengan `;;` untuk menghindari kesalahan sintaks.
- Gunakan `*` di akhir pola untuk menangkap semua kemungkinan yang tidak ditangani sebelumnya.