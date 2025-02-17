# [Linux] Bash test penggunaan: Memeriksa ekspresi

## Overview
Perintah `test` dalam Bash digunakan untuk mengevaluasi ekspresi dan mengembalikan nilai benar (true) atau salah (false). Ia sering digunakan dalam skrip untuk membuat keputusan berdasarkan kondisi tertentu.

## Usage
Sintaks asas untuk perintah `test` adalah seperti berikut:

```bash
test [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk perintah `test`:

- `-e [file]`: Memeriksa jika fail wujud.
- `-d [directory]`: Memeriksa jika direktori wujud.
- `-f [file]`: Memeriksa jika fail adalah fail biasa.
- `-z [string]`: Memeriksa jika panjang string adalah kosong.
- `-n [string]`: Memeriksa jika panjang string tidak kosong.
- `[string1] = [string2]`: Memeriksa jika dua string adalah sama.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `test`:

1. Memeriksa jika fail wujud:
    ```bash
    test -e myfile.txt && echo "Fail wujud"
    ```

2. Memeriksa jika direktori wujud:
    ```bash
    test -d mydirectory && echo "Direktori wujud"
    ```

3. Memeriksa jika fail adalah fail biasa:
    ```bash
    test -f myscript.sh && echo "Ini adalah fail biasa"
    ```

4. Memeriksa jika string kosong:
    ```bash
    mystring=""
    test -z "$mystring" && echo "String adalah kosong"
    ```

5. Memeriksa jika dua string adalah sama:
    ```bash
    test "hello" = "hello" && echo "String adalah sama"
    ```

## Tips
- Gunakan `[` sebagai alternatif untuk `test`, contohnya: `[ -e myfile.txt ]`.
- Selalu gunakan tanda kutip untuk string untuk mengelakkan masalah dengan ruang kosong.
- Gabungkan beberapa pernyataan menggunakan `&&` atau `||` untuk membuat keputusan yang lebih kompleks.