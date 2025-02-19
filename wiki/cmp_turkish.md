# [Linux] C Shell (csh) cmp Kullanımı: İki dosyayı karşılaştırma

## Overview
`cmp` komutu, iki dosyanın içeriğini karşılaştırmak için kullanılır. Bu komut, dosyalar arasında farklılıkları tespit eder ve hangi baytların farklı olduğunu gösterir.

## Usage
Temel sözdizimi şu şekildedir:
```csh
cmp [options] [arguments]
```

## Common Options
- `-l`: Farklı baytların konumlarını ve değerlerini gösterir.
- `-s`: Farklılık olup olmadığını kontrol eder, ancak herhangi bir çıktı vermez.
- `-i OFFSET`: Karşılaştırmaya belirli bir bayt konumundan başlar.
- `-n N`: Sadece ilk N baytı karşılaştırır.

## Common Examples
Aşağıda `cmp` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### İki dosyayı karşılaştırma
```csh
cmp dosya1.txt dosya2.txt
```

### Farklı baytların konumlarını ve değerlerini gösterme
```csh
cmp -l dosya1.txt dosya2.txt
```

### Sadece farklılık olup olmadığını kontrol etme
```csh
cmp -s dosya1.txt dosya2.txt
```

### Belirli bir bayt konumundan karşılaştırmaya başlama
```csh
cmp -i 10 dosya1.txt dosya2.txt
```

### İlk N baytı karşılaştırma
```csh
cmp -n 100 dosya1.txt dosya2.txt
```

## Tips
- `cmp` komutunu kullanırken, dosyaların boyutlarının aynı olup olmadığını kontrol etmek iyi bir uygulamadır.
- Farklılıkları daha iyi anlamak için `-l` seçeneğini kullanarak hangi baytların farklı olduğunu görebilirsiniz.
- `cmp` komutunu sık sık kullananlar için, alias tanımlayarak daha hızlı erişim sağlamak faydalı olabilir.