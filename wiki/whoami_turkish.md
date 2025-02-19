# [Linux] C Shell (csh) whoami Kullanımı: Kullanıcının adını gösterir

## Genel Bakış
`whoami` komutu, mevcut oturumda kim olduğunuzu gösterir. Yani, terminalde oturum açmış olan kullanıcı adını döndürür. Bu komut, özellikle birden fazla kullanıcı hesabı olan sistemlerde hangi kullanıcıyla işlem yaptığınızı kontrol etmek için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
whoami [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
`whoami` komutunun genellikle kullanılan seçenekleri şunlardır:
- `--help`: Komutun kullanımına dair yardım bilgilerini gösterir.
- `--version`: Komutun sürüm bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `whoami` komutunun bazı pratik örnekleri bulunmaktadır:

1. Mevcut kullanıcı adını öğrenmek için:
   ```csh
   whoami
   ```

2. Yardım bilgilerini görüntülemek için:
   ```csh
   whoami --help
   ```

3. Komutun sürümünü kontrol etmek için:
   ```csh
   whoami --version
   ```

## İpuçları
- `whoami` komutunu sık sık kullanıyorsanız, bir alias oluşturarak daha hızlı erişim sağlayabilirsiniz.
- Eğer birden fazla terminal açtıysanız, hangi terminalde hangi kullanıcıyla işlem yaptığınızı kontrol etmek için `whoami` komutunu kullanmayı unutmayın.