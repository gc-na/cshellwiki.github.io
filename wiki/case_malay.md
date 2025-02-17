# [Linux] Bash case penggunaan: Menentukan pilihan berdasarkan pola

## Overview
Perintah `case` dalam Bash digunakan untuk membuat keputusan berdasarkan nilai yang diberikan. Ia membolehkan pengguna untuk memeriksa satu nilai terhadap beberapa pola dan melaksanakan arahan tertentu berdasarkan padanan yang ditemui.

## Usage
Sintaks asas untuk perintah `case` adalah seperti berikut:

```bash
case [value] in
    [pattern1])
        [commands1]
        ;;
    [pattern2])
        [commands2]
        ;;
    *)
        [default_commands]
        ;;
esac
```

## Common Options
Perintah `case` tidak mempunyai banyak pilihan seperti perintah lain, tetapi berikut adalah beberapa elemen penting:
- `*)`: Menunjukkan pilihan lalai jika tiada pola yang dipadankan.
- `;;`: Menandakan akhir bagi setiap blok arahan untuk pola tertentu.

## Common Examples

### Contoh 1: Memeriksa jenis fail
```bash
filename="data.txt"

case $filename in
    *.txt)
        echo "Ini adalah fail teks."
        ;;
    *.jpg)
        echo "Ini adalah fail gambar."
        ;;
    *)
        echo "Jenis fail tidak dikenali."
        ;;
esac
```

### Contoh 2: Menentukan hari dalam seminggu
```bash
day="Isnin"

case $day in
    Isnin)
        echo "Hari ini adalah Isnin."
        ;;
    Selasa)
        echo "Hari ini adalah Selasa."
        ;;
    Rabu)
        echo "Hari ini adalah Rabu."
        ;;
    *)
        echo "Hari tidak dikenali."
        ;;
esac
```

### Contoh 3: Menentukan pilihan pengguna
```bash
read -p "Pilih pilihan (1/2/3): " choice

case $choice in
    1)
        echo "Anda memilih pilihan 1."
        ;;
    2)
        echo "Anda memilih pilihan 2."
        ;;
    3)
        echo "Anda memilih pilihan 3."
        ;;
    *)
        echo "Pilihan tidak sah."
        ;;
esac
```

## Tips
- Gunakan `case` apabila anda mempunyai banyak pilihan untuk diperiksa; ia lebih bersih dan lebih mudah dibaca berbanding dengan banyak `if` bersarang.
- Pastikan untuk menutup setiap blok arahan dengan `;;` untuk mengelakkan kesilapan.
- Anda boleh menggunakan ekspresi reguler dalam pola untuk lebih fleksibiliti dalam padanan.