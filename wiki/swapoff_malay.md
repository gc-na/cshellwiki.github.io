# [Linux] Bash swapoff Penggunaan: Menonaktifkan ruang swap

## Overview
Perintah `swapoff` digunakan untuk menonaktifkan ruang swap pada sistem Linux. Ruang swap adalah ruang penyimpanan yang digunakan ketika RAM penuh, dan menonaktifkannya dapat membantu meningkatkan prestasi sistem dalam situasi tertentu.

## Usage
Berikut adalah sintaks asas untuk perintah `swapoff`:

```bash
swapoff [options] [arguments]
```

## Common Options
- `-a` : Menonaktifkan semua ruang swap yang ditentukan dalam fail `/etc/fstab`.
- `-e` : Mengabaikan sebarang kesilapan yang mungkin berlaku semasa menonaktifkan ruang swap.
- `-h` : Menampilkan bantuan dan maklumat tentang penggunaan perintah.

## Common Examples
Berikut adalah beberapa contoh penggunaan `swapoff`:

1. **Menonaktifkan semua ruang swap:**
   ```bash
   swapoff -a
   ```

2. **Menonaktifkan ruang swap tertentu:**
   ```bash
   swapoff /dev/sda2
   ```

3. **Menonaktifkan ruang swap dengan mengabaikan kesilapan:**
   ```bash
   swapoff -e /dev/sda2
   ```

4. **Menampilkan bantuan untuk swapoff:**
   ```bash
   swapoff -h
   ```

## Tips
- Pastikan untuk memeriksa penggunaan RAM sebelum menonaktifkan ruang swap, kerana ini boleh menyebabkan sistem menjadi tidak stabil jika RAM sudah penuh.
- Gunakan `free -h` untuk memeriksa status memori dan ruang swap sebelum dan selepas menggunakan `swapoff`.
- Jika anda merancang untuk menonaktifkan swap secara tetap, pertimbangkan untuk mengedit fail `/etc/fstab` untuk mengeluarkan entri swap.