# [Sistem Operasi] C Shell (csh) pengguna: Mengelola pengguna sistem

## Overview
Perintah `users` dalam C Shell (csh) digunakan untuk menampilkan nama-nama pengguna yang sedang aktif di sistem. Ini berguna untuk mengetahui siapa saja yang sedang login pada saat tertentu.

## Usage
Berikut adalah sintaks dasar dari perintah `users`:

```csh
users [options] [arguments]
```

## Common Options
- `-n`: Menampilkan nama pengguna tanpa duplikasi.
- `-r`: Menampilkan pengguna yang sedang aktif secara real-time.

## Common Examples

1. **Menampilkan pengguna aktif:**
   ```csh
   users
   ```

2. **Menampilkan pengguna aktif tanpa duplikasi:**
   ```csh
   users -n
   ```

3. **Menampilkan pengguna aktif secara real-time:**
   ```csh
   users -r
   ```

## Tips
- Gunakan opsi `-n` jika Anda ingin mendapatkan daftar pengguna yang unik, terutama jika beberapa pengguna login lebih dari sekali.
- Perintah ini dapat digunakan dalam skrip untuk memantau aktivitas pengguna di sistem secara otomatis.