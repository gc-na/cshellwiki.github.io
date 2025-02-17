# [Linux] Bash unsetenv Penggunaan: Menghapus variabel lingkungan

## Overview
Perintah `unsetenv` digunakan untuk menghapus variabel lingkungan dalam sesi shell. Dengan menggunakan perintah ini, Anda dapat menghapus variabel yang tidak lagi diperlukan, sehingga membantu menjaga kebersihan lingkungan shell Anda.

## Usage
Berikut adalah sintaks dasar dari perintah `unsetenv`:

```bash
unsetenv [nama_variabel]
```

## Common Options
Perintah `unsetenv` tidak memiliki banyak opsi, tetapi berikut adalah beberapa yang umum digunakan:
- Tidak ada opsi khusus: `unsetenv` hanya memerlukan nama variabel yang ingin dihapus.

## Common Examples
Berikut adalah beberapa contoh penggunaan `unsetenv`:

1. Menghapus satu variabel lingkungan:
   ```bash
   unsetenv MY_VARIABLE
   ```

2. Menghapus variabel lingkungan yang telah ditetapkan sebelumnya:
   ```bash
   export MY_VAR="Hello World"
   unsetenv MY_VAR
   ```

3. Menghapus variabel yang tidak ada (tidak akan menghasilkan kesalahan):
   ```bash
   unsetenv NON_EXISTENT_VAR
   ```

## Tips
- Pastikan untuk memeriksa variabel yang ingin Anda hapus sebelum menggunakan `unsetenv`, untuk menghindari penghapusan yang tidak disengaja.
- Gunakan perintah `printenv` atau `env` untuk melihat daftar variabel lingkungan yang ada sebelum dan sesudah menggunakan `unsetenv`.
- Perintah ini biasanya digunakan dalam skrip shell untuk membersihkan variabel yang tidak lagi diperlukan setelah proses tertentu selesai.