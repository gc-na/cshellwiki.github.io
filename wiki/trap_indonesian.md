# [Sistem Operasi] C Shell (csh) trap: Mengelola sinyal dan kejadian

## Overview
Perintah `trap` dalam C Shell (csh) digunakan untuk menangkap sinyal dan kejadian tertentu yang terjadi selama eksekusi skrip. Dengan menggunakan `trap`, pengguna dapat menentukan tindakan yang harus diambil ketika sinyal tertentu diterima, seperti menghentikan skrip atau menjalankan perintah tertentu.

## Usage
Berikut adalah sintaks dasar dari perintah `trap`:

```csh
trap [options] [arguments]
```

## Common Options
- `SIGINT`: Menangkap sinyal interupsi (Ctrl+C).
- `SIGTERM`: Menangkap sinyal terminasi.
- `EXIT`: Menangkap kejadian ketika skrip keluar.
- `DEBUG`: Menangkap setiap perintah yang dieksekusi.

## Common Examples

1. **Menangkap sinyal interupsi (Ctrl+C)**:
   ```csh
   trap 'echo "Sinyal interupsi diterima!"' SIGINT
   ```

2. **Menangkap sinyal terminasi dan menjalankan perintah**:
   ```csh
   trap 'echo "Skrip dihentikan!"' SIGTERM
   ```

3. **Menangkap kejadian saat skrip keluar**:
   ```csh
   trap 'echo "Skrip selesai!"' EXIT
   ```

4. **Menangkap setiap perintah yang dieksekusi**:
   ```csh
   trap 'echo "Perintah dieksekusi."' DEBUG
   ```

## Tips
- Selalu gunakan `trap` untuk menangani sinyal yang tidak terduga agar skrip dapat berfungsi dengan baik dan tidak berhenti secara tiba-tiba.
- Pastikan untuk menguji skrip Anda dengan berbagai sinyal untuk memastikan bahwa tindakan yang diinginkan dijalankan dengan benar.
- Gunakan `trap` dengan bijak untuk menjaga agar skrip Anda tetap bersih dan mudah dipahami, terutama ketika menangani banyak sinyal.