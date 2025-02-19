# [Linux] C Shell (csh) split Kullanımı: Dosyaları parçalara ayırma

## Overview
`split` komutu, büyük dosyaları daha küçük parçalara ayırmak için kullanılır. Bu, büyük dosyaların yönetimini kolaylaştırır ve belirli boyutlarda dosyalar oluşturmanıza olanak tanır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
split [options] [arguments]
```

## Common Options
- `-b SIZE`: Her parçanın boyutunu belirler. Örneğin, `-b 1M` 1 megabaytlık parçalar oluşturur.
- `-l NUM`: Her parçanın satır sayısını belirler. Örneğin, `-l 100` her parçanın 100 satır içermesini sağlar.
- `-d`: Parçaların adlandırılmasında sayısal bir sıralama kullanır. Varsayılan olarak harf sıralaması kullanılır.
- `--additional-suffix=SUFFIX`: Parçalara ek bir uzantı ekler.

## Common Examples
Aşağıda `split` komutunun bazı pratik örnekleri verilmiştir:

### Örnek 1: Satır sayısına göre parçalama
```bash
split -l 50 büyük_dosya.txt
```
Bu komut, `büyük_dosya.txt` dosyasını her biri 50 satır içeren parçalara ayırır.

### Örnek 2: Boyuta göre parçalama
```bash
split -b 1M büyük_dosya.txt
```
Bu komut, `büyük_dosya.txt` dosyasını her biri 1 megabayt boyutunda parçalara ayırır.

### Örnek 3: Sayısal sıralama ile parçalama
```bash
split -d -l 100 büyük_dosya.txt parça_
```
Bu komut, `büyük_dosya.txt` dosyasını her biri 100 satır içeren parçalara ayırır ve parçaları `parça_00`, `parça_01`, vb. şeklinde adlandırır.

### Örnek 4: Ek uzantı ile parçalama
```bash
split --additional-suffix=.txt -b 500k büyük_dosya.txt parça_
```
Bu komut, `büyük_dosya.txt` dosyasını her biri 500 kilobayt boyutunda parçalara ayırır ve her parçaya `.txt` uzantısı ekler.

## Tips
- Büyük dosyaları parçalara ayırmadan önce dosyanın boyutunu kontrol edin, böylece uygun boyutları seçebilirsiniz.
- Parçaları adlandırırken anlamlı isimler kullanmak, dosyaları daha sonra bulmayı kolaylaştırır.
- `split` komutunu sık sık kullananlar için, sık kullanılan seçenekleri bir alias olarak tanımlamak faydalı olabilir.