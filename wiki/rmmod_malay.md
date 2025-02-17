# [Linux] Bash rmmod: Mengeluarkan modul kernel

## Overview
Perintah `rmmod` digunakan untuk mengeluarkan atau memadam modul kernel yang sedang dimuat dalam sistem Linux. Modul kernel adalah komponen yang boleh dimuatkan dan dikeluarkan dari kernel semasa tanpa perlu memulakan semula sistem. Ini membolehkan pengguna untuk menambah atau mengurangkan fungsi kernel dengan lebih fleksibel.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `rmmod`:

```bash
rmmod [options] [arguments]
```

## Common Options
- `-f`: Memaksa pengeluaran modul walaupun terdapat ralat.
- `-n`: Menunjukkan nama modul yang akan dikeluarkan tanpa melakukannya.
- `--help`: Menunjukkan bantuan dan pilihan yang tersedia untuk perintah ini.
- `--version`: Menunjukkan versi perintah `rmmod`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `rmmod`:

1. Mengeluarkan modul kernel tertentu:
   ```bash
   rmmod modul_nama
   ```

2. Memaksa pengeluaran modul walaupun terdapat ralat:
   ```bash
   rmmod -f modul_nama
   ```

3. Menunjukkan nama modul tanpa mengeluarkannya:
   ```bash
   rmmod -n modul_nama
   ```

4. Mengeluarkan beberapa modul sekaligus:
   ```bash
   rmmod modul1 modul2 modul3
   ```

## Tips
- Pastikan modul yang ingin dikeluarkan tidak sedang digunakan oleh mana-mana proses lain untuk mengelakkan ralat.
- Gunakan pilihan `-f` dengan berhati-hati, kerana ia boleh menyebabkan sistem menjadi tidak stabil jika modul yang penting dikeluarkan.
- Sentiasa semak senarai modul yang sedang dimuatkan dengan perintah `lsmod` sebelum menggunakan `rmmod`.