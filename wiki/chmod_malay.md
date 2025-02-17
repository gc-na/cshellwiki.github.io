# [Linux] Bash chmod Penggunaan: Mengubah kebenaran fail

## Overview
Perintah `chmod` digunakan untuk mengubah kebenaran akses kepada fail dan direktori dalam sistem operasi Linux. Ia membolehkan pengguna menetapkan siapa yang boleh membaca, menulis, atau melaksanakan fail tertentu.

## Usage
Sintaks asas bagi perintah `chmod` adalah seperti berikut:

```bash
chmod [options] [arguments]
```

## Common Options
- `+` : Menambah kebenaran.
- `-` : Mengurangkan kebenaran.
- `=` : Menetapkan kebenaran yang tepat.
- `u` : Pemilik fail (user).
- `g` : Kumpulan pemilik fail (group).
- `o` : Lain-lain pengguna (others).
- `a` : Semua pengguna (all).

## Common Examples
1. **Menambah kebenaran baca untuk semua pengguna:**
   ```bash
   chmod a+r fail.txt
   ```

2. **Mengurangkan kebenaran tulis untuk pemilik fail:**
   ```bash
   chmod u-w fail.txt
   ```

3. **Menetapkan kebenaran baca dan laksana untuk kumpulan:**
   ```bash
   chmod g=rx fail.txt
   ```

4. **Menambah kebenaran laksana untuk semua pengguna:**
   ```bash
   chmod a+x skrip.sh
   ```

5. **Memberikan kebenaran penuh kepada pemilik dan mengurangkan kebenaran kepada lain-lain:**
   ```bash
   chmod u=rwx,go= fail.txt
   ```

## Tips
- Sentiasa semak kebenaran fail selepas menggunakan `chmod` dengan perintah `ls -l`.
- Gunakan `chmod` dengan berhati-hati, terutamanya pada fail sistem penting.
- Untuk mengelakkan kesilapan, gunakan mod numerik (contoh: `chmod 755 fail.txt`) jika anda lebih selesa dengan nombor.