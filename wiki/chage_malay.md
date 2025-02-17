# [Linux] Bash chage Penggunaan: Mengurus tempoh sah kata laluan pengguna

## Overview
Perintah `chage` digunakan untuk mengubah dan mengurus tempoh sah kata laluan bagi pengguna dalam sistem Linux. Dengan `chage`, anda boleh menetapkan bila kata laluan perlu ditukar dan mengawal pelbagai aspek lain berkaitan keselamatan kata laluan.

## Usage
Berikut adalah sintaks asas untuk perintah `chage`:

```bash
chage [options] [arguments]
```

## Common Options
- `-l, --list`: Menunjukkan maklumat tempoh sah kata laluan untuk pengguna tertentu.
- `-m, --mindays`: Menetapkan bilangan hari minimum antara perubahan kata laluan.
- `-M, --maxdays`: Menetapkan bilangan hari maksimum sebelum kata laluan perlu ditukar.
- `-I, --inactive`: Menetapkan bilangan hari selepas kata laluan tamat tempoh sebelum akaun dinyahaktifkan.
- `-E, --expiredate`: Menetapkan tarikh tamat untuk akaun pengguna.

## Common Examples
1. **Menunjukkan maklumat kata laluan pengguna:**
   ```bash
   chage -l username
   ```

2. **Menetapkan kata laluan perlu ditukar setiap 30 hari:**
   ```bash
   chage -M 30 username
   ```

3. **Menetapkan kata laluan tidak boleh ditukar selama 7 hari selepas ditetapkan:**
   ```bash
   chage -m 7 username
   ```

4. **Menetapkan tarikh tamat untuk akaun pengguna:**
   ```bash
   chage -E 2024-12-31 username
   ```

5. **Menetapkan kata laluan untuk tidak aktif selepas 15 hari tamat:**
   ```bash
   chage -I 15 username
   ```

## Tips
- Sentiasa semak maklumat kata laluan pengguna dengan `chage -l` sebelum membuat perubahan.
- Gunakan pilihan `-M` dan `-m` secara bijak untuk memastikan keselamatan tanpa mengganggu pengguna.
- Pastikan untuk mengingat tarikh tamat yang ditetapkan untuk mengelakkan akaun pengguna terputus akses secara tidak sengaja.