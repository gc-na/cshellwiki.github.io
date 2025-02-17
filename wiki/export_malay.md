# [Linux] Bash export Penggunaan: Mengurus Pembolehubah Persekitaran

## Overview
Perintah `export` dalam Bash digunakan untuk menetapkan pembolehubah persekitaran yang boleh diakses oleh proses anak. Dengan menggunakan `export`, anda boleh memastikan bahawa pembolehubah yang anda buat dalam sesi terminal dapat digunakan oleh skrip atau program lain yang dijalankan dalam sesi tersebut.

## Usage
Sintaks asas untuk perintah `export` adalah seperti berikut:

```
export [options] [arguments]
```

## Common Options
- `-p`: Menunjukkan semua pembolehubah persekitaran yang telah dieksport.
- `-n`: Menghapuskan pembolehubah persekitaran yang telah dieksport.
- `VAR=value`: Menetapkan dan mengeksport pembolehubah baru.

## Common Examples
Berikut adalah beberapa contoh penggunaan `export`:

1. **Mengeksport Pembolehubah Baru**
   ```bash
   export MY_VAR="Hello World"
   ```

2. **Menyemak Pembolehubah Persekitaran**
   ```bash
   export -p
   ```

3. **Menghapus Pembolehubah Persekitaran**
   ```bash
   export -n MY_VAR
   ```

4. **Mengeksport Pembolehubah dengan Nilai**
   ```bash
   export PATH="$PATH:/usr/local/bin"
   ```

## Tips
- Sentiasa gunakan huruf besar untuk nama pembolehubah persekitaran agar mudah dikenali.
- Gunakan `export -p` untuk menyemak semua pembolehubah yang telah dieksport sebelum menambah yang baru.
- Pastikan untuk mengeksport pembolehubah yang diperlukan sebelum menjalankan skrip yang bergantung kepada mereka.