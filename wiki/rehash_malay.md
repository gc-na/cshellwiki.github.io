# [Linux] Bash rehash Penggunaan: Mengemas kini cache perintah

## Overview
Perintah `rehash` dalam Bash digunakan untuk mengemas kini cache perintah yang disimpan. Ini berguna apabila anda telah menambah atau mengubah suai skrip atau program dalam direktori yang ada dalam `PATH`, dan anda ingin memastikan bahawa shell anda mengenali perubahan tersebut tanpa perlu memulakan semula sesi shell.

## Usage
Sintaks asas untuk perintah `rehash` adalah seperti berikut:

```
rehash [options] [arguments]
```

## Common Options
- Tiada pilihan khusus yang biasa digunakan dengan `rehash`. Perintah ini biasanya dijalankan tanpa sebarang pilihan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `rehash`:

### Contoh 1: Mengemas kini cache secara langsung
```bash
rehash
```
Perintah ini akan mengemas kini cache perintah untuk sesi shell semasa.

### Contoh 2: Menggunakan selepas menambah skrip baru
Jika anda telah menambah skrip baru ke dalam direktori yang ada dalam `PATH`, jalankan:
```bash
rehash
```
Ini memastikan bahawa skrip baru tersebut dapat dijalankan tanpa perlu memulakan semula sesi shell.

## Tips
- Gunakan `rehash` selepas anda menambah atau mengubah suai skrip dalam direktori `PATH` untuk memastikan perubahan dikenali.
- Perintah `rehash` tidak memerlukan sebarang pilihan, jadi ia mudah dan cepat untuk digunakan.
- Jika anda menggunakan shell lain seperti `zsh`, perintah ini mungkin berfungsi dengan cara yang sama tetapi dengan beberapa perbezaan dalam konteks penggunaannya.