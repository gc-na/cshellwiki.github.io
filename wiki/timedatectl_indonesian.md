# [Linux] Bash timedatectl Penggunaan: Mengelola waktu dan tanggal sistem

## Overview
Perintah `timedatectl` digunakan untuk mengelola waktu dan tanggal pada sistem Linux. Dengan perintah ini, pengguna dapat melihat informasi waktu saat ini, mengubah zona waktu, dan mengatur waktu sistem.

## Usage
Berikut adalah sintaks dasar dari perintah `timedatectl`:

```bash
timedatectl [options] [arguments]
```

## Common Options
- `status`: Menampilkan status waktu dan tanggal saat ini.
- `set-time`: Mengatur waktu dan tanggal sistem.
- `set-timezone`: Mengubah zona waktu sistem.
- `set-ntp`: Mengaktifkan atau menonaktifkan sinkronisasi waktu melalui NTP (Network Time Protocol).
- `list-timezones`: Menampilkan daftar semua zona waktu yang tersedia.

## Common Examples
1. **Menampilkan status waktu dan tanggal saat ini:**
   ```bash
   timedatectl status
   ```

2. **Mengatur waktu dan tanggal sistem:**
   ```bash
   timedatectl set-time '2023-10-01 12:00:00'
   ```

3. **Mengubah zona waktu sistem:**
   ```bash
   timedatectl set-timezone Asia/Jakarta
   ```

4. **Mengaktifkan sinkronisasi waktu NTP:**
   ```bash
   timedatectl set-ntp true
   ```

5. **Menampilkan daftar zona waktu yang tersedia:**
   ```bash
   timedatectl list-timezones
   ```

## Tips
- Pastikan untuk menjalankan perintah `timedatectl` dengan hak akses yang sesuai, biasanya sebagai pengguna root atau menggunakan `sudo`.
- Selalu periksa status waktu dan tanggal setelah melakukan perubahan untuk memastikan bahwa pengaturan telah diterapkan dengan benar.
- Gunakan opsi `list-timezones` untuk menemukan zona waktu yang tepat sebelum mengubahnya.