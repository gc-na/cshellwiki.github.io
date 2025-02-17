# [Linux] Bash sysctl Penggunaan: Mengurus parameter kernel

## Overview
Perintah `sysctl` digunakan untuk mengurus dan mengubah parameter kernel Linux pada waktu berjalan. Ia membolehkan pengguna untuk melihat dan mengubah pelbagai tetapan sistem yang berkaitan dengan prestasi dan keselamatan.

## Usage
Berikut adalah sintaks asas untuk perintah `sysctl`:

```bash
sysctl [options] [arguments]
```

## Common Options
- `-a`: Menunjukkan semua parameter kernel dan nilai semasa.
- `-w`: Mengubah nilai parameter kernel.
- `-p`: Memuatkan parameter dari fail konfigurasi.
- `-n`: Menunjukkan nilai parameter tanpa nama parameter.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sysctl`:

1. **Melihat semua parameter kernel:**
   ```bash
   sysctl -a
   ```

2. **Mengubah nilai parameter kernel:**
   ```bash
   sysctl -w net.ipv4.ip_forward=1
   ```

3. **Memuatkan parameter dari fail konfigurasi:**
   ```bash
   sysctl -p
   ```

4. **Menunjukkan nilai spesifik tanpa nama parameter:**
   ```bash
   sysctl -n net.ipv4.tcp_max_syn_backlog
   ```

## Tips
- Sentiasa buat salinan konfigurasi sebelum mengubah parameter kernel.
- Gunakan `sysctl -a` untuk mendapatkan gambaran keseluruhan tentang parameter yang boleh diubah.
- Untuk perubahan yang kekal selepas reboot, tambahkan parameter ke dalam fail `/etc/sysctl.conf`.