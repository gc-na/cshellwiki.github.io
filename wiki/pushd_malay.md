# [Linux] Bash pushd Penggunaan: Mengurus direktori dengan mudah

## Overview
Perintah `pushd` dalam Bash digunakan untuk mengurus direktori dengan cara menyimpan direktori semasa ke dalam stack dan kemudian berpindah ke direktori baru. Ini membolehkan pengguna untuk dengan mudah kembali ke direktori asal menggunakan perintah `popd`.

## Usage
Sintaks asas untuk perintah `pushd` adalah seperti berikut:

```bash
pushd [options] [arguments]
```

## Common Options
- `+n` : Pindah ke direktori yang berada pada kedudukan n dalam stack.
- `-n` : Pindah ke direktori yang berada pada kedudukan n dalam stack tanpa menambahkannya ke dalam stack.
- `-` : Kembali ke direktori sebelumnya dalam stack.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `pushd`:

1. **Pindah ke direktori baru dan simpan direktori semasa**:
   ```bash
   pushd /path/to/directory
   ```

2. **Kembali ke direktori sebelumnya**:
   ```bash
   popd
   ```

3. **Pindah ke direktori tertentu dalam stack**:
   ```bash
   pushd +1
   ```

4. **Pindah ke direktori tanpa menambahkannya ke dalam stack**:
   ```bash
   pushd -n /another/path
   ```

## Tips
- Gunakan `dirs` untuk melihat senarai direktori dalam stack.
- Untuk navigasi yang lebih cepat, gabungkan `pushd` dengan perintah lain seperti `ls` untuk memeriksa kandungan direktori sebelum berpindah.
- Ingat untuk menggunakan `popd` untuk mengelakkan penumpukan direktori dalam stack yang tidak diperlukan.