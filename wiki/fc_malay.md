# [Linux] Bash fc Penggunaan: Mengedit dan menjalankan perintah sebelumnya

## Overview
Perintah `fc` dalam Bash digunakan untuk mengedit dan menjalankan perintah yang telah dilaksanakan sebelumnya dalam sesi terminal. Ia membolehkan pengguna untuk dengan mudah mengakses dan mengubah perintah-perintah yang telah dimasukkan tanpa perlu menaip semula dari awal.

## Usage
Sintaks asas untuk perintah `fc` adalah seperti berikut:

```bash
fc [options] [arguments]
```

## Common Options
- `-l`: Menyenaraikan perintah-perintah yang telah dilaksanakan.
- `-s`: Menjalankan perintah terakhir tanpa membuka editor.
- `-n`: Menyenaraikan perintah tanpa nombor baris.
- `-e`: Menentukan editor yang ingin digunakan untuk mengedit perintah.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `fc`:

1. **Menjalankan perintah terakhir**:
   ```bash
   fc -s
   ```

2. **Menyenaraikan 5 perintah terakhir**:
   ```bash
   fc -l -n -5
   ```

3. **Mengedit perintah terakhir menggunakan editor default**:
   ```bash
   fc
   ```

4. **Mengedit perintah tertentu (contohnya perintah ke-3)**:
   ```bash
   fc 3
   ```

5. **Menjalankan perintah ke-2 tanpa mengedit**:
   ```bash
   fc -s 2
   ```

## Tips
- Gunakan `fc -l` untuk melihat senarai perintah yang telah dilaksanakan sebelum ini, ini boleh membantu anda memilih perintah yang ingin diubah.
- Jika anda sering melakukan kesilapan pada perintah tertentu, gunakan `fc` untuk mengeditnya dan simpan masa anda daripada menaip semula.
- Anda boleh menetapkan editor pilihan anda dengan menggunakan `export EDITOR=nama_editor` sebelum menggunakan `fc`.