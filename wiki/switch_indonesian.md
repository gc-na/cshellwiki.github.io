# [Sistem Operasi] C Shell (csh) switch: Mengubah nilai variabel

## Overview
Perintah `switch` dalam C Shell (csh) digunakan untuk melakukan pemilihan berdasarkan nilai dari suatu variabel. Ini mirip dengan pernyataan `switch` dalam bahasa pemrograman lain, yang memungkinkan pengguna untuk mengeksekusi blok kode yang berbeda berdasarkan nilai yang diberikan.

## Usage
Berikut adalah sintaks dasar untuk perintah `switch`:

```
switch (ekspresi)
    case nilai1:
        perintah1
        breaksw
    case nilai2:
        perintah2
        breaksw
    default:
        perintah_default
endsw
```

## Common Options
- `case nilai:`: Menentukan nilai yang akan diperiksa.
- `breaksw`: Menghentikan eksekusi dari blok `switch` saat ini.
- `default:`: Menentukan perintah yang dijalankan jika tidak ada nilai yang cocok.

## Common Examples

### Contoh 1: Pemilihan Berdasarkan Bulan
```csh
set bulan = "Januari"
switch ($bulan)
    case "Januari":
        echo "Ini bulan pertama."
        breaksw
    case "Februari":
        echo "Ini bulan kedua."
        breaksw
    default:
        echo "Bulan tidak dikenali."
endsw
```

### Contoh 2: Menentukan Hari
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
        echo "Hari tidak dikenali."
endsw
```

### Contoh 3: Menggunakan Default
```csh
set warna = "Merah"
switch ($warna)
    case "Hijau":
        echo "Warna adalah Hijau."
        breaksw
    case "Biru":
        echo "Warna adalah Biru."
        breaksw
    default:
        echo "Warna tidak dikenali, menggunakan default."
endsw
```

## Tips
- Selalu gunakan `breaksw` setelah setiap case untuk mencegah eksekusi berlanjut ke case berikutnya.
- Gunakan `default` untuk menangani nilai yang tidak terduga.
- Pastikan untuk mengelompokkan case yang memiliki hasil yang sama untuk mengurangi duplikasi kode.