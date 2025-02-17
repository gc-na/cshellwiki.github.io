# [Linux] Bash vmstat Penggunaan: Memantau Statistik Sistem

## Overview
Perintah `vmstat` digunakan untuk memantau statistik sistem, termasuk penggunaan memori, proses, dan aktivitas I/O. Dengan menggunakan `vmstat`, pengguna dapat memperoleh informasi penting tentang kinerja sistem secara real-time.

## Usage
Berikut adalah sintaks dasar dari perintah `vmstat`:

```bash
vmstat [options] [arguments]
```

## Common Options
- `-a`: Menampilkan statistik memori aktif dan tidak aktif.
- `-m`: Menampilkan statistik penggunaan memori untuk cache dan buffer.
- `-s`: Menampilkan statistik sistem dalam format ringkas.
- `-d`: Menampilkan statistik disk.
- `interval`: Menentukan interval waktu (dalam detik) untuk pembaruan statistik.

## Common Examples
Berikut adalah beberapa contoh penggunaan `vmstat`:

1. Menampilkan statistik sistem secara default:
   ```bash
   vmstat
   ```

2. Menampilkan statistik setiap 2 detik:
   ```bash
   vmstat 2
   ```

3. Menampilkan statistik memori aktif dan tidak aktif:
   ```bash
   vmstat -a
   ```

4. Menampilkan statistik disk:
   ```bash
   vmstat -d
   ```

5. Menampilkan statistik sistem dalam format ringkas:
   ```bash
   vmstat -s
   ```

## Tips
- Gunakan `vmstat` bersama dengan perintah lain seperti `top` atau `htop` untuk mendapatkan gambaran yang lebih lengkap tentang kinerja sistem.
- Perhatikan nilai `si` (swap in) dan `so` (swap out) untuk memahami apakah sistem Anda menggunakan swap, yang dapat mempengaruhi kinerja.
- Cobalah untuk menjalankan `vmstat` dalam interval yang berbeda untuk melihat bagaimana statistik berubah seiring waktu, terutama saat menjalankan aplikasi berat.