# [Linux] Bash uptime Penggunaan: Menunjukkan masa aktif sistem

## Overview
Perintah `uptime` digunakan untuk menunjukkan berapa lama sistem telah berjalan, serta memaparkan beban sistem dalam tempoh tertentu. Ini memberikan gambaran tentang prestasi sistem dan membantu pengguna memahami beban kerja semasa.

## Usage
Berikut adalah sintaks asas untuk perintah `uptime`:

```
uptime [options]
```

## Common Options
- `-p`: Menunjukkan masa aktif dalam format yang lebih mudah dibaca.
- `-s`: Menunjukkan waktu sistem dimulakan.
- `-h`: Menunjukkan bantuan untuk perintah ini.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `uptime`:

1. **Menunjukkan masa aktif dan beban sistem:**
   ```bash
   uptime
   ```

2. **Menunjukkan masa aktif dalam format yang lebih mudah dibaca:**
   ```bash
   uptime -p
   ```

3. **Menunjukkan waktu sistem dimulakan:**
   ```bash
   uptime -s
   ```

## Tips
- Gunakan `uptime` secara berkala untuk memantau prestasi sistem anda.
- Kombinasikan dengan perintah lain seperti `top` untuk analisis yang lebih mendalam tentang beban sistem.
- Perhatikan nilai beban yang ditunjukkan; jika ia tinggi, mungkin perlu untuk menyemak proses yang sedang berjalan.