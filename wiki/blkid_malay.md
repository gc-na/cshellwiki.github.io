# [Linux] Bash blkid Penggunaan: Menyenaraikan UUID dan jenis sistem fail

## Overview
Perintah `blkid` digunakan untuk mengenal pasti dan menyenaraikan UUID (Universally Unique Identifier) dan jenis sistem fail bagi peranti penyimpanan yang disambungkan ke sistem Linux. Ia membantu pengguna untuk mendapatkan maklumat penting tentang peranti penyimpanan tanpa perlu memasang atau mengakses sistem fail secara langsung.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `blkid`:

```
blkid [options] [arguments]
```

## Common Options
- `-o, --output`: Menentukan format output (contohnya, `value`, `full`, `list`).
- `-s, --match-tag`: Menyaring output berdasarkan tag tertentu (contohnya, `UUID`, `TYPE`).
- `-p, --probe`: Melakukan pengesanan pada peranti yang ditentukan.
- `-c, --cache`: Menggunakan cache untuk mempercepatkan proses pengenalan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `blkid`:

1. **Menyenaraikan semua peranti penyimpanan**:
   ```bash
   blkid
   ```

2. **Mendapatkan UUID bagi peranti tertentu**:
   ```bash
   blkid /dev/sda1
   ```

3. **Menunjukkan output dalam format nilai**:
   ```bash
   blkid -o value -s UUID /dev/sda1
   ```

4. **Menyaring output untuk menunjukkan hanya jenis sistem fail**:
   ```bash
   blkid -s TYPE
   ```

5. **Menggunakan cache untuk mempercepatkan proses**:
   ```bash
   blkid -c /etc/blkid.tab
   ```

## Tips
- Sentiasa gunakan `blkid` dengan hak akses yang mencukupi (seperti `sudo`) untuk mendapatkan maklumat lengkap tentang peranti penyimpanan.
- Gunakan pilihan `-o` untuk mengubah format output mengikut keperluan anda.
- Jika anda sering menggunakan `blkid`, pertimbangkan untuk menyimpan hasil dalam fail untuk rujukan masa depan.