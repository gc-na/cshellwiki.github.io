# [Linux] Bash mkfifo Penggunaan: Membuat FIFO (named pipe)

## Overview
Perintah `mkfifo` digunakan untuk membuat FIFO (First In First Out) atau named pipe di sistem operasi Unix dan Linux. FIFO memungkinkan proses untuk berkomunikasi satu sama lain dengan cara mengirim dan menerima data dalam urutan yang ditentukan.

## Usage
Sintaks dasar dari perintah `mkfifo` adalah sebagai berikut:

```bash
mkfifo [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `mkfifo`:

- `-m, --mode=MODE` : Menentukan mode izin untuk file FIFO yang dibuat. Misalnya, `-m 644` akan memberikan izin baca dan tulis kepada pemilik, serta izin baca kepada grup dan lainnya.
- `--help` : Menampilkan bantuan tentang penggunaan perintah `mkfifo`.
- `--version` : Menampilkan versi dari perintah `mkfifo`.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `mkfifo`:

1. **Membuat FIFO sederhana:**
   ```bash
   mkfifo myfifo
   ```

2. **Membuat FIFO dengan izin khusus:**
   ```bash
   mkfifo -m 666 myfifo
   ```

3. **Membuat beberapa FIFO sekaligus:**
   ```bash
   mkfifo fifo1 fifo2 fifo3
   ```

4. **Menggunakan FIFO dalam komunikasi antar proses:**
   - Di satu terminal, Anda bisa menulis ke FIFO:
     ```bash
     echo "Hello, FIFO!" > myfifo
     ```
   - Di terminal lain, Anda bisa membaca dari FIFO:
     ```bash
     cat myfifo
     ```

## Tips
- Pastikan untuk menghapus FIFO yang tidak lagi digunakan dengan perintah `rm` untuk mencegah kebingungan.
- Gunakan izin yang tepat saat membuat FIFO untuk memastikan bahwa proses lain dapat mengaksesnya sesuai kebutuhan.
- Ingat bahwa FIFO bersifat blocking, artinya jika tidak ada proses yang membaca dari FIFO, proses yang mencoba menulis ke FIFO akan terhenti sampai ada yang membaca.