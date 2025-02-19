# [Linux] C Shell (csh) rmdir Kullanımı: Boş dizinleri silme

## Genel Bakış
`rmdir` komutu, belirtilen dizinleri silmek için kullanılır. Ancak, yalnızca boş dizinleri silebilir; eğer dizin içinde dosya veya başka dizinler varsa, bu komut çalışmaz.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
rmdir [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Üst dizinleri de siler, yalnızca boş oldukları takdirde.
- `--help`: Komutun kullanımına dair yardım bilgilerini gösterir.
- `--version`: Komutun sürüm bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `rmdir` komutunun bazı pratik örnekleri bulunmaktadır:

1. Boş bir dizini silmek:
   ```csh
   rmdir /path/to/empty_directory
   ```

2. Birden fazla boş dizini silmek:
   ```csh
   rmdir /path/to/empty_directory1 /path/to/empty_directory2
   ```

3. Üst dizinleri de silmek (boş oldukları takdirde):
   ```csh
   rmdir -p /path/to/parent_directory/empty_directory
   ```

4. Yardım almak için:
   ```csh
   rmdir --help
   ```

## İpuçları
- `rmdir` komutunu kullanmadan önce dizinin gerçekten boş olduğundan emin olun; aksi takdirde komut başarısız olacaktır.
- Dizinleri silmeden önce içindeki dosyaları kontrol etmek için `ls` komutunu kullanabilirsiniz.
- Eğer dizin içinde dosyalar varsa ve bunları silmek istiyorsanız, `rm -r` komutunu kullanmalısınız.