# [Linux] Bash lsmod Penggunaan: Menunjukkan modul kernel yang dimuat

## Overview
Perintah `lsmod` digunakan untuk memaparkan senarai modul kernel yang sedang dimuat dalam sistem Linux. Modul ini adalah komponen yang boleh dimuatkan ke dalam kernel untuk memberikan sokongan kepada pelbagai perkakasan dan fungsi.

## Usage
Sintaks asas untuk perintah `lsmod` adalah seperti berikut:

```bash
lsmod [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `lsmod`:

- `-h`, `--help`: Menunjukkan bantuan tentang penggunaan perintah.
- `-v`, `--verbose`: Menunjukkan maklumat tambahan tentang modul yang dimuat.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `lsmod`:

1. **Menunjukkan semua modul yang dimuat:**

   ```bash
   lsmod
   ```

2. **Menunjukkan bantuan untuk lsmod:**

   ```bash
   lsmod --help
   ```

3. **Menunjukkan maklumat terperinci tentang modul:**

   ```bash
   lsmod --verbose
   ```

## Tips
- Gunakan `lsmod` bersama dengan `grep` untuk mencari modul tertentu. Contohnya, untuk mencari modul `nvidia`, anda boleh menggunakan:

  ```bash
  lsmod | grep nvidia
  ```

- Perintah ini biasanya digunakan bersama dengan perintah lain seperti `modinfo` untuk mendapatkan maklumat lanjut tentang modul tertentu.
- Pastikan anda menjalankan perintah ini dengan hak akses yang sesuai jika anda ingin melihat semua modul yang dimuat.