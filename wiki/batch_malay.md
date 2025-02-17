# [Linux] Bash batch penggunaan: Menjadwalkan tugas untuk dijalankan kemudian

## Overview
Perintah `batch` dalam Bash digunakan untuk menjadwalkan tugas yang akan dijalankan secara automatik pada waktu yang tidak sibuk. Tugas ini akan dilaksanakan setelah beban sistem menurun, biasanya ketika sistem tidak digunakan oleh pengguna lain.

## Usage
Sintaks asas untuk perintah `batch` adalah seperti berikut:

```
batch [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk perintah `batch`:

- `-l` : Menunjukkan waktu dan tarikh untuk tugas yang dijadwalkan.
- `-q` : Menghantar output ke `/dev/null` untuk mengabaikan hasil.
- `-n` : Menentukan jumlah maksimum proses yang boleh dijadwalkan.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `batch`:

1. **Menjadwalkan skrip untuk dijalankan**:
   ```bash
   batch < my_script.sh
   ```

2. **Menjadwalkan beberapa perintah**:
   ```bash
   echo "echo Hello, World!" | batch
   ```

3. **Menjadwalkan perintah dengan output ke fail**:
   ```bash
   echo "date" | batch > output.txt
   ```

4. **Menjadwalkan perintah dengan pilihan untuk mengabaikan output**:
   ```bash
   echo "ls -l" | batch -q
   ```

## Tips
- Pastikan untuk memeriksa beban sistem sebelum menggunakan `batch` untuk memastikan tugas anda dijadwalkan dengan baik.
- Gunakan `atq` untuk menyemak senarai tugas yang telah dijadwalkan.
- Jika anda ingin menjalankan tugas pada waktu tertentu, pertimbangkan untuk menggunakan perintah `at` yang lebih spesifik.