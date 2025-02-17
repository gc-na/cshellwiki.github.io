# [Linux] Bash wait Penggunaan: Menunggu proses selesai

## Overview
Perintah `wait` dalam Bash digunakan untuk menunggu proses latar belakang (background process) selesai sebelum meneruskan eksekusi perintah berikutnya. Ini berguna apabila anda ingin memastikan bahawa satu atau lebih proses telah selesai sebelum melanjutkan ke langkah seterusnya dalam skrip.

## Usage
Berikut adalah sintaks asas untuk perintah `wait`:

```bash
wait [options] [arguments]
```

## Common Options
- `-n`: Menunggu proses yang pertama kali selesai di antara proses latar belakang yang sedang berjalan.
- `PID`: Menentukan ID proses tertentu yang ingin ditunggu. Jika tidak ada PID yang diberikan, `wait` akan menunggu semua proses latar belakang.

## Common Examples

### Menunggu Semua Proses Latar Belakang
```bash
sleep 5 &
sleep 3 &
wait
echo "Semua proses selesai."
```
Dalam contoh ini, skrip akan menunggu kedua-dua proses `sleep` selesai sebelum mencetak "Semua proses selesai."

### Menunggu Proses Tertentu
```bash
sleep 5 &
PID=$!
sleep 3 &
wait $PID
echo "Proses dengan PID $PID telah selesai."
```
Di sini, skrip menyimpan PID proses pertama dan menunggu hanya proses tersebut untuk selesai.

### Menunggu Proses Pertama yang Selesai
```bash
sleep 5 &
sleep 3 &
wait -n
echo "Salah satu proses telah selesai."
```
Dengan menggunakan pilihan `-n`, skrip akan mencetak "Salah satu proses telah selesai" sebaik sahaja salah satu proses selesai.

## Tips
- Gunakan `wait` dalam skrip untuk mengelakkan masalah dengan proses yang tidak selesai sebelum skrip berakhir.
- Simpan PID proses yang anda ingin tunggu untuk lebih banyak kawalan dalam skrip.
- Jika anda menggunakan `wait` tanpa sebarang argumen, ia akan menunggu semua proses latar belakang, jadi pastikan itu adalah tingkah laku yang anda inginkan.