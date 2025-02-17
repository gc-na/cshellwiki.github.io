# [Linux] Bash command penggunaan: [menjalankan perintah dalam shell]

## Overview
Perintah `bash` digunakan untuk menjalankan shell Bash, yang merupakan salah satu shell yang paling popular di sistem operasi Linux dan Unix. Ia membolehkan pengguna untuk mengeksekusi perintah, menjalankan skrip, dan menguruskan proses dalam persekitaran terminal.

## Usage
Berikut adalah sintaks asas untuk perintah `bash`:

```bash
bash [options] [file]
```

## Common Options
- `-c`: Menjalankan perintah yang diberikan sebagai argumen.
- `-i`: Menjalankan shell dalam mod interaktif.
- `-l`: Menjalankan shell sebagai shell login.
- `-s`: Membaca perintah dari standard input.

## Common Examples
1. Menjalankan skrip Bash dari fail:
    ```bash
    bash script.sh
    ```

2. Menjalankan perintah secara langsung:
    ```bash
    bash -c 'echo "Hello, World!"'
    ```

3. Memulakan shell Bash interaktif:
    ```bash
    bash -i
    ```

4. Menjalankan shell Bash sebagai shell login:
    ```bash
    bash -l
    ```

## Tips
- Gunakan `bash -i` untuk mendapatkan prompt interaktif yang membolehkan anda menjalankan perintah secara langsung.
- Jika anda ingin menjalankan skrip yang tidak mempunyai izin pelaksanaan, anda boleh menggunakan `bash script.sh` untuk menjalankannya.
- Sentiasa semak skrip anda dengan `bash -n script.sh` untuk mengesan sebarang kesalahan tanpa menjalankannya.