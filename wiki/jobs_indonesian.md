# [Linux] Bash jobs Penggunaan: Mengelola Proses Latar Belakang

## Overview
Perintah `jobs` dalam Bash digunakan untuk menampilkan daftar proses yang berjalan di latar belakang dalam sesi shell saat ini. Ini membantu pengguna untuk memantau dan mengelola proses yang telah dijalankan, termasuk proses yang dihentikan atau ditangguhkan.

## Usage
Berikut adalah sintaks dasar dari perintah `jobs`:

```
jobs [options] [arguments]
```

## Common Options
- `-l`: Menampilkan ID proses (PID) dari setiap pekerjaan.
- `-n`: Menampilkan hanya pekerjaan yang telah berubah status sejak perintah `jobs` terakhir dijalankan.
- `-p`: Menampilkan hanya PID dari pekerjaan yang sedang berjalan.

## Common Examples

1. **Menampilkan Daftar Pekerjaan**
   ```bash
   jobs
   ```

2. **Menampilkan Daftar Pekerjaan dengan PID**
   ```bash
   jobs -l
   ```

3. **Menampilkan Pekerjaan yang Baru Berubah Status**
   ```bash
   jobs -n
   ```

4. **Menampilkan PID dari Pekerjaan yang Sedang Berjalan**
   ```bash
   jobs -p
   ```

## Tips
- Gunakan `bg` untuk melanjutkan pekerjaan yang dihentikan ke latar belakang setelah melihat daftar dengan `jobs`.
- Gunakan `fg` untuk membawa pekerjaan latar belakang ke depan dan melanjutkan eksekusinya.
- Periksa status pekerjaan secara berkala untuk memastikan tidak ada yang terhenti atau gagal.