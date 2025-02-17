# [Linux] Bash stty Penggunaan: Mengawal tetapan terminal

## Overview
Perintah `stty` digunakan untuk mengubah dan mengawal tetapan terminal dalam sistem operasi Unix dan Linux. Ia membolehkan pengguna untuk mengkonfigurasi cara input dan output berfungsi dalam terminal, seperti mengubah pengendalian karakter, mengaktifkan atau mematikan echo, dan banyak lagi.

## Usage
Sintaks asas untuk perintah `stty` adalah seperti berikut:

```bash
stty [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `stty` beserta penjelasan ringkas:

- `-a` : Menunjukkan semua tetapan semasa terminal.
- `-g` : Mengeluarkan tetapan dalam format yang boleh digunakan semula.
- `erase` : Menetapkan karakter yang digunakan untuk menghapuskan karakter sebelumnya.
- `intr` : Menetapkan karakter untuk menghentikan proses yang sedang berjalan.
- `echo` : Menghidupkan atau mematikan echo input ke terminal.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `stty`:

1. **Menunjukkan semua tetapan terminal:**
   ```bash
   stty -a
   ```

2. **Menetapkan karakter penghapusan kepada Ctrl + H:**
   ```bash
   stty erase ^H
   ```

3. **Menghidupkan echo input:**
   ```bash
   stty echo
   ```

4. **Menetapkan karakter interupsi kepada Ctrl + C:**
   ```bash
   stty intr ^C
   ```

5. **Menyimpan tetapan semasa untuk digunakan kemudian:**
   ```bash
   stty -g > settings.txt
   ```

## Tips
- Sentiasa semak tetapan semasa sebelum membuat perubahan dengan `stty -a` untuk mengelakkan kesilapan.
- Gunakan `stty -g` untuk menyimpan tetapan yang boleh dipulihkan jika perlu.
- Berhati-hati apabila mematikan echo, kerana ini boleh menyebabkan input tidak ditunjukkan di terminal.