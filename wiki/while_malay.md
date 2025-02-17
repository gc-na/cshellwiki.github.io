# [Linux] Bash while penggunaan: Mengulangi arahan berdasarkan syarat

## Overview
Perintah `while` dalam Bash digunakan untuk menjalankan satu atau lebih arahan berulang kali selagi syarat yang ditetapkan adalah benar. Ini membolehkan pengguna untuk mencipta gelung yang berkesan untuk pelbagai tugas automasi.

## Usage
Berikut adalah sintaks asas untuk perintah `while`:

```bash
while [syarat]
do
    # arahan yang ingin dijalankan
done
```

## Common Options
- `-n`: Menguji jika panjang string tidak kosong.
- `-z`: Menguji jika panjang string kosong.
- `-eq`: Menguji jika dua nilai adalah sama.
- `-ne`: Menguji jika dua nilai tidak sama.

## Common Examples

### Contoh 1: Mengulangi sehingga syarat tidak lagi dipenuhi
```bash
count=1
while [ $count -le 5 ]
do
    echo "Pengiraan: $count"
    ((count++))
done
```
*Output:*
```
Pengiraan: 1
Pengiraan: 2
Pengiraan: 3
Pengiraan: 4
Pengiraan: 5
```

### Contoh 2: Membaca fail baris demi baris
```bash
while IFS= read -r line
do
    echo "Baris: $line"
done < fail.txt
```

### Contoh 3: Mengulangi sehingga pengguna menghentikan proses
```bash
while true
do
    read -p "Teruskan? (y/n): " answer
    if [ "$answer" != "y" ]; then
        break
    fi
done
```

## Tips
- Pastikan syarat dalam `while` adalah jelas untuk mengelakkan gelung tanpa henti.
- Gunakan `break` untuk keluar dari gelung apabila syarat tertentu dipenuhi.
- Sentiasa gunakan `IFS= read -r` untuk membaca fail bagi mengelakkan masalah dengan ruang kosong dan karakter khas.