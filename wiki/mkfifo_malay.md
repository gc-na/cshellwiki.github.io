# [Linux] Bash mkfifo Penggunaan: Membuat fail FIFO (first-in, first-out)

## Overview
Perintah `mkfifo` digunakan untuk membuat fail FIFO (first-in, first-out) di dalam sistem fail. Fail FIFO membolehkan komunikasi antara proses dengan cara menghantar dan menerima data secara berurutan.

## Usage
Sintaks asas untuk menggunakan perintah `mkfifo` adalah seperti berikut:

```bash
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE` : Menetapkan hak akses untuk fail FIFO yang baru dibuat.
- `--help` : Menunjukkan maklumat bantuan untuk perintah ini.
- `--version` : Menunjukkan versi perintah `mkfifo`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `mkfifo`:

1. **Membuat fail FIFO dengan nama `myfifo`:**
   ```bash
   mkfifo myfifo
   ```

2. **Membuat fail FIFO dengan hak akses tertentu:**
   ```bash
   mkfifo -m 644 myfifo
   ```

3. **Membuat beberapa fail FIFO sekaligus:**
   ```bash
   mkfifo fifo1 fifo2 fifo3
   ```

4. **Menggunakan fail FIFO dalam komunikasi antara dua proses:**
   ```bash
   # Dalam satu terminal, tulis:
   cat > myfifo
   # Dalam terminal lain, baca dari myfifo:
   cat < myfifo
   ```

## Tips
- Pastikan untuk menghapus fail FIFO setelah selesai menggunakannya untuk mengelakkan kekeliruan.
- Gunakan hak akses yang sesuai untuk fail FIFO agar hanya proses yang dibenarkan dapat mengaksesnya.
- Untuk menguji komunikasi antara proses, gunakan terminal yang berbeza untuk menjalankan perintah yang berkaitan dengan fail FIFO.