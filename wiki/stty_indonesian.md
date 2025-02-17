# [Linux] Bash stty Penggunaan: Mengatur dan menampilkan atribut terminal

## Overview
Perintah `stty` digunakan untuk mengatur dan menampilkan atribut terminal di sistem Unix dan Linux. Dengan `stty`, pengguna dapat mengubah pengaturan input dan output terminal, seperti karakter kontrol, pengaturan echo, dan banyak lagi.

## Usage
Sintaks dasar dari perintah `stty` adalah sebagai berikut:

```
stty [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `stty`:

- `-a`: Menampilkan semua pengaturan terminal saat ini.
- `-g`: Menghasilkan pengaturan terminal dalam format yang dapat digunakan kembali.
- `erase <char>`: Mengatur karakter penghapus (default biasanya adalah backspace).
- `kill <char>`: Mengatur karakter untuk menghapus seluruh baris (default biasanya adalah Ctrl+U).
- `echo`: Mengaktifkan echo input di terminal.
- `-echo`: Menonaktifkan echo input di terminal.

## Common Examples

1. **Menampilkan semua pengaturan terminal saat ini:**
   ```bash
   stty -a
   ```

2. **Mengatur karakter penghapus menjadi Ctrl+H:**
   ```bash
   stty erase ^H
   ```

3. **Menonaktifkan echo input:**
   ```bash
   stty -echo
   ```

4. **Mengaktifkan echo input kembali:**
   ```bash
   stty echo
   ```

5. **Menyimpan pengaturan terminal saat ini ke dalam variabel:**
   ```bash
   settings=$(stty -g)
   ```

## Tips
- Selalu periksa pengaturan terminal saat ini dengan `stty -a` sebelum melakukan perubahan untuk menghindari kebingungan.
- Jika Anda ingin mengembalikan pengaturan terminal ke keadaan semula setelah melakukan perubahan, simpan pengaturan awal menggunakan `stty -g`.
- Gunakan `stty` dengan hati-hati, terutama saat menonaktifkan echo, karena Anda mungkin tidak dapat melihat input yang Anda ketik.