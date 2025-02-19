# [Sistem Operasi] C Shell (csh) htop Penggunaan: Memantau penggunaan sumber daya sistem

## Overview
Perintah `htop` adalah alat interaktif untuk memantau penggunaan sumber daya sistem secara real-time. Ini memberikan tampilan yang lebih informatif dan mudah digunakan dibandingkan dengan perintah `top`, memungkinkan pengguna untuk melihat proses yang berjalan, penggunaan CPU, memori, dan swap dengan cara yang lebih visual.

## Usage
Berikut adalah sintaks dasar untuk menggunakan perintah `htop`:

```csh
htop [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `htop`:

- `-h`, `--help`: Menampilkan bantuan tentang penggunaan `htop`.
- `-s`, `--sort`: Mengurutkan tampilan berdasarkan kolom tertentu (misalnya, CPU atau memori).
- `-p`, `--pid`: Menampilkan hanya proses dengan ID tertentu.
- `-u`, `--user`: Menampilkan hanya proses yang dimiliki oleh pengguna tertentu.

## Common Examples
Berikut adalah beberapa contoh penggunaan `htop`:

1. Menjalankan `htop` tanpa opsi:
   ```csh
   htop
   ```

2. Menampilkan bantuan:
   ```csh
   htop -h
   ```

3. Mengurutkan proses berdasarkan penggunaan CPU:
   ```csh
   htop -s PERCENT_CPU
   ```

4. Menampilkan proses untuk pengguna tertentu:
   ```csh
   htop -u username
   ```

5. Menampilkan proses dengan ID tertentu:
   ```csh
   htop -p 1234
   ```

## Tips
- Gunakan tombol panah untuk menavigasi antar proses dan tekan `F9` untuk membunuh proses yang dipilih.
- Anda dapat menyesuaikan tampilan dengan menekan `F2` untuk membuka menu setup.
- Untuk memperbarui tampilan secara manual, tekan `F5` untuk mengubah tampilan menjadi pohon proses. 

Dengan menggunakan `htop`, Anda dapat dengan mudah memantau dan mengelola proses yang berjalan di sistem Anda.