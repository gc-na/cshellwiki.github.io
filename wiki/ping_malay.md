# [Linux] Bash ping Penggunaan: Menguji sambungan rangkaian

## Overview
Perintah `ping` digunakan untuk menguji sambungan rangkaian antara komputer anda dan host lain di internet atau rangkaian tempatan. Ia menghantar paket ICMP Echo Request dan menunggu balasan ICMP Echo Reply, membolehkan pengguna menilai keupayaan sambungan dan masa respons.

## Usage
Sintaks asas untuk perintah `ping` adalah seperti berikut:
```
ping [options] [arguments]
```

## Common Options
- `-c [count]`: Menentukan jumlah paket yang akan dihantar.
- `-i [interval]`: Menetapkan selang masa antara paket yang dihantar, dalam saat.
- `-s [size]`: Menentukan saiz paket yang dihantar.
- `-t [ttl]`: Menetapkan nilai Time To Live untuk paket.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ping`:

1. **Menghantar paket ke alamat IP tertentu:**
   ```bash
   ping 8.8.8.8
   ```

2. **Menghantar 4 paket ke host tertentu:**
   ```bash
   ping -c 4 google.com
   ```

3. **Menghantar paket dengan saiz tertentu:**
   ```bash
   ping -s 100 google.com
   ```

4. **Menghantar paket dengan selang masa 2 saat antara setiap paket:**
   ```bash
   ping -i 2 google.com
   ```

## Tips
- Gunakan pilihan `-c` untuk menghentikan ping secara automatik selepas menghantar jumlah paket yang ditetapkan.
- Untuk menguji sambungan rangkaian secara berterusan, gunakan `ping` tanpa pilihan `-c`.
- Perhatikan masa respons yang ditunjukkan untuk menilai kualiti sambungan rangkaian.