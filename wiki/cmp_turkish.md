# [Linux] Bash cmp Kullanımı: İki dosyayı karşılaştırma

## Overview
`cmp` komutu, iki dosyanın içeriğini karşılaştırmak için kullanılır. Bu komut, dosyalar arasındaki farklılıkları belirlemek ve hangi baytların farklı olduğunu göstermek için idealdir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
cmp [options] [arguments]
```

## Common Options
- `-l`: Farklı baytları ve konumlarını listele.
- `-s`: Çıktıyı bastır, sadece dosyaların farklı olup olmadığını belirt.
- `-i`: Belirtilen bayt sayısına kadar karşılaştırma yap.
- `-n`: Belirtilen bayt sayısı kadar karşılaştırma yap, eğer bu sayı dosyanın boyutundan küçükse.

## Common Examples
Aşağıda `cmp` komutunun bazı pratik örnekleri bulunmaktadır:

1. İki dosyayı karşılaştır ve farklılıkları göster:
   ```bash
   cmp dosya1.txt dosya2.txt
   ```

2. Farklı baytları ve konumlarını listele:
   ```bash
   cmp -l dosya1.txt dosya2.txt
   ```

3. Sadece dosyaların farklı olup olmadığını kontrol et:
   ```bash
   cmp -s dosya1.txt dosya2.txt
   ```

4. İlk 10 baytı karşılaştır:
   ```bash
   cmp -n 10 dosya1.txt dosya2.txt
   ```

## Tips
- `cmp` komutunu kullanmadan önce dosyaların boyutlarını kontrol etmek, gereksiz karşılaştırmaların önüne geçebilir.
- Büyük dosyalarla çalışırken, `-s` seçeneği ile yalnızca farklılıkların olup olmadığını kontrol etmek zaman kazandırabilir.
- Farklılıkları daha iyi anlamak için `-l` seçeneği ile detaylı bir çıktı almak faydalı olabilir.