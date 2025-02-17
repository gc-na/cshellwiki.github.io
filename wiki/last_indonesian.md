# [Linux] Bash last penggunaan: Menampilkan riwayat login pengguna

## Overview
Perintah `last` digunakan untuk menampilkan daftar login pengguna yang terakhir pada sistem. Ini memberikan informasi tentang siapa yang telah masuk ke sistem, kapan mereka masuk, dan dari mana mereka mengaksesnya. Data yang ditampilkan diambil dari file log sistem.

## Usage
Berikut adalah sintaks dasar dari perintah `last`:

```bash
last [options] [arguments]
```

## Common Options
- `-a`: Menampilkan alamat host dari mana pengguna masuk.
- `-n [number]`: Menentukan jumlah entri yang ingin ditampilkan.
- `-x`: Menampilkan informasi tentang sesi yang tidak aktif, seperti reboot dan shutdown.
- `-R`: Menghilangkan informasi tentang alamat host.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `last`:

1. Menampilkan semua login terakhir:
   ```bash
   last
   ```

2. Menampilkan 5 login terakhir:
   ```bash
   last -n 5
   ```

3. Menampilkan login terakhir dengan alamat host:
   ```bash
   last -a
   ```

4. Menampilkan informasi tentang sesi reboot dan shutdown:
   ```bash
   last -x
   ```

5. Menampilkan login terakhir untuk pengguna tertentu:
   ```bash
   last username
   ```

## Tips
- Gunakan opsi `-n` untuk membatasi jumlah entri yang ditampilkan, sehingga lebih mudah untuk membaca.
- Periksa file `/var/log/wtmp` untuk melihat data login yang lebih mendetail jika diperlukan.
- Ingat bahwa informasi yang ditampilkan oleh `last` hanya mencakup sesi yang telah berakhir, jadi tidak akan menunjukkan sesi pengguna yang sedang aktif.