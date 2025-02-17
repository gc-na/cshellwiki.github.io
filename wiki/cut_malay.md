# [Linux] Bash cut Penggunaan: Memotong bahagian teks

## Overview
Perintah `cut` dalam Bash digunakan untuk memotong dan mengekstrak bahagian tertentu dari setiap baris dalam fail teks atau input standard. Ia sangat berguna untuk memproses data yang terstruktur, seperti fail CSV atau teks berformat lain.

## Usage
Berikut adalah sintaks asas untuk perintah `cut`:

```bash
cut [options] [arguments]
```

## Common Options
- `-f` : Menentukan medan (field) yang ingin dipotong, berdasarkan pemisah yang ditentukan.
- `-d` : Menentukan pemisah (delimiter) yang digunakan untuk memisahkan medan. Secara default, pemisah adalah tab.
- `-c` : Memotong berdasarkan karakter tertentu. Anda boleh menentukan julat karakter yang ingin dipotong.
- `--complement` : Mengembalikan semua medan kecuali yang ditentukan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cut`:

1. **Memotong berdasarkan medan dengan pemisah koma:**
   ```bash
   cut -d',' -f1 data.csv
   ```
   Perintah ini akan mengekstrak medan pertama dari setiap baris dalam fail `data.csv`, menggunakan koma sebagai pemisah.

2. **Memotong berdasarkan julat karakter:**
   ```bash
   echo "Hello World" | cut -c1-5
   ```
   Ini akan menghasilkan `Hello`, iaitu lima karakter pertama dari input.

3. **Menggunakan `cut` untuk mengekstrak medan kedua dan ketiga:**
   ```bash
   cut -d':' -f2,3 /etc/passwd
   ```
   Perintah ini akan mengekstrak medan kedua dan ketiga dari fail `/etc/passwd`, yang biasanya mengandungi maklumat pengguna.

4. **Menggunakan `--complement` untuk mendapatkan semua medan kecuali yang ditentukan:**
   ```bash
   cut -d' ' -f1 --complement file.txt
   ```
   Ini akan mengekstrak semua medan kecuali medan pertama dari setiap baris dalam `file.txt`.

## Tips
- Sentiasa tentukan pemisah dengan `-d` jika data anda tidak menggunakan pemisah tab.
- Gunakan `-f` untuk mengekstrak beberapa medan sekaligus dengan menyenaraikan mereka, seperti `-f1,3,5`.
- Untuk memproses fail besar, pertimbangkan untuk mengalihkan output ke fail lain untuk analisis lanjut.