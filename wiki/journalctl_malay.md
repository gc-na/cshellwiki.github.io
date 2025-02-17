# [Linux] Bash journalctl Penggunaan: Mengurus log sistem

## Overview
Perintah `journalctl` digunakan untuk mengakses dan mengurus log sistem yang dihasilkan oleh `systemd`. Ia membolehkan pengguna melihat log yang disimpan dalam sistem, membantu dalam penyelesaian masalah dan pemantauan sistem.

## Usage
Berikut adalah sintaks asas untuk menggunakan `journalctl`:

```bash
journalctl [options] [arguments]
```

## Common Options
- `-b` : Menunjukkan log dari boot semasa.
- `-f` : Mengikuti log secara langsung (seperti `tail -f`).
- `--since` : Menunjukkan log dari tarikh atau masa tertentu.
- `--until` : Menunjukkan log hingga tarikh atau masa tertentu.
- `-u` : Menunjukkan log untuk unit tertentu (misalnya, perkhidmatan).

## Common Examples
Berikut adalah beberapa contoh penggunaan `journalctl`:

1. **Melihat semua log:**
   ```bash
   journalctl
   ```

2. **Melihat log dari boot semasa:**
   ```bash
   journalctl -b
   ```

3. **Mengikuti log secara langsung:**
   ```bash
   journalctl -f
   ```

4. **Melihat log untuk perkhidmatan tertentu:**
   ```bash
   journalctl -u nama_perkhidmatan
   ```

5. **Melihat log dari tarikh tertentu:**
   ```bash
   journalctl --since "2023-10-01" --until "2023-10-10"
   ```

## Tips
- Gunakan `-f` untuk memantau log secara langsung semasa anda menjalankan aplikasi.
- Filter log dengan `--since` dan `--until` untuk mendapatkan maklumat yang lebih tepat.
- Simpan log ke dalam fail dengan menggunakan `journalctl > log.txt` untuk analisis lanjut.