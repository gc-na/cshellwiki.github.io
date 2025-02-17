# [Linux] Bash head Penggunaan: Mengambil baris teratas dari fail

## Overview
Perintah `head` dalam Bash digunakan untuk memaparkan beberapa baris teratas dari satu atau lebih fail. Secara lalai, ia akan menunjukkan 10 baris pertama, tetapi pengguna boleh mengubah jumlah baris yang ingin dipaparkan.

## Usage
Berikut adalah sintaks asas untuk perintah `head`:

```bash
head [options] [arguments]
```

## Common Options
- `-n [jumlah]`: Menentukan bilangan baris yang ingin dipaparkan. Contohnya, `-n 5` akan memaparkan 5 baris pertama.
- `-c [jumlah]`: Menentukan bilangan bait yang ingin dipaparkan.
- `-q`: Tidak memaparkan nama fail sebelum output.
- `-v`: Sentiasa memaparkan nama fail sebelum output, walaupun hanya satu fail yang diproses.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `head`:

1. **Menunjukkan 10 baris pertama dari fail teks:**
   ```bash
   head fail.txt
   ```

2. **Menunjukkan 5 baris pertama dari fail teks:**
   ```bash
   head -n 5 fail.txt
   ```

3. **Menunjukkan 20 bait pertama dari fail:**
   ```bash
   head -c 20 fail.txt
   ```

4. **Menunjukkan baris pertama dari beberapa fail:**
   ```bash
   head fail1.txt fail2.txt
   ```

5. **Menunjukkan 3 baris pertama tanpa nama fail:**
   ```bash
   head -n 3 -q fail.txt
   ```

## Tips
- Gunakan `head` bersama dengan `tail` untuk mendapatkan baris tertentu dari fail. Contohnya, `tail -n +11 fail.txt | head -n 5` akan memaparkan baris 11 hingga 15.
- Jika anda ingin melihat output secara langsung dari arahan lain, anda boleh menggunakan `head` dengan pipe. Contohnya, `ls -l | head` akan menunjukkan 10 fail pertama dalam direktori.
- Ingat bahawa `head` tidak mengubah fail asal; ia hanya memaparkan output ke terminal.