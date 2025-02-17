# [Linux] Bash fdisk Penggunaan: Mengurus partisi cakera

## Overview
Perintah `fdisk` adalah alat yang digunakan untuk mengurus partisi pada cakera keras dalam sistem operasi Linux. Ia membolehkan pengguna untuk membuat, mengubah, dan menghapus partisi, serta memaparkan maklumat tentang struktur partisi pada cakera.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `fdisk`:

```
fdisk [options] [arguments]
```

## Common Options
- `-l`: Menunjukkan senarai semua partisi pada semua cakera.
- `-u`: Menggunakan unit sektor untuk menunjukkan saiz partisi.
- `-n`: Membuat partisi baru.
- `-d`: Menghapus partisi yang sedia ada.
- `-s`: Menunjukkan saiz partisi dalam sektor.

## Common Examples
1. **Menunjukkan senarai partisi pada cakera**:
   ```bash
   fdisk -l
   ```

2. **Membuat partisi baru**:
   ```bash
   fdisk /dev/sda
   ```
   (Kemudian, ikuti arahan dalam antaramuka interaktif untuk membuat partisi.)

3. **Menghapus partisi**:
   ```bash
   fdisk /dev/sda
   ```
   (Masukkan arahan interaktif untuk memilih dan menghapus partisi.)

4. **Menunjukkan saiz partisi dalam sektor**:
   ```bash
   fdisk -s /dev/sda1
   ```

## Tips
- Sentiasa buat salinan sandaran data penting sebelum mengubah suai partisi.
- Gunakan `man fdisk` untuk mendapatkan maklumat lanjut tentang semua pilihan dan cara penggunaannya.
- Pastikan anda mempunyai hak akses yang mencukupi (biasanya sebagai pengguna root) untuk menjalankan perintah `fdisk`.