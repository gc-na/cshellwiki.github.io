# [Linux] Bash exec penggunaan: Menjalankan perintah dalam konteks shell

## Overview
Perintah `exec` dalam Bash digunakan untuk menggantikan proses shell semasa dengan perintah baru. Ini bermakna apabila anda menggunakan `exec`, shell yang sedang berjalan akan ditukar kepada perintah yang anda nyatakan, dan tidak akan kembali ke shell asal setelah perintah tersebut selesai.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `exec`:

```
exec [options] [arguments]
```

## Common Options
- `-a` : Menetapkan nama yang berbeza untuk perintah yang dijalankan.
- `-l` : Menjalankan perintah dalam mod login.
- `-c` : Menjalankan perintah dalam konteks baru tanpa mengwarisi persekitaran semasa.

## Common Examples

1. **Menjalankan perintah baru tanpa kembali ke shell asal:**
   ```bash
   exec ls -l
   ```
   Dalam contoh ini, perintah `ls -l` akan dijalankan dan shell asal akan digantikan oleh output perintah tersebut.

2. **Menggunakan exec untuk menjalankan skrip:**
   ```bash
   exec ./myscript.sh
   ```
   Skrip `myscript.sh` akan dijalankan dan shell semasa akan ditukar kepada skrip tersebut.

3. **Menetapkan nama perintah yang berbeza:**
   ```bash
   exec -a mycustomname /bin/bash
   ```
   Dalam contoh ini, perintah `/bin/bash` akan dijalankan dengan nama `mycustomname`.

## Tips
- Gunakan `exec` apabila anda ingin menjalankan perintah yang tidak perlu kembali ke shell asal, seperti dalam skrip yang memerlukan penggantian proses.
- Pastikan anda memahami bahawa setelah menggunakan `exec`, shell semasa tidak akan kembali. Ini berguna untuk mengelakkan penggunaan sumber yang tidak perlu.
- Jika anda ingin mengekalkan shell asal, pertimbangkan untuk menggunakan perintah lain seperti `bash` atau `sh` tanpa `exec`.