# [Linux] Bash ss Penggunaan: Memaparkan soket rangkaian

## Overview
Perintah `ss` digunakan untuk memaparkan soket rangkaian yang aktif di sistem Linux. Ia memberikan maklumat terperinci tentang sambungan rangkaian, termasuk soket TCP, UDP, dan UNIX, serta status dan statistik berkaitan.

## Usage
Berikut adalah sintaks asas untuk perintah `ss`:

```bash
ss [options] [arguments]
```

## Common Options
- `-t`: Paparkan soket TCP sahaja.
- `-u`: Paparkan soket UDP sahaja.
- `-l`: Paparkan soket yang sedang mendengar.
- `-p`: Paparkan proses yang menggunakan soket.
- `-n`: Paparkan alamat dan nombor port dalam format nombor, bukan nama.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ss`:

1. **Paparkan semua soket TCP:**
   ```bash
   ss -t
   ```

2. **Paparkan semua soket UDP:**
   ```bash
   ss -u
   ```

3. **Paparkan soket yang sedang mendengar:**
   ```bash
   ss -l
   ```

4. **Paparkan semua soket dengan maklumat proses:**
   ```bash
   ss -p
   ```

5. **Paparkan semua soket dengan alamat dan nombor port dalam format nombor:**
   ```bash
   ss -n
   ```

## Tips
- Gunakan `ss -t -l` untuk melihat semua soket TCP yang sedang mendengar, berguna untuk mengesahkan pelayan yang sedang berjalan.
- Kombinasikan pilihan untuk mendapatkan maklumat yang lebih terperinci, contohnya `ss -tunap` untuk melihat semua soket TCP dan UDP dengan maklumat proses.
- Sentiasa pastikan anda menjalankan perintah ini dengan hak akses yang sesuai jika anda ingin melihat semua soket yang digunakan oleh proses lain.