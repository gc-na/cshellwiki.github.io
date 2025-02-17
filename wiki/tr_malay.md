# [Linux] Bash tr Penggunaan: Menukar dan menghapus karakter

## Overview
Perintah `tr` dalam Bash digunakan untuk menukar atau menghapus karakter dalam input. Ia sangat berguna untuk memanipulasi teks dalam skrip dan baris perintah.

## Usage
Sintaks asas untuk menggunakan perintah `tr` adalah seperti berikut:

```bash
tr [options] [arguments]
```

## Common Options
- `-d`: Menghapus karakter yang ditentukan.
- `-s`: Mengganti urutan karakter berulang dengan satu karakter.
- `-c`: Mengambil semua karakter yang tidak termasuk dalam set yang ditentukan.

## Common Examples

1. **Menukar huruf kecil ke huruf besar:**
   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```
   Output: `HELLO WORLD`

2. **Menghapus semua angka dari teks:**
   ```bash
   echo "abc123def456" | tr -d '0-9'
   ```
   Output: `abcdef`

3. **Mengganti urutan spasi berulang dengan satu spasi:**
   ```bash
   echo "This    is    a    test." | tr -s ' '
   ```
   Output: `This is a test.`

4. **Mengambil semua karakter bukan huruf:**
   ```bash
   echo "Hello, World! 123" | tr -c 'A-Za-z\n' ' '
   ```
   Output: `Hello World`

## Tips
- Gunakan `tr` bersama dengan perintah lain seperti `grep` atau `awk` untuk pemprosesan teks yang lebih kompleks.
- Pastikan untuk menguji perintah `tr` dengan input yang berbeza untuk memahami bagaimana ia berfungsi sebelum menggunakannya dalam skrip yang lebih besar.
- Ingat bahawa `tr` tidak membaca dari fail secara langsung; anda perlu menggunakan input dari stdin atau mengalihkan fail ke dalamnya.