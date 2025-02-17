# [Linux] Bash wait Penggunaan: Menunggu Proses Selesai

## Overview
Perintah `wait` dalam Bash digunakan untuk menunggu proses latar belakang (background) selesai sebelum melanjutkan eksekusi perintah berikutnya. Ini sangat berguna ketika Anda menjalankan beberapa proses secara bersamaan dan ingin memastikan bahwa semua proses tersebut telah selesai sebelum melanjutkan.

## Usage
Sintaks dasar dari perintah `wait` adalah sebagai berikut:

```bash
wait [options] [arguments]
```

## Common Options
- `-n`: Menunggu hingga salah satu proses latar belakang selesai.
- `pid`: Menentukan ID proses tertentu yang ingin ditunggu. Jika tidak ada ID proses yang diberikan, `wait` akan menunggu semua proses latar belakang yang sedang berjalan.

## Common Examples

1. **Menunggu Semua Proses Latar Belakang**
   ```bash
   sleep 5 &
   sleep 3 &
   wait
   echo "Semua proses selesai."
   ```

2. **Menunggu Proses Tertentu dengan PID**
   ```bash
   sleep 5 &
   pid=$!
   echo "Menunggu proses dengan PID $pid..."
   wait $pid
   echo "Proses dengan PID $pid selesai."
   ```

3. **Menunggu Proses Pertama yang Selesai**
   ```bash
   sleep 5 &
   sleep 3 &
   wait -n
   echo "Salah satu proses selesai."
   ```

## Tips
- Gunakan `wait` setelah menjalankan beberapa proses latar belakang untuk memastikan semua proses selesai sebelum melanjutkan.
- Simpan ID proses (PID) ke dalam variabel jika Anda perlu menunggu proses tertentu di kemudian hari.
- Perhatikan bahwa `wait` tidak akan mengembalikan kontrol ke terminal sampai semua proses yang ditunggu selesai, jadi gunakan dengan bijak dalam skrip yang membutuhkan interaksi pengguna.