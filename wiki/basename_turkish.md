# [Linux] C Shell (csh) basename Kullanımı: Dosya adlarını ayıklama

## Genel Bakış
`basename` komutu, bir dosya yolundan yalnızca dosya adını ayıklamak için kullanılır. Bu, dosya yolunun son kısmını alarak, dosyanın tam yolunu bilmeden yalnızca adını elde etmenizi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
basename [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Birden fazla dosya adı ile çalışır ve her birinin adını döndürür.
- `-s`: Belirtilen bir uzantıyı dosya adından kaldırır.

## Yaygın Örnekler
Aşağıda `basename` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Basit kullanım
Tam bir dosya yolundan yalnızca dosya adını almak için:

```csh
basename /home/kullanici/dosya.txt
```
Çıktı:
```
dosya.txt
```

### Örnek 2: Uzantıyı kaldırma
Bir dosya adından belirli bir uzantıyı kaldırmak için:

```csh
basename /home/kullanici/dosya.txt .txt
```
Çıktı:
```
dosya
```

### Örnek 3: Birden fazla dosya adı ile çalışma
Birden fazla dosya adı ile çalışmak için:

```csh
basename -a /home/kullanici/dosya1.txt /home/kullanici/dosya2.txt
```
Çıktı:
```
dosya1.txt
dosya2.txt
```

## İpuçları
- `basename` komutunu, dosya adlarını işlemek istediğiniz betiklerde sıkça kullanabilirsiniz.
- Uzantıları kaldırmak için doğru uzantıyı belirttiğinizden emin olun, aksi takdirde beklenmeyen sonuçlar alabilirsiniz.
- Birden fazla dosya adı ile çalışırken `-a` seçeneğini kullanarak tüm dosya adlarını kolayca alabilirsiniz.