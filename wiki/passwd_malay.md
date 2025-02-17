# [Linux] Bash passwd Penggunaan: Mengubah kata laluan pengguna

## Overview
Perintah `passwd` digunakan untuk mengubah kata laluan pengguna dalam sistem Linux. Ia membolehkan pengguna menukar kata laluan mereka sendiri atau pentadbir menukar kata laluan untuk pengguna lain.

## Usage
Sintaks asas untuk perintah `passwd` adalah seperti berikut:

```
passwd [options] [username]
```

## Common Options
- `-d`: Hapuskan kata laluan pengguna, membolehkan akses tanpa kata laluan.
- `-l`: Kunci akaun pengguna, menjadikannya tidak dapat digunakan.
- `-u`: Buka kunci akaun pengguna yang telah dikunci.
- `-e`: Paksa pengguna untuk menukar kata laluan mereka pada log masuk seterusnya.

## Common Examples
1. **Menukar kata laluan pengguna semasa:**
   ```bash
   passwd
   ```

2. **Menukar kata laluan untuk pengguna tertentu:**
   ```bash
   passwd username
   ```

3. **Menghapuskan kata laluan pengguna:**
   ```bash
   passwd -d username
   ```

4. **Mengunci akaun pengguna:**
   ```bash
   passwd -l username
   ```

5. **Membuka kunci akaun pengguna:**
   ```bash
   passwd -u username
   ```

6. **Memaksa pengguna untuk menukar kata laluan pada log masuk seterusnya:**
   ```bash
   passwd -e username
   ```

## Tips
- Sentiasa gunakan kata laluan yang kuat dan sukar diteka untuk meningkatkan keselamatan.
- Jika anda adalah pentadbir, pastikan untuk memberi amaran kepada pengguna sebelum mengunci atau menghapuskan kata laluan mereka.
- Gunakan pilihan `-e` untuk memastikan pengguna menukar kata laluan mereka secara berkala.