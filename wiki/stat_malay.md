# [Linux] Bash stat Penggunaan: Menunjukkan maklumat fail

## Overview
Perintah `stat` digunakan untuk memaparkan maklumat terperinci tentang fail atau direktori. Ia memberikan data seperti saiz fail, tarikh dan masa penciptaan, pengubahsuaian, dan akses, serta maklumat pemilik dan kebenaran fail.

## Usage
Berikut adalah sintaks asas untuk perintah `stat`:

```bash
stat [options] [arguments]
```

## Common Options
- `-c` : Format output menggunakan format yang ditentukan.
- `-f` : Tunjukkan maklumat sistem fail.
- `--format` : Menentukan format output secara khusus.
- `-t` : Tunjukkan output dalam format ringkas.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `stat`:

1. **Menunjukkan maklumat tentang satu fail:**
   ```bash
   stat fail.txt
   ```

2. **Menunjukkan maklumat tentang direktori:**
   ```bash
   stat /home/user/
   ```

3. **Menggunakan format khusus untuk output:**
   ```bash
   stat -c '%n: %s bytes' fail.txt
   ```

4. **Menunjukkan maklumat sistem fail:**
   ```bash
   stat -f /home/user/
   ```

5. **Menunjukkan output dalam format ringkas:**
   ```bash
   stat -t fail.txt
   ```

## Tips
- Gunakan pilihan `-c` untuk menyesuaikan output agar lebih mudah dibaca.
- Untuk memeriksa beberapa fail sekaligus, anda boleh menyenaraikan nama fail dalam satu perintah:
  ```bash
  stat fail1.txt fail2.txt
  ```
- Sentiasa periksa kebenaran fail jika anda menghadapi masalah akses, menggunakan `stat` untuk melihat pemilik dan kebenaran yang ditetapkan.