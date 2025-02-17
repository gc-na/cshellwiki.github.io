# [Linux] Pengguna Bash: Mengurus pengguna sistem

## Overview
Perintah `users` digunakan untuk menunjukkan nama pengguna yang sedang log masuk ke sistem. Ia memberikan senarai ringkas pengguna yang aktif pada masa tertentu.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `users`:

```bash
users [options]
```

## Common Options
- `-n`: Menunjukkan nama pengguna tanpa duplikasi.
- `-r`: Menunjukkan pengguna yang sedang log masuk sebagai pengguna biasa sahaja.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `users`:

1. **Menunjukkan semua pengguna yang sedang log masuk:**
   ```bash
   users
   ```

2. **Menunjukkan nama pengguna tanpa duplikasi:**
   ```bash
   users -n
   ```

3. **Menunjukkan pengguna biasa sahaja:**
   ```bash
   users -r
   ```

## Tips
- Gunakan `users` bersama perintah lain seperti `who` untuk mendapatkan maklumat lebih terperinci tentang sesi pengguna.
- Perintah ini berguna untuk pemantauan sistem, terutamanya dalam persekitaran pelayan.