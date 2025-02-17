# [Linux] Bash rehash Penggunaan: Memperbarui cache perintah

## Overview
Perintah `rehash` dalam Bash digunakan untuk memperbarui cache perintah yang ada di shell. Ini berguna ketika Anda telah menambahkan atau menghapus program dari direktori yang ada dalam PATH, sehingga shell dapat mengenali perintah baru tanpa harus memulai ulang sesi terminal.

## Usage
Sintaks dasar dari perintah `rehash` adalah sebagai berikut:

```bash
rehash [options] [arguments]
```

## Common Options
Perintah `rehash` tidak memiliki banyak opsi. Berikut adalah beberapa yang umum digunakan:

- `-p` : Memperbarui cache hanya untuk direktori yang ditentukan dalam PATH.

## Common Examples

1. **Memperbarui cache perintah setelah menginstal program baru:**
   ```bash
   rehash
   ```

2. **Memperbarui cache untuk direktori tertentu:**
   ```bash
   rehash -p
   ```

3. **Menggunakan rehash setelah mengubah file skrip:**
   ```bash
   # Setelah mengedit skrip di ~/bin
   rehash
   ```

## Tips
- Selalu jalankan `rehash` setelah Anda menginstal atau menghapus program untuk memastikan shell Anda mengenali perintah terbaru.
- Gunakan opsi `-p` jika Anda hanya ingin memperbarui cache untuk direktori tertentu, ini dapat menghemat waktu jika Anda memiliki banyak direktori dalam PATH.