# [Linux] Bash basename Kullanımı: Dosya adını almak için

## Genel Bakış
`basename` komutu, bir dosya yolundan yalnızca dosya adını çıkarmak için kullanılır. Bu, dosya adını ve uzantısını ayırmak veya yalnızca dosya adını almak için faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
basename [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Birden fazla dosya adı için `basename` komutunu uygular.
- `-s`: Belirtilen bir uzantıyı dosya adından kaldırır.

## Yaygın Örnekler
Aşağıda `basename` komutunun bazı pratik örnekleri verilmiştir:

### Örnek 1: Basit Kullanım
Bir dosya yolundan yalnızca dosya adını almak için:

```bash
basename /home/kullanici/dosya.txt
```
Çıktı:
```
dosya.txt
```

### Örnek 2: Uzantıyı Kaldırma
Bir dosya adından uzantıyı kaldırmak için:

```bash
basename /home/kullanici/dosya.txt .txt
```
Çıktı:
```
dosya
```

### Örnek 3: Birden Fazla Dosya Adı
Birden fazla dosya adı için `-a` seçeneği ile kullanımı:

```bash
basename -a /home/kullanici/dosya1.txt /home/kullanici/dosya2.txt
```
Çıktı:
```
dosya1.txt
dosya2.txt
```

## İpuçları
- `basename` komutunu, dosya adlarını işlemek için betiklerinizde kullanarak daha okunabilir hale getirebilirsiniz.
- Uzantıları kaldırmak için `-s` seçeneğini kullanarak dosya adlarını daha temiz hale getirebilirsiniz.
- Birden fazla dosya adı ile çalışırken, çıktıyı daha iyi yönetmek için `xargs` ile birleştirebilirsiniz.