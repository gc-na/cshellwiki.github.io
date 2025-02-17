# [Linux] Bash strace Penggunaan: Mengesan panggilan sistem dan isyarat

## Overview
Perintah `strace` digunakan untuk mengesan dan menganalisis panggilan sistem yang dilakukan oleh program di Linux. Ia membolehkan pengguna melihat interaksi antara aplikasi dan kernel, membantu dalam pengesanan masalah dan pemahaman tingkah laku program.

## Usage
Berikut adalah sintaks asas untuk menggunakan `strace`:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: Mengira statistik panggilan sistem dan memaparkan ringkasan.
- `-e`: Menentukan jenis panggilan sistem yang ingin dikesan.
- `-p`: Menyambung ke proses yang sedang berjalan menggunakan PID.
- `-o <file>`: Menyimpan output ke dalam fail yang ditentukan.
- `-f`: Mengesan proses kanak-kanak yang dicipta oleh proses utama.

## Common Examples
Berikut adalah beberapa contoh penggunaan `strace`:

1. **Mengesan panggilan sistem untuk program tertentu:**

   ```bash
   strace ls
   ```

2. **Menyimpan output ke dalam fail:**

   ```bash
   strace -o output.txt ls
   ```

3. **Mengira statistik panggilan sistem:**

   ```bash
   strace -c ls
   ```

4. **Menyambung ke proses yang sedang berjalan:**

   ```bash
   strace -p 1234
   ```

5. **Menggunakan pilihan untuk hanya mengesan panggilan sistem tertentu:**

   ```bash
   strace -e trace=open,close ls
   ```

## Tips
- Gunakan `-o` untuk menyimpan output ke dalam fail bagi analisis yang lebih mendalam.
- Pilih pilihan `-c` untuk mendapatkan ringkasan statistik yang berguna jika anda ingin melihat prestasi panggilan sistem.
- Sentiasa semak proses yang sedang berjalan dengan `ps` sebelum menggunakan pilihan `-p` untuk memastikan anda menyambung ke proses yang betul.
- Gunakan `-f` jika anda ingin mengesan proses kanak-kanak yang dicipta oleh proses utama.