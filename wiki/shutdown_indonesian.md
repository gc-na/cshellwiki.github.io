# [Linux] Bash shutdown Penggunaan: Mematikan atau merestart sistem

## Overview
Perintah `shutdown` digunakan untuk mematikan atau merestart sistem Linux secara aman. Perintah ini memberi tahu semua pengguna bahwa sistem akan dimatikan, memberikan waktu untuk menyimpan pekerjaan mereka sebelum sistem benar-benar dimatikan.

## Usage
Berikut adalah sintaks dasar dari perintah `shutdown`:

```bash
shutdown [options] [time] [message]
```

## Common Options
- `-h`: Mematikan sistem.
- `-r`: Merestart sistem.
- `-c`: Membatalkan perintah shutdown yang sedang berjalan.
- `+m`: Menentukan waktu dalam menit sebelum sistem dimatikan (misalnya, `+5` untuk 5 menit).
- `hh:mm`: Menentukan waktu tertentu untuk mematikan sistem (format 24 jam).

## Common Examples
1. **Mematikan sistem segera:**
   ```bash
   shutdown -h now
   ```

2. **Merestart sistem segera:**
   ```bash
   shutdown -r now
   ```

3. **Mematikan sistem setelah 10 menit:**
   ```bash
   shutdown -h +10
   ```

4. **Mematikan sistem pada waktu tertentu (misalnya, 22:30):**
   ```bash
   shutdown -h 22:30
   ```

5. **Membatalkan perintah shutdown yang sedang berjalan:**
   ```bash
   shutdown -c
   ```

## Tips
- Selalu beri tahu pengguna lain sebelum mematikan sistem, gunakan opsi `message` untuk menginformasikan mereka.
- Gunakan opsi `-r` jika Anda ingin merestart sistem setelah pemeliharaan atau pembaruan.
- Pastikan untuk menyimpan semua pekerjaan sebelum menjalankan perintah shutdown untuk menghindari kehilangan data.