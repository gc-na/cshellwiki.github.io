# [Linux] Bash ftp Penggunaan: Mengurus pemindahan fail melalui FTP

## Overview
Perintah `ftp` digunakan untuk mengurus pemindahan fail antara komputer melalui protokol File Transfer Protocol (FTP). Ia membolehkan pengguna untuk menyambung ke pelayan FTP, memuat naik dan memuat turun fail, serta menguruskan direktori.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `ftp`:

```bash
ftp [options] [arguments]
```

## Common Options
- `-i`: Mematikan mod interaktif, membolehkan pemindahan fail tanpa meminta pengesahan.
- `-v`: Menunjukkan maklumat terperinci semasa pemindahan.
- `-n`: Menghalang ftp daripada secara automatik menyambung ke pelayan.
- `-p`: Menggunakan mod pasif untuk sambungan FTP.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `ftp`:

1. **Menyambung ke pelayan FTP:**
   ```bash
   ftp ftp.example.com
   ```

2. **Muat turun fail dari pelayan:**
   ```bash
   get nama_fail.txt
   ```

3. **Muat naik fail ke pelayan:**
   ```bash
   put nama_fail.txt
   ```

4. **Melihat senarai fail dalam direktori pelayan:**
   ```bash
   ls
   ```

5. **Menggunakan mod pasif:**
   ```bash
   ftp -p ftp.example.com
   ```

## Tips
- Sentiasa gunakan mod pasif (`-p`) jika anda menghadapi masalah sambungan, terutamanya di belakang firewall.
- Pastikan anda keluar dari sesi FTP dengan menggunakan perintah `bye` atau `quit` untuk mengelakkan sambungan terbuka.
- Gunakan `-v` untuk mendapatkan maklumat tambahan semasa pemindahan, ini boleh membantu dalam menyelesaikan masalah.