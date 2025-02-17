# [Linux] Bash break Penggunaan: Menghentikan loop

## Overview
Perintah `break` dalam Bash digunakan untuk menghentikan eksekusi loop, baik itu loop `for`, `while`, atau `until`. Ketika `break` dijalankan, kontrol program akan keluar dari loop yang sedang berjalan dan melanjutkan eksekusi perintah setelah loop tersebut.

## Usage
Berikut adalah sintaks dasar dari perintah `break`:

```bash
break [n]
```

Di mana `n` adalah jumlah level loop yang ingin dihentikan. Jika `n` tidak diberikan, `break` akan menghentikan loop terdekat.

## Common Options
- `n`: Menentukan jumlah level loop yang ingin dihentikan. Jika tidak ada nilai yang diberikan, `break` hanya menghentikan loop terdekat.

## Common Examples

### Contoh 1: Menghentikan loop `for`
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo "Angka: $i"
done
```
Output:
```
Angka: 1
Angka: 2
```

### Contoh 2: Menghentikan loop `while`
```bash
count=1
while [ $count -le 5 ]; do
  if [ $count -eq 4 ]; then
    break
  fi
  echo "Hitung: $count"
  ((count++))
done
```
Output:
```
Hitung: 1
Hitung: 2
Hitung: 3
```

### Contoh 3: Menghentikan loop bersarang
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "i: $i, j: $j"
  done
done
```
Output:
```
i: 1, j: 1
```

## Tips
- Gunakan `break` dengan hati-hati, terutama dalam loop bersarang, untuk memastikan Anda menghentikan loop yang tepat.
- Pertimbangkan untuk menggunakan `continue` jika Anda hanya ingin melewatkan iterasi tertentu tanpa menghentikan seluruh loop.
- Selalu uji skrip Anda untuk memastikan bahwa penggunaan `break` tidak menyebabkan perilaku yang tidak diinginkan dalam logika program Anda.