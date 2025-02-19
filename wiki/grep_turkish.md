# [Linux] C Shell (csh) grep Kullanımı: Metin içinde desen arama

## Genel Bakış
`grep` komutu, bir dosya veya standart girdi içinde belirli bir deseni aramak için kullanılır. Genellikle metin dosyalarında belirli kelimeleri veya ifadeleri bulmak için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
grep [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Büyük/küçük harf duyarsız arama yapar.
- `-v`: Belirtilen deseni içermeyen satırları gösterir.
- `-r`: Alt dizinlerdeki dosyalar dahil olmak üzere, dizin içinde arama yapar.
- `-n`: Eşleşen satırların numaralarını gösterir.
- `-l`: Eşleşen dosyaların adlarını listeler.

## Yaygın Örnekler
Aşağıda `grep` komutunun bazı pratik örnekleri bulunmaktadır:

1. Belirli bir kelimeyi bir dosyada arama:
   ```bash
   grep "kelime" dosya.txt
   ```

2. Büyük/küçük harf duyarsız arama:
   ```bash
   grep -i "kelime" dosya.txt
   ```

3. Eşleşmeyen satırları gösterme:
   ```bash
   grep -v "kelime" dosya.txt
   ```

4. Bir dizin içindeki tüm dosyalarda arama:
   ```bash
   grep -r "kelime" /path/to/dizin
   ```

5. Eşleşen satırların numaralarını gösterme:
   ```bash
   grep -n "kelime" dosya.txt
   ```

## İpuçları
- `grep` komutunu daha etkili kullanmak için, aramak istediğiniz deseni tırnak içinde belirtin.
- Karmaşık desenler için düzenli ifadeleri kullanabilirsiniz.
- `grep` komutunu diğer komutlarla birleştirerek daha güçlü aramalar yapabilirsiniz. Örneğin, `cat dosya.txt | grep "kelime"` ile dosyayı okuduktan sonra arama yapabilirsiniz.