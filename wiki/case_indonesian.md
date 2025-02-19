# [Sistem Operasi] C Shell (csh) case: Mengelompokkan pernyataan

## Overview
Perintah `case` dalam C Shell (csh) digunakan untuk mengelompokkan pernyataan berdasarkan pola yang cocok dengan nilai variabel. Ini berguna untuk menghindari penggunaan banyak pernyataan `if` dan membuat skrip lebih mudah dibaca.

## Usage
Sintaks dasar dari perintah `case` adalah sebagai berikut:

```
case [variabel] in
    [pola1]) 
        [pernyataan1]
        ;;
    [pola2]) 
        [pernyataan2]
        ;;
    ...
esac
```

## Common Options
Perintah `case` tidak memiliki banyak opsi, tetapi berikut adalah beberapa elemen penting yang perlu diperhatikan:
- `in`: Menandai awal dari pola yang akan dicocokkan.
- `)` : Menandai akhir dari pola.
- `;;`: Menandai akhir dari pernyataan untuk pola tertentu.
- `esac`: Menandai akhir dari blok `case`.

## Common Examples

### Contoh 1: Menggunakan case untuk menentukan hari
```csh
set hari = "Senin"
switch ($hari)
    case "Senin":
        echo "Hari ini adalah Senin."
        breaksw
    case "Selasa":
        echo "Hari ini adalah Selasa."
        breaksw
    default:
        echo "Hari tidak dikenal."
end
```

### Contoh 2: Mengelompokkan input pengguna
```csh
set warna = $1
switch ($warna)
    case "merah":
        echo "Anda memilih warna merah."
        breaksw
    case "biru":
        echo "Anda memilih warna biru."
        breaksw
    case "hijau":
        echo "Anda memilih warna hijau."
        breaksw
    default:
        echo "Warna tidak dikenali."
end
```

### Contoh 3: Menggunakan wildcard
```csh
set file = "data.txt"
switch ($file)
    case "*.txt":
        echo "Ini adalah file teks."
        breaksw
    case "*.jpg":
        echo "Ini adalah file gambar."
        breaksw
    default:
        echo "Tipe file tidak dikenali."
end
```

## Tips
- Gunakan `case` untuk menyederhanakan logika pemilihan yang kompleks dalam skrip Anda.
- Pastikan untuk menggunakan `breaksw` setelah setiap pernyataan untuk mencegah eksekusi pernyataan berikutnya.
- Manfaatkan wildcard untuk mencocokkan pola yang lebih umum, seperti file dengan ekstensi tertentu.