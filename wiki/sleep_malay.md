# [Linux] Bash sleep Penggunaan: Menangguhkan proses untuk tempoh tertentu

## Overview
Perintah `sleep` dalam Bash digunakan untuk menangguhkan atau menghentikan pelaksanaan skrip atau perintah untuk tempoh masa yang ditentukan. Ini berguna dalam pelbagai situasi, seperti memberi masa untuk proses lain selesai atau mengatur jadual pelaksanaan.

## Usage
Sintaks asas untuk perintah `sleep` adalah seperti berikut:

```bash
sleep [options] [arguments]
```

## Common Options
- `-s`, `--seconds`: Menentukan tempoh dalam saat. Ini adalah pilihan lalai.
- `-m`, `--minutes`: Menentukan tempoh dalam minit.
- `-h`, `--hours`: Menentukan tempoh dalam jam.
- `-d`, `--days`: Menentukan tempoh dalam hari.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `sleep`:

1. **Menangguhkan selama 5 saat:**
   ```bash
   sleep 5
   ```

2. **Menangguhkan selama 2 minit:**
   ```bash
   sleep 2m
   ```

3. **Menangguhkan selama 1 jam:**
   ```bash
   sleep 1h
   ```

4. **Menangguhkan selama 3 hari:**
   ```bash
   sleep 3d
   ```

5. **Menggunakan sleep dalam skrip:**
   ```bash
   echo "Proses bermula..."
   sleep 10
   echo "Proses selesai selepas 10 saat."
   ```

## Tips
- Gunakan `sleep` untuk mengelakkan penggunaan sumber yang berlebihan dalam skrip yang berjalan berulang kali.
- Pertimbangkan untuk menggunakan `sleep` dalam pengujian automatik untuk memberi masa bagi elemen yang dimuatkan.
- Jangan gunakan tempoh yang terlalu panjang tanpa keperluan, kerana ini boleh melambatkan keseluruhan proses.