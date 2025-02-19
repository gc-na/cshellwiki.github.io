# [Sistem Operasi] C Shell (csh) wait Penggunaan: Menunggu Proses Selesai

## Overview
Perintah `wait` dalam C Shell (csh) digunakan untuk menunggu proses latar belakang selesai sebelum melanjutkan eksekusi perintah berikutnya. Ini sangat berguna ketika Anda ingin memastikan bahwa suatu proses telah selesai sebelum melanjutkan dengan tugas lain.

## Usage
Berikut adalah sintaks dasar dari perintah `wait`:

```
wait [options] [arguments]
```

## Common Options
- `-p`: Menunggu proses tertentu berdasarkan ID proses (PID).
- `-n`: Menunggu proses terakhir yang selesai dari semua proses latar belakang yang dijalankan.

## Common Examples

1. **Menunggu Semua Proses Latar Belakang**
   ```csh
   sleep 5 &
   sleep 3 &
   wait
   echo "Semua proses selesai."
   ```

2. **Menunggu Proses Tertentu dengan PID**
   ```csh
   sleep 5 &
   pid=$!
   echo "Menunggu proses dengan PID $pid..."
   wait $pid
   echo "Proses dengan PID $pid selesai."
   ```

3. **Menunggu Proses Terakhir yang Selesai**
   ```csh
   sleep 5 &
   sleep 3 &
   sleep 4 &
   wait -n
   echo "Proses terakhir selesai."
   ```

## Tips
- Gunakan `wait` setelah menjalankan beberapa proses latar belakang untuk memastikan semua proses telah selesai sebelum melanjutkan.
- Simpan PID proses yang dijalankan di latar belakang untuk menunggu proses tertentu jika diperlukan.
- Pastikan untuk menangani potensi kesalahan jika proses yang ditunggu tidak ada atau telah selesai sebelumnya.