# [Linux] Bash w Penggunaan: Menunjukkan pengguna yang sedang log masuk

## Overview
Perintah `w` dalam Bash digunakan untuk menunjukkan pengguna yang sedang log masuk ke sistem serta aktiviti mereka. Ia memberikan maklumat tentang siapa yang sedang menggunakan sistem, dari mana mereka log masuk, dan apa yang mereka lakukan.

## Usage
Sintaks asas untuk menggunakan perintah `w` adalah seperti berikut:

```
w [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk perintah `w`:

- `-h`: Mengabaikan baris header dalam output.
- `-s`: Menunjukkan output yang lebih ringkas.
- `-f`: Menunjukkan nama fail dari mana pengguna log masuk.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `w`:

1. **Menunjukkan semua pengguna yang sedang log masuk:**
   ```
   w
   ```

2. **Menunjukkan pengguna dengan output ringkas:**
   ```
   w -s
   ```

3. **Menunjukkan pengguna tanpa baris header:**
   ```
   w -h
   ```

4. **Menunjukkan pengguna dengan nama fail log masuk:**
   ```
   w -f
   ```

## Tips
- Gunakan `w` secara berkala untuk memantau aktiviti pengguna di sistem anda.
- Kombinasikan `w` dengan perintah lain seperti `grep` untuk mencari pengguna tertentu.
- Perhatikan waktu yang ditunjukkan dalam output untuk memahami berapa lama pengguna telah log masuk.