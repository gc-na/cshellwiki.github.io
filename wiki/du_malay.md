# [Linux] Bash du Penggunaan: Mengukur saiz direktori dan fail

## Overview
Perintah `du` (disk usage) digunakan untuk mengukur saiz direktori dan fail dalam sistem fail. Ia memberikan maklumat tentang ruang yang digunakan oleh fail dan subdirektori, membolehkan pengguna untuk memahami penggunaan ruang disk mereka dengan lebih baik.

## Usage
Berikut adalah sintaks asas untuk perintah `du`:

```bash
du [options] [arguments]
```

## Common Options
- `-h`: Menunjukkan saiz dalam format yang mudah dibaca (contohnya, KB, MB).
- `-s`: Menunjukkan jumlah saiz untuk setiap argumen, bukan untuk setiap fail dan subdirektori.
- `-a`: Menunjukkan saiz untuk semua fail, bukan hanya direktori.
- `-c`: Menunjukkan jumlah keseluruhan di akhir output.
- `--max-depth=N`: Menunjukkan saiz untuk direktori hingga kedalaman N.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `du`:

1. **Mengukur saiz direktori semasa:**
   ```bash
   du -h
   ```

2. **Mengukur saiz direktori tertentu:**
   ```bash
   du -h /path/to/directory
   ```

3. **Menunjukkan saiz setiap fail dan subdirektori:**
   ```bash
   du -ah /path/to/directory
   ```

4. **Menunjukkan jumlah saiz untuk direktori tertentu:**
   ```bash
   du -sh /path/to/directory
   ```

5. **Menunjukkan saiz dengan kedalaman maksimum 1:**
   ```bash
   du -h --max-depth=1 /path/to/directory
   ```

## Tips
- Gunakan pilihan `-h` untuk mendapatkan output yang lebih mudah dibaca.
- Jika anda hanya memerlukan jumlah keseluruhan untuk direktori, gunakan pilihan `-s`.
- Untuk memantau penggunaan ruang disk secara berkala, pertimbangkan untuk menggabungkan `du` dengan perintah lain seperti `sort` untuk mengatur output berdasarkan saiz.