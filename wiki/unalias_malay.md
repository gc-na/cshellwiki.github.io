# [Linux] Bash unalias Penggunaan: Menghapus alias dalam sesi terminal

## Overview
Perintah `unalias` digunakan dalam Bash untuk menghapus alias yang telah ditetapkan sebelumnya. Alias adalah nama pendek yang digunakan untuk menggantikan perintah yang lebih panjang, dan dengan `unalias`, anda dapat menghapus alias tersebut agar tidak lagi digunakan dalam sesi terminal.

## Usage
Berikut adalah sintaks asas untuk perintah `unalias`:

```bash
unalias [options] [arguments]
```

## Common Options
- `-a`: Menghapus semua alias yang ditetapkan.
- `-p`: Menampilkan semua alias yang ada tanpa menghapusnya.

## Common Examples
Berikut adalah beberapa contoh penggunaan `unalias`:

1. **Menghapus alias tertentu**:
   Jika anda mempunyai alias bernama `ll` yang merujuk kepada `ls -l`, anda boleh menghapusnya dengan perintah berikut:
   ```bash
   unalias ll
   ```

2. **Menghapus semua alias**:
   Untuk menghapus semua alias yang telah ditetapkan dalam sesi terminal, gunakan:
   ```bash
   unalias -a
   ```

3. **Menampilkan semua alias**:
   Untuk melihat semua alias yang ada tanpa menghapusnya, gunakan:
   ```bash
   unalias -p
   ```

## Tips
- Sentiasa semak alias yang telah ditetapkan sebelum menggunakan `unalias` untuk memastikan anda tidak menghapus alias yang penting.
- Gunakan `unalias -a` dengan hati-hati, kerana ini akan menghapus semua alias dan mungkin mengganggu aliran kerja anda.
- Pertimbangkan untuk menyimpan alias yang sering digunakan dalam fail konfigurasi seperti `.bashrc` agar mudah diakses kembali jika diperlukan.