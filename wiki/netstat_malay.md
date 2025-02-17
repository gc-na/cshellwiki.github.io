# [Linux] Bash netstat Penggunaan: Menunjukkan sambungan rangkaian

## Overview
Perintah `netstat` digunakan untuk memaparkan statistik rangkaian dan sambungan rangkaian yang aktif pada sistem. Ia memberikan maklumat tentang sambungan TCP/IP, pengendali yang mendengar, dan statistik protokol.

## Usage
Sintaks asas untuk menggunakan `netstat` adalah seperti berikut:
```
netstat [options] [arguments]
```

## Common Options
- `-a`: Menunjukkan semua sambungan dan pengendali yang mendengar.
- `-t`: Menunjukkan sambungan TCP sahaja.
- `-u`: Menunjukkan sambungan UDP sahaja.
- `-n`: Menunjukkan alamat IP dan nombor port dalam format numerik.
- `-l`: Menunjukkan hanya pengendali yang mendengar.
- `-p`: Menunjukkan proses yang menggunakan sambungan tersebut.

## Common Examples
Berikut adalah beberapa contoh penggunaan `netstat`:

1. **Menunjukkan semua sambungan dan pengendali yang mendengar:**
   ```bash
   netstat -a
   ```

2. **Menunjukkan sambungan TCP sahaja:**
   ```bash
   netstat -t
   ```

3. **Menunjukkan sambungan UDP sahaja:**
   ```bash
   netstat -u
   ```

4. **Menunjukkan sambungan dengan alamat IP dan nombor port dalam format numerik:**
   ```bash
   netstat -n
   ```

5. **Menunjukkan pengendali yang mendengar sahaja:**
   ```bash
   netstat -l
   ```

6. **Menunjukkan sambungan berserta proses yang menggunakannya:**
   ```bash
   netstat -p
   ```

## Tips
- Gunakan `netstat -tuln` untuk mendapatkan gambaran lengkap tentang sambungan TCP dan UDP yang mendengar tanpa nama host.
- Kombinasi pilihan seperti `netstat -tulnp` boleh memberikan maklumat yang lebih terperinci tentang sambungan dan proses.
- Untuk maklumat lebih terkini, pertimbangkan untuk menggunakan `ss`, yang merupakan alat yang lebih moden dan lebih cepat daripada `netstat`.