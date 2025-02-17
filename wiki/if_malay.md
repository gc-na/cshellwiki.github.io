# [Linux] Bash if: Memeriksa syarat

## Overview
Perintah `if` dalam Bash digunakan untuk membuat keputusan berdasarkan syarat yang ditentukan. Ia membolehkan pengguna untuk menjalankan arahan tertentu jika syarat yang diberikan adalah benar.

## Usage
Sintaks asas untuk perintah `if` adalah seperti berikut:

```bash
if [ syarat ]; then
    arahan
fi
```

## Common Options
- `-e`: Memeriksa jika fail wujud.
- `-d`: Memeriksa jika direktori wujud.
- `-f`: Memeriksa jika fail adalah fail biasa.
- `-z`: Memeriksa jika panjang rentetan adalah kosong.
- `-n`: Memeriksa jika panjang rentetan tidak kosong.

## Common Examples

1. **Memeriksa jika fail wujud:**
   ```bash
   if [ -e fail.txt ]; then
       echo "Fail wujud."
   else
       echo "Fail tidak wujud."
   fi
   ```

2. **Memeriksa jika direktori wujud:**
   ```bash
   if [ -d /home/user ]; then
       echo "Direktori wujud."
   else
       echo "Direktori tidak wujud."
   fi
   ```

3. **Memeriksa jika rentetan tidak kosong:**
   ```bash
   my_string="Hello"
   if [ -n "$my_string" ]; then
       echo "Rentetan tidak kosong."
   else
       echo "Rentetan kosong."
   fi
   ```

4. **Menggunakan syarat berganda:**
   ```bash
   if [ -f fail.txt ] && [ -r fail.txt ]; then
       echo "Fail wujud dan boleh dibaca."
   else
       echo "Fail tidak wujud atau tidak boleh dibaca."
   fi
   ```

## Tips
- Sentiasa gunakan ruang kosong di sekitar tanda kurung untuk mengelakkan ralat sintaks.
- Gunakan `elif` untuk menambah lebih banyak syarat dalam pernyataan `if`.
- Pastikan untuk menutup pernyataan `if` dengan `fi` untuk mengelakkan ralat dalam skrip.