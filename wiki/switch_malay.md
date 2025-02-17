# [Linux] Bash switch penggunaan: Mengubah antara pilihan

## Overview
Perintah `switch` dalam Bash digunakan untuk mengendalikan aliran program berdasarkan nilai yang diberikan. Ia membolehkan pengguna untuk membuat keputusan berdasarkan pelbagai pilihan yang ditetapkan.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `switch`:

```bash
switch [options] [arguments]
```

## Common Options
- `-e`: Menetapkan pilihan lalai jika tiada pilihan lain yang sepadan.
- `-v`: Mengaktifkan mod verbose untuk output yang lebih terperinci.
- `-h`: Menunjukkan bantuan dan maklumat penggunaan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `switch`:

### Contoh 1: Menggunakan switch untuk pilihan
```bash
case $1 in
    start)
        echo "Memulakan proses..."
        ;;
    stop)
        echo "Menghentikan proses..."
        ;;
    *)
        echo "Pilihan tidak sah. Sila gunakan 'start' atau 'stop'."
        ;;
esac
```

### Contoh 2: Menggunakan switch dengan argumen
```bash
case $2 in
    debug)
        echo "Mod debug diaktifkan."
        ;;
    release)
        echo "Mod release diaktifkan."
        ;;
    *)
        echo "Mod tidak dikenali. Sila pilih 'debug' atau 'release'."
        ;;
esac
```

### Contoh 3: Menetapkan pilihan lalai
```bash
case $1 in
    yes)
        echo "Anda memilih ya."
        ;;
    no)
        echo "Anda memilih tidak."
        ;;
    *)
        echo "Pilihan lalai: tidak ada pilihan yang dipilih."
        ;;
esac
```

## Tips
- Sentiasa gunakan tanda kurung untuk memisahkan pilihan dalam `case`.
- Pastikan untuk menutup setiap pilihan dengan `;;` untuk mengelakkan kesilapan.
- Gunakan mod verbose (`-v`) untuk mendapatkan maklumat tambahan semasa debugging.