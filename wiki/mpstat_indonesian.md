# [Sistem Operasi] C Shell (csh) mpstat Penggunaan: Memantau statistik CPU

## Overview
Perintah `mpstat` digunakan untuk menampilkan statistik penggunaan CPU secara real-time. Ini memberikan informasi tentang aktivitas CPU di sistem, termasuk persentase waktu CPU yang digunakan untuk berbagai tugas seperti pengguna, sistem, dan idle.

## Usage
Berikut adalah sintaks dasar dari perintah `mpstat`:

```csh
mpstat [options] [arguments]
```

## Common Options
- `-P ALL`: Menampilkan statistik untuk semua CPU.
- `-u`: Menampilkan statistik penggunaan CPU dalam format persentase.
- `-h`: Menampilkan output dalam format yang lebih mudah dibaca.
- `interval`: Menentukan interval waktu (dalam detik) untuk pembaruan statistik.
- `count`: Menentukan jumlah pengulangan yang akan ditampilkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mpstat`:

1. Menampilkan statistik CPU untuk semua prosesor setiap 5 detik:
   ```csh
   mpstat -P ALL 5
   ```

2. Menampilkan penggunaan CPU dalam format persentase:
   ```csh
   mpstat -u
   ```

3. Menampilkan statistik CPU dengan output yang lebih mudah dibaca:
   ```csh
   mpstat -h
   ```

4. Menampilkan statistik CPU setiap 2 detik selama 3 kali:
   ```csh
   mpstat 2 3
   ```

## Tips
- Gunakan opsi `-P ALL` untuk mendapatkan gambaran lengkap dari semua CPU di sistem Anda.
- Pertimbangkan untuk menggabungkan `mpstat` dengan alat pemantauan lainnya untuk analisis yang lebih mendalam.
- Simpan output `mpstat` ke dalam file untuk analisis lebih lanjut dengan menggunakan redirection, misalnya:
  ```csh
  mpstat -P ALL 5 > cpu_stats.txt
  ```