# [Linux] Bash printenv Penggunaan: Mencetak pembolehubah persekitaran

## Overview
Perintah `printenv` digunakan untuk mencetak semua pembolehubah persekitaran yang sedang aktif dalam sesi terminal. Ini membolehkan pengguna melihat nilai-nilai yang ditetapkan dalam persekitaran sistem mereka.

## Usage
Sintaks asas untuk menggunakan perintah `printenv` adalah seperti berikut:

```bash
printenv [options] [arguments]
```

## Common Options
- `-0` : Menggunakan pemisah null untuk output.
- `NAME` : Jika diberikan, hanya nilai pembolehubah persekitaran dengan nama yang ditentukan akan dicetak.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `printenv`:

1. **Mencetak semua pembolehubah persekitaran:**
   ```bash
   printenv
   ```

2. **Mencetak nilai pembolehubah persekitaran tertentu (contohnya, `HOME`):**
   ```bash
   printenv HOME
   ```

3. **Mencetak pembolehubah persekitaran dengan pemisah null:**
   ```bash
   printenv -0
   ```

## Tips
- Gunakan `printenv` untuk menyemak pembolehubah persekitaran sebelum menjalankan skrip untuk memastikan semua nilai yang diperlukan telah ditetapkan.
- Anda boleh menggabungkan `printenv` dengan perintah lain menggunakan paip (`|`) untuk memproses output lebih lanjut.
- Untuk menyimpan output `printenv` ke dalam fail, gunakan pengalihan (`>`) seperti berikut:
  ```bash
  printenv > env_variables.txt
  ```