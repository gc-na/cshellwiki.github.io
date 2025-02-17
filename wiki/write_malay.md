# [Linux] Bash tulis perintah: menghantar mesej kepada pengguna lain

## Overview
Perintah `write` dalam Bash digunakan untuk menghantar mesej teks secara langsung kepada pengguna lain yang sedang log masuk ke sistem. Ini membolehkan komunikasi yang cepat dan mudah antara pengguna dalam persekitaran terminal.

## Usage
Sintaks asas untuk menggunakan perintah `write` adalah seperti berikut:

```bash
write [options] [user] [tty]
```

## Common Options
- `-n`: Menghantar mesej tanpa menambah nama pengguna di awal.
- `-s`: Menghantar mesej secara senyap tanpa memaparkan mesej di skrin penerima.

## Common Examples

1. **Menghantar mesej kepada pengguna tertentu:**
   ```bash
   write john
   Hello John, can we meet at 3 PM?
   ```
   Dalam contoh ini, mesej "Hello John, can we meet at 3 PM?" akan dihantar kepada pengguna bernama John.

2. **Menghantar mesej secara senyap:**
   ```bash
   write -s jane
   Please check your email.
   ```
   Mesej ini akan dihantar kepada Jane tanpa sebarang makluman di skrin.

3. **Menghantar mesej kepada pengguna di tty tertentu:**
   ```bash
   write john pts/1
   Are you available for a quick chat?
   ```
   Di sini, mesej dihantar kepada pengguna John yang sedang menggunakan tty `pts/1`.

## Tips
- Pastikan penerima tidak menggunakan perintah `mesg n`, kerana ini akan menghalang mereka daripada menerima mesej.
- Gunakan perintah `who` untuk melihat senarai pengguna yang sedang log masuk dan tty mereka sebelum menghantar mesej.
- Untuk menghentikan sesi `write`, tekan `Ctrl + D` untuk menghantar EOF (End of File).