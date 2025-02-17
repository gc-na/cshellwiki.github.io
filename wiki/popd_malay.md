# [Linux] Bash popd Penggunaan: Mengeluarkan direktori dari tumpukan

## Overview
Perintah `popd` digunakan dalam Bash untuk mengeluarkan direktori dari tumpukan direktori yang telah disimpan. Ia membolehkan pengguna untuk kembali ke direktori sebelumnya yang telah disimpan dengan perintah `pushd`.

## Usage
Sintaks asas untuk menggunakan `popd` adalah seperti berikut:

```bash
popd [options]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `popd`:

- `-n`: Tidak mengubah direktori semasa, hanya mengeluarkan direktori dari tumpukan.
- `+n`: Mengeluarkan direktori dari tumpukan berdasarkan indeks, di mana `n` adalah nombor indeks.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `popd`:

1. **Mengeluarkan direktori teratas dari tumpukan:**

   ```bash
   popd
   ```

2. **Mengeluarkan direktori tertentu berdasarkan indeks:**

   ```bash
   popd +1
   ```

3. **Mengeluarkan direktori tanpa mengubah direktori semasa:**

   ```bash
   popd -n
   ```

## Tips
- Pastikan anda telah menggunakan `pushd` untuk menyimpan direktori sebelum menggunakan `popd`.
- Gunakan `dirs` untuk melihat senarai direktori dalam tumpukan sebelum mengeluarkannya.
- Jika anda sering beralih antara beberapa direktori, pertimbangkan untuk menggunakan `pushd` dan `popd` secara berpasangan untuk navigasi yang lebih efisien.