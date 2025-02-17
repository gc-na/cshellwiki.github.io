# [Linux] Bash unset Penggunaan: Menghapus pembolehubah

## Overview
Perintah `unset` dalam Bash digunakan untuk menghapus pembolehubah atau fungsi yang telah ditetapkan. Ini berguna untuk mengurus ruang memori dan memastikan bahawa pembolehubah yang tidak diperlukan tidak lagi wujud dalam sesi semasa.

## Usage
Sintaks asas untuk perintah `unset` adalah seperti berikut:

```bash
unset [options] [arguments]
```

## Common Options
- `-f`: Menghapus fungsi yang ditetapkan.
- `-v`: Menghapus pembolehubah yang ditetapkan.

## Common Examples

### Menghapus Pembolehubah
Untuk menghapus pembolehubah yang bernama `VAR`, anda boleh menggunakan perintah berikut:

```bash
VAR="Hello, World!"
unset VAR
```

### Menghapus Fungsi
Jika anda mempunyai fungsi yang ditetapkan dan ingin menghapuskannya, contohnya fungsi `myFunction`, gunakan:

```bash
myFunction() {
    echo "This is my function."
}
unset -f myFunction
```

### Menghapus Beberapa Pembolehubah
Anda juga boleh menghapus beberapa pembolehubah sekaligus dengan menyenaraikannya:

```bash
VAR1="Value1"
VAR2="Value2"
unset VAR1 VAR2
```

## Tips
- Sentiasa semak pembolehubah yang anda ingin hapus sebelum menggunakan `unset` untuk mengelakkan kehilangan data yang penting.
- Gunakan `declare -p` untuk menyemak pembolehubah yang ada sebelum menghapusnya.
- Pastikan anda memahami kesan penghapusan fungsi, kerana ia tidak boleh dipulihkan selepas dihapus.