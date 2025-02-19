# [Linux] C Shell (csh) diff Kullanımı: Dosya farklılıklarını karşılaştırma

## Genel Bakış
`diff` komutu, iki dosya arasındaki farklılıkları karşılaştırmak için kullanılır. Bu komut, hangi satırların eklendiğini, silindiğini veya değiştirildiğini gösterir ve genellikle metin dosyaları üzerinde çalışırken oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
diff [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u`: Birleştirilmiş biçimde çıktı verir.
- `-c`: Bağlam biçiminde çıktı verir.
- `-i`: Büyük/küçük harf duyarsız karşılaştırma yapar.
- `-w`: Boşlukları dikkate almaz.

## Yaygın Örnekler
Aşağıda `diff` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: İki dosya arasındaki farklılıkları gösterme
```csh
diff dosya1.txt dosya2.txt
```

### Örnek 2: Birleştirilmiş biçimde çıktı alma
```csh
diff -u dosya1.txt dosya2.txt
```

### Örnek 3: Büyük/küçük harf duyarsız karşılaştırma
```csh
diff -i dosya1.txt dosya2.txt
```

### Örnek 4: Boşlukları dikkate almadan karşılaştırma
```csh
diff -w dosya1.txt dosya2.txt
```

## İpuçları
- `diff` çıktısını daha iyi anlamak için `-u` veya `-c` seçeneklerini kullanarak daha okunabilir bir format elde edebilirsiniz.
- Farklılıkları daha iyi analiz etmek için `diff` çıktısını bir dosyaya yönlendirebilirsiniz:
  ```csh
  diff dosya1.txt dosya2.txt > farklar.txt
  ```
- `diff` komutunu sıkça kullandığınız dosyalar için bir alias tanımlamak, işlemlerinizi hızlandırabilir. Örneğin:
  ```csh
  alias d='diff -u'
  ```