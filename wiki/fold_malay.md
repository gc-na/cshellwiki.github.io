# [Linux] Bash fold Penggunaan: Memecahkan teks kepada baris yang lebih pendek

## Overview
Perintah `fold` dalam Bash digunakan untuk memecahkan teks yang panjang kepada baris yang lebih pendek. Ini berguna untuk memastikan teks dapat dibaca dengan lebih mudah, terutamanya apabila dipaparkan pada terminal atau dalam dokumen yang mempunyai lebar terhad.

## Usage
Berikut adalah sintaks asas untuk perintah `fold`:

```
fold [options] [arguments]
```

## Common Options
- `-w, --width=N` : Menentukan lebar maksimum bagi setiap baris yang dihasilkan. N adalah bilangan aksara.
- `-s, --spaces` : Memecahkan baris pada ruang kosong terdekat sebelum lebar yang ditentukan.
- `-b, --bytes` : Mengira lebar dalam bait, bukan aksara.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `fold`:

1. Memecahkan fail teks kepada lebar 50 aksara:
   ```bash
   fold -w 50 fail.txt
   ```

2. Menggunakan `fold` dengan pemisahan pada ruang kosong:
   ```bash
   fold -s -w 30 fail.txt
   ```

3. Memecahkan output perintah lain, seperti `echo`:
   ```bash
   echo "Ini adalah contoh teks yang sangat panjang dan perlu dipendekkan." | fold -w 20
   ```

4. Mengira lebar dalam bait:
   ```bash
   fold -b -w 40 fail.txt
   ```

## Tips
- Sentiasa gunakan pilihan `-s` jika anda ingin memastikan teks tidak terputus di tengah perkataan.
- Uji lebar yang berbeza untuk melihat apa yang paling sesuai dengan keperluan anda.
- Gabungkan `fold` dengan perintah lain menggunakan paip (`|`) untuk memproses output secara langsung.