# [Linux] Bash mpstat Penggunaan: Memantau Statistik CPU

## Overview
Perintah `mpstat` digunakan untuk menampilkan statistik penggunaan CPU pada sistem Linux. Ini memberikan informasi tentang penggunaan CPU secara keseluruhan dan juga per CPU jika ada lebih dari satu. Dengan `mpstat`, pengguna dapat menganalisis kinerja CPU dan mengidentifikasi potensi masalah.

## Usage
Berikut adalah sintaks dasar dari perintah `mpstat`:

```bash
mpstat [options] [arguments]
```

## Common Options
- `-P ALL` : Menampilkan statistik untuk semua CPU.
- `-u` : Menampilkan penggunaan CPU dalam persentase.
- `-h` : Menampilkan output dalam format yang lebih mudah dibaca (human-readable).
- `interval` : Menentukan interval waktu (dalam detik) antara pengukuran.
- `count` : Menentukan jumlah pengukuran yang akan dilakukan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mpstat`:

1. Menampilkan statistik CPU untuk semua CPU setiap 1 detik:
   ```bash
   mpstat -P ALL 1
   ```

2. Menampilkan penggunaan CPU dalam format yang lebih mudah dibaca:
   ```bash
   mpstat -u -h 1 5
   ```

3. Menampilkan statistik CPU untuk CPU tertentu (misalnya CPU 0):
   ```bash
   mpstat -P 0 2
   ```

4. Menampilkan statistik CPU dengan interval 2 detik dan 3 pengukuran:
   ```bash
   mpstat 2 3
   ```

## Tips
- Gunakan opsi `-P ALL` untuk mendapatkan gambaran lengkap tentang penggunaan CPU di semua inti.
- Perhatikan nilai `idle` untuk memahami seberapa banyak CPU yang tidak digunakan, ini bisa membantu dalam mengidentifikasi bottleneck.
- Jika Anda melakukan pemantauan jangka panjang, pertimbangkan untuk mengarahkan output ke file untuk analisis lebih lanjut:
  ```bash
  mpstat -P ALL 1 10 > cpu_stats.txt
  ```