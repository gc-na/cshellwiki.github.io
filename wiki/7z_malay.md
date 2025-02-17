# [Linux] Bash 7z Penggunaan: Mengurus fail arkib

## Overview
Perintah `7z` adalah alat pengurusan arkib yang digunakan untuk memampatkan dan mengekstrak fail. Ia menyokong pelbagai format arkib seperti 7z, ZIP, RAR, dan banyak lagi, menjadikannya pilihan yang popular untuk pengguna yang memerlukan pengurusan fail yang berkesan.

## Usage
Sintaks asas untuk menggunakan perintah `7z` adalah seperti berikut:

```
7z [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `7z`:

- `a`: Menambah fail ke dalam arkib.
- `x`: Mengekstrak fail dari arkib.
- `l`: Menyenaraikan kandungan arkib.
- `d`: Menghapuskan fail dari arkib.
- `t`: Menguji integriti arkib.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `7z`:

1. **Mampatkan fail ke dalam arkib 7z:**
   ```bash
   7z a fail.7z fail1.txt fail2.txt
   ```

2. **Mengekstrak semua fail dari arkib 7z:**
   ```bash
   7z x fail.7z
   ```

3. **Menyenaraikan kandungan arkib:**
   ```bash
   7z l fail.7z
   ```

4. **Menghapuskan fail dari arkib:**
   ```bash
   7z d fail.7z fail1.txt
   ```

5. **Menguji integriti arkib:**
   ```bash
   7z t fail.7z
   ```

## Tips
- Sentiasa gunakan pilihan `l` untuk menyemak kandungan arkib sebelum mengekstrak untuk memastikan anda tahu apa yang akan diekstrak.
- Untuk memampatkan fail dengan kadar mampatan yang lebih tinggi, anda boleh menggunakan pilihan `-mx=9` seperti berikut:
  ```bash
  7z a -mx=9 fail.7z fail1.txt
  ```
- Pastikan anda mempunyai ruang yang cukup pada pemacu anda sebelum mengekstrak arkib yang besar.