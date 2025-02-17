# [Linux] Bash mkswap: [membuat fail swap]

## Overview
Perintah `mkswap` digunakan untuk menyediakan ruang swap pada sistem Linux. Ruang swap adalah kawasan pada cakera keras yang digunakan sebagai memori tambahan apabila RAM penuh. Dengan menggunakan `mkswap`, anda boleh menyiapkan fail atau partition untuk digunakan sebagai swap.

## Usage
Sintaks asas untuk perintah `mkswap` adalah seperti berikut:

```bash
mkswap [options] [arguments]
```

## Common Options
- `-f`, `--force`: Memaksa pembuatan swap walaupun terdapat kesalahan.
- `-L`, `--label LABEL`: Menetapkan label untuk ruang swap yang dibuat.
- `-p`, `--pagesize SIZE`: Menentukan saiz halaman untuk ruang swap.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mkswap`:

### Contoh 1: Membuat fail swap
Untuk membuat fail swap bernama `swapfile` dengan saiz 1GB, gunakan perintah berikut:

```bash
fallocate -l 1G /swapfile
mkswap /swapfile
```

### Contoh 2: Menggunakan partition sebagai swap
Jika anda mempunyai partition yang ingin digunakan sebagai swap, anda boleh melakukannya dengan perintah ini:

```bash
mkswap /dev/sdX
```
Gantikan `/dev/sdX` dengan nama partition yang sesuai.

### Contoh 3: Menetapkan label untuk swap
Untuk membuat swap dengan label tertentu, gunakan pilihan `-L`:

```bash
mkswap -L my_swap /swapfile
```

## Tips
- Pastikan untuk mengatur izin fail swap dengan betul setelah membuatnya, menggunakan perintah `chmod 600 /swapfile`.
- Sentiasa periksa ruang swap yang ada menggunakan perintah `swapon --show` setelah menyiapkan swap.
- Untuk mengaktifkan fail swap yang baru dibuat, gunakan perintah `swapon /swapfile`.