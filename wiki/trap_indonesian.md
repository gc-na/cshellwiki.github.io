# [Linux] Bash trap Penggunaan: Mengelola sinyal dan kejadian

## Overview
Perintah `trap` dalam Bash digunakan untuk menangani sinyal dan kejadian tertentu yang terjadi selama eksekusi skrip. Dengan menggunakan `trap`, Anda dapat menentukan tindakan yang harus diambil ketika sinyal tertentu diterima, seperti menghentikan skrip dengan bersih atau menjalankan fungsi tertentu.

## Usage
Sintaks dasar dari perintah `trap` adalah sebagai berikut:

```bash
trap [options] [commands] [signals]
```

## Common Options
- `-l`: Menampilkan daftar sinyal yang tersedia.
- `-p`: Menampilkan perintah yang terdaftar untuk sinyal yang ditentukan.
- `signals`: Daftar sinyal yang ingin Anda tangani, seperti `SIGINT`, `SIGTERM`, dll.

## Common Examples

### Contoh 1: Menangani Sinyal SIGINT
Menangkap sinyal `SIGINT` (biasanya dihasilkan oleh Ctrl+C) dan menjalankan perintah tertentu.

```bash
trap 'echo "Sinyal SIGINT diterima. Keluar..."' SIGINT
while true; do
    echo "Menunggu sinyal..."
    sleep 1
done
```

### Contoh 2: Membersihkan Sebelum Keluar
Menggunakan `trap` untuk membersihkan file sementara sebelum skrip keluar.

```bash
trap 'rm -f /tmp/tempfile; echo "File sementara dihapus."' EXIT
touch /tmp/tempfile
echo "Skrip sedang berjalan..."
sleep 5
```

### Contoh 3: Menangani Beberapa Sinyal
Menangani beberapa sinyal sekaligus dengan satu perintah.

```bash
trap 'echo "Sinyal diterima, keluar..."' SIGINT SIGTERM
while true; do
    echo "Menunggu sinyal..."
    sleep 1
done
```

## Tips
- Selalu gunakan `trap` untuk menangani sinyal yang dapat menghentikan skrip Anda secara tiba-tiba, seperti `SIGINT` dan `SIGTERM`.
- Pastikan untuk menguji skrip Anda dengan sinyal yang berbeda untuk memastikan bahwa penanganan sinyal berfungsi seperti yang diharapkan.
- Gunakan `trap` dengan perintah `EXIT` untuk menjalankan pembersihan atau tindakan lain saat skrip selesai, baik secara normal maupun karena sinyal.