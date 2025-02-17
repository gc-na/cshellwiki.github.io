# [Linux] Bash split Kullanımı: Dosyaları parçalara ayırma

## Overview
`split` komutu, büyük dosyaları daha küçük parçalara ayırmak için kullanılır. Bu, özellikle büyük veri setleriyle çalışırken veya belirli bir boyut sınırına ulaşan dosyaları yönetirken faydalıdır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
split [options] [arguments]
```

## Common Options
- `-b, --bytes=SIZE`: Her parçanın boyutunu belirler. Örneğin, `-b 1M` 1 megabaytlık parçalar oluşturur.
- `-l, --lines=NUMBER`: Her parçanın kaç satır içereceğini belirler.
- `-d, --numeric-suffixes`: Parça isimlerinde sayısal ekler kullanır.
- `--additional-suffix=SUFFIX`: Parça dosyalarına ek bir uzantı ekler.

## Common Examples
1. **Bir dosyayı 100 satırlık parçalara ayırma:**
   ```bash
   split -l 100 dosya.txt
   ```

2. **Bir dosyayı 1 megabaytlık parçalara ayırma:**
   ```bash
   split -b 1M dosya.txt
   ```

3. **Parça dosyalarına sayısal ek ekleyerek ayırma:**
   ```bash
   split -d -l 50 dosya.txt parca_
   ```

4. **Ek bir uzantı ile parça dosyaları oluşturma:**
   ```bash
   split --additional-suffix=.txt -b 500k dosya.txt parca_
   ```

## Tips
- Parçaların adlandırılmasını kolaylaştırmak için `-d` seçeneğini kullanarak sayısal ekler ekleyebilirsiniz.
- Parçaların boyutunu belirlerken, dosyanızın içeriğine göre uygun bir boyut seçmeye dikkat edin.
- Büyük dosyalarla çalışırken, parçaları bir dizine kaydetmek, dosya yönetimini kolaylaştırabilir.