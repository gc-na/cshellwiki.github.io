# [Linux] Bash set penggunaan: Mengubah parameter shell

## Overview
Perintah `set` dalam Bash digunakan untuk mengubah atau menetapkan parameter dan pilihan shell. Ia membolehkan pengguna untuk mengawal tingkah laku shell dengan menetapkan pelbagai pilihan yang mempengaruhi cara skrip dan perintah dijalankan.

## Usage
Berikut adalah sintaks asas untuk perintah `set`:

```bash
set [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan `set`:

- `-e`: Menghentikan skrip apabila terdapat perintah yang gagal.
- `-u`: Mengeluarkan ralat apabila terdapat penggunaan pembolehubah yang tidak ditetapkan.
- `-x`: Menunjukkan perintah yang sedang dijalankan dengan menggandakan setiap perintah sebelum ia dilaksanakan.
- `-o`: Mengubah pilihan shell yang tertentu, seperti `-o noclobber` untuk mengelakkan penulisan fail yang sedia ada.

## Common Examples

1. **Menghentikan skrip pada ralat:**
   ```bash
   set -e
   command1
   command2  # Jika command1 gagal, command2 tidak akan dijalankan.
   ```

2. **Mengeluarkan ralat untuk pembolehubah tidak ditetapkan:**
   ```bash
   set -u
   echo $undefined_variable  # Ini akan mengeluarkan ralat.
   ```

3. **Menunjukkan perintah yang sedang dijalankan:**
   ```bash
   set -x
   echo "Hello, World!"  # Akan menunjukkan perintah ini sebelum ia dijalankan.
   ```

4. **Mengelakkan penulisan fail yang sedia ada:**
   ```bash
   set -o noclobber
   echo "Data" > file.txt  # Ini akan gagal jika file.txt sudah wujud.
   ```

## Tips
- Gunakan `set -e` untuk memastikan skrip anda tidak meneruskan jika terdapat sebarang kesilapan.
- Sentiasa gunakan `set -u` untuk mengelakkan ralat yang sukar dikesan akibat pembolehubah yang tidak ditetapkan.
- Untuk debugging, `set -x` sangat berguna untuk melihat urutan pelaksanaan perintah dalam skrip anda.