# [Linux] C Shell (csh) hexdump Kullanımı: İkili dosyaların hex formatında görüntülenmesi

## Genel Bakış
`hexdump` komutu, ikili dosyaların içeriğini hexadecimal (hex) formatında görüntülemek için kullanılır. Bu komut, dosyaların iç yapısını analiz etmek veya hata ayıklamak için oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
hexdump [opsiyonlar] [argümanlar]
```

## Yaygın Opsiyonlar
- `-C`: Hexadecimal çıktıyı ASCII karşılıklarıyla birlikte gösterir.
- `-n <byte sayısı>`: Sadece belirtilen byte sayısını görüntüler.
- `-v`: Tüm verileri gösterir; varsayılan olarak tekrarlayan byte'lar gizlenir.
- `-e <format>`: Çıktının formatını özelleştirir.

## Yaygın Örnekler
Aşağıda `hexdump` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Bir dosyanın içeriğini hexadecimal formatında görüntülemek:
   ```csh
   hexdump dosya.txt
   ```

2. Sadece ilk 16 byte'ı görüntülemek:
   ```csh
   hexdump -n 16 dosya.bin
   ```

3. Hexadecimal çıktıyı ASCII karşılıklarıyla birlikte göstermek:
   ```csh
   hexdump -C dosya.txt
   ```

4. Özel bir format ile çıktı almak:
   ```csh
   hexdump -e '16/1 "%02x " "\n"' dosya.bin
   ```

## İpuçları
- `hexdump` komutunu kullanmadan önce dosyanın boyutunu kontrol etmek, gereksiz büyük dosyaların çıktısını almak istemediğinizde faydalı olabilir.
- Çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```csh
  hexdump dosya.txt > cikti.txt
  ```
- Farklı format seçeneklerini denemek, çıktıyı daha okunabilir hale getirebilir. Özellikle `-e` opsiyonu ile özelleştirilmiş formatlar oluşturmak oldukça yararlıdır.