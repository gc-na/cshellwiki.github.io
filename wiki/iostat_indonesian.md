# [Linux] Bash iostat Penggunaan: Memantau Statistik I/O

## Overview
Perintah `iostat` digunakan untuk memantau statistik input/output (I/O) dari sistem, termasuk penggunaan CPU dan aktivitas disk. Ini membantu administrator sistem dalam menganalisis kinerja sistem dan mendeteksi masalah yang mungkin terjadi.

## Usage
Berikut adalah sintaks dasar dari perintah `iostat`:

```bash
iostat [options] [arguments]
```

## Common Options
- `-c`: Menampilkan statistik CPU.
- `-d`: Menampilkan statistik disk.
- `-x`: Menampilkan statistik disk yang lebih rinci.
- `-t`: Menampilkan waktu dan tanggal saat laporan dibuat.
- `interval`: Menentukan interval waktu (dalam detik) untuk memperbarui laporan.
- `count`: Menentukan jumlah laporan yang akan ditampilkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `iostat`:

1. Menampilkan statistik CPU dan disk secara default:
   ```bash
   iostat
   ```

2. Menampilkan statistik CPU saja:
   ```bash
   iostat -c
   ```

3. Menampilkan statistik disk dengan rincian tambahan:
   ```bash
   iostat -dx
   ```

4. Menampilkan statistik setiap 5 detik sebanyak 3 kali:
   ```bash
   iostat 5 3
   ```

5. Menampilkan statistik dengan waktu dan tanggal:
   ```bash
   iostat -t
   ```

## Tips
- Gunakan opsi `-x` untuk mendapatkan informasi lebih mendetail tentang penggunaan disk, yang dapat membantu dalam analisis kinerja.
- Perhatikan penggunaan CPU dan disk dalam interval waktu untuk mengidentifikasi pola atau lonjakan aktivitas.
- Simpan output `iostat` ke dalam file untuk analisis lebih lanjut dengan menggunakan redirection:
  ```bash
  iostat -dx > iostat_report.txt
  ```