# [Linux] Bash chown Penggunaan: Mengubah pemilik dan kumpulan fail

## Overview
Perintah `chown` dalam Bash digunakan untuk mengubah pemilik dan kumpulan fail atau direktori. Ini berguna untuk menguruskan akses dan hak pemilikan dalam sistem fail Linux.

## Usage
Berikut adalah sintaks asas bagi perintah `chown`:

```bash
chown [options] [owner][:group] [file]
```

## Common Options
- `-R`: Mengubah pemilik secara rekursif untuk semua fail dan subdirektori dalam direktori.
- `-v`: Menunjukkan maklumat tentang fail yang diubah.
- `--reference=FILE`: Mengubah pemilik dan kumpulan fail kepada pemilik dan kumpulan fail lain yang ditentukan.

## Common Examples
1. **Mengubah pemilik fail:**
   ```bash
   chown alice file.txt
   ```

2. **Mengubah pemilik dan kumpulan fail:**
   ```bash
   chown alice:staff file.txt
   ```

3. **Mengubah pemilik secara rekursif dalam direktori:**
   ```bash
   chown -R alice /path/to/directory
   ```

4. **Menggunakan pilihan verbose untuk melihat perubahan:**
   ```bash
   chown -v alice file.txt
   ```

5. **Mengubah pemilik dan kumpulan berdasarkan fail lain:**
   ```bash
   chown --reference=reference.txt file.txt
   ```

## Tips
- Sentiasa semak pemilik dan kumpulan fail selepas menggunakan `chown` dengan perintah `ls -l`.
- Gunakan pilihan `-R` dengan hati-hati, kerana ia akan mengubah pemilik untuk semua fail dalam direktori.
- Pastikan anda mempunyai hak akses yang diperlukan untuk mengubah pemilik fail, biasanya memerlukan keistimewaan superuser.