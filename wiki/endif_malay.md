# [Linux] Bash endif: Mengakhiri blok kondisional

## Overview
Perintah `endif` dalam Bash digunakan untuk menandakan akhir dari blok kondisional yang dimulai dengan perintah `if`. Ia membantu dalam mengatur aliran logik dalam skrip Bash, memastikan bahawa kod yang berkaitan dengan kondisi tertentu hanya dijalankan apabila syarat yang ditetapkan dipenuhi.

## Usage
Berikut adalah sintaks asas untuk perintah `endif`:

```bash
endif
```

## Common Options
Perintah `endif` tidak mempunyai pilihan khusus kerana ia hanya digunakan untuk menandakan akhir blok `if`. Namun, ia perlu digunakan dalam konteks yang tepat bersama dengan perintah `if` dan `then`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `endif` dalam skrip Bash:

### Contoh 1: Menggunakan `if` dan `endif`
```bash
if [ -f "fail.txt" ]; then
    echo "Fail wujud."
endif
```

### Contoh 2: Menggunakan `if` dengan `else` dan `endif`
```bash
if [ -f "fail.txt" ]; then
    echo "Fail wujud."
else
    echo "Fail tidak wujud."
endif
```

### Contoh 3: Menggunakan `if` dengan `elif` dan `endif`
```bash
if [ -f "fail.txt" ]; then
    echo "Fail wujud."
elif [ -d "folder" ]; then
    echo "Folder wujud."
endif
```

## Tips
- Pastikan untuk selalu menggunakan `endif` untuk menandakan akhir blok `if` agar skrip anda lebih teratur dan mudah dibaca.
- Gunakan indentasi yang konsisten untuk meningkatkan keterbacaan skrip, terutama ketika menggunakan blok bersarang.
- Sentiasa periksa sintaks anda untuk memastikan bahawa semua perintah kondisional ditutup dengan betul menggunakan `endif`.