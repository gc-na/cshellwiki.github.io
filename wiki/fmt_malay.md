# [Linux] Bash fmt Penggunaan: Memformat teks

## Overview
Perintah `fmt` dalam Bash digunakan untuk memformat teks dengan cara mengatur lebar baris dan merapikan teks agar lebih mudah dibaca. Ia sangat berguna untuk memperbaiki format dokumen teks yang tidak teratur.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `fmt`:

```
fmt [options] [arguments]
```

## Common Options
- `-w <width>`: Menentukan lebar maksimum baris yang diinginkan. Defaultnya adalah 75 karakter.
- `-s`: Mengabaikan baris kosong dan tidak merapikan teks jika terdapat lebih dari satu baris kosong berturut-turut.
- `-u`: Menghapus spasi tambahan di antara kata-kata.

## Common Examples

### Contoh 1: Memformat Teks
Untuk memformat fail teks yang bernama `dokumen.txt` dengan lebar maksimum 50 karakter, anda boleh menggunakan:

```bash
fmt -w 50 dokumen.txt
```

### Contoh 2: Mengabaikan Baris Kosong
Jika anda ingin memformat teks tetapi mengabaikan baris kosong, gunakan pilihan `-s`:

```bash
fmt -s dokumen.txt
```

### Contoh 3: Menggunakan Lebar Default
Anda juga boleh menggunakan `fmt` tanpa pilihan untuk memformat teks dengan lebar default:

```bash
fmt dokumen.txt
```

## Tips
- Sentiasa semak lebar baris yang sesuai untuk jenis dokumen yang anda format agar hasilnya lebih baik.
- Gunakan pilihan `-u` jika anda sering menghadapi masalah dengan spasi tambahan dalam teks.
- Untuk hasil yang lebih baik, pertimbangkan untuk menggabungkan `fmt` dengan perintah lain seperti `cat` atau `less` untuk melihat hasil format dengan lebih mudah.