# [Linux] Bash swapon Penggunaan: Mengaktifkan ruang swap

## Overview
Perintah `swapon` digunakan untuk mengaktifkan ruang swap pada sistem Linux. Ruang swap adalah ruang di disk yang digunakan sebagai memori tambahan ketika RAM penuh. Dengan mengaktifkan ruang swap, sistem dapat menjalankan lebih banyak aplikasi tanpa kehabisan memori.

## Usage
Sintaks asas untuk perintah `swapon` adalah seperti berikut:

```
swapon [options] [arguments]
```

## Common Options
- `-a`: Mengaktifkan semua ruang swap yang ditentukan dalam fail `/etc/fstab`.
- `-e`: Mengabaikan kesilapan dan teruskan mengaktifkan ruang swap yang lain.
- `-s`: Menunjukkan status ruang swap yang sedang aktif.

## Common Examples
Berikut adalah beberapa contoh penggunaan `swapon`:

1. **Mengaktifkan ruang swap tertentu**:
   ```bash
   swapon /dev/sdX
   ```

2. **Mengaktifkan semua ruang swap yang ditentukan dalam `/etc/fstab`**:
   ```bash
   swapon -a
   ```

3. **Menunjukkan status ruang swap yang aktif**:
   ```bash
   swapon -s
   ```

## Tips
- Pastikan ruang swap telah dibuat dan diformat sebelum mengaktifkannya.
- Gunakan `swapon -s` untuk memeriksa ruang swap yang sedang aktif dan mengesahkan bahawa ia berfungsi dengan baik.
- Jika sistem sering menggunakan ruang swap, pertimbangkan untuk menambah RAM untuk prestasi yang lebih baik.