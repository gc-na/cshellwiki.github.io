# [Linux] Bash grep Kullanımı: Metin içinde desen arama

## Genel Bakış
`grep` komutu, metin dosyaları içinde belirli bir desen veya kelime grubu aramak için kullanılır. Kullanıcıların dosyaların içeriğini hızlı bir şekilde taramasına ve aradıkları bilgiyi bulmasına olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
grep [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Büyük/küçük harf duyarsız arama yapar.
- `-v`: Belirtilen deseni içermeyen satırları gösterir.
- `-r`: Alt dizinler dahil olmak üzere, dizin içinde arama yapar.
- `-n`: Eşleşen satırların numaralarını gösterir.
- `-l`: Eşleşen dosya adlarını listeler.

## Yaygın Örnekler
Aşağıda `grep` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Belirli bir kelimeyi bir dosyada aramak:
   ```bash
   grep "örnek" dosya.txt
   ```

2. Büyük/küçük harf duyarsız arama yapmak:
   ```bash
   grep -i "örnek" dosya.txt
   ```

3. Bir dizin içinde alt dizinlerle birlikte arama yapmak:
   ```bash
   grep -r "örnek" /path/to/dizin
   ```

4. Eşleşen satırların numaralarını görmek:
   ```bash
   grep -n "örnek" dosya.txt
   ```

5. Eşleşmeyen satırları listelemek:
   ```bash
   grep -v "örnek" dosya.txt
   ```

## İpuçları
- `grep` komutunu daha etkili kullanmak için, arama yapmadan önce dosyanın içeriğini `cat` komutuyla görüntüleyebilirsiniz.
- Birden fazla deseni aramak için `-e` seçeneğini kullanabilirsiniz:
  ```bash
  grep -e "örnek1" -e "örnek2" dosya.txt
  ```
- Daha karmaşık aramalar için düzenli ifadeleri kullanabilirsiniz. Bu, arama yeteneklerinizi büyük ölçüde artırır.