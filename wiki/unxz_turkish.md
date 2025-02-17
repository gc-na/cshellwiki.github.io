# [Linux] Bash unxz Kullanımı: Sıkıştırılmış dosyaları açar

## Genel Bakış
`unxz` komutu, XZ formatında sıkıştırılmış dosyaları açmak için kullanılan bir araçtır. Bu komut, dosyaların boyutunu küçültmek için XZ algoritmasıyla sıkıştırılmış dosyaları geri yükler ve orijinal dosyayı geri kazanmanızı sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
unxz [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-k`, `--keep`: Sıkıştırılmış dosyayı silmeden açar.
- `-f`, `--force`: Var olan dosyaların üzerine yazmayı zorlar.
- `-v`, `--verbose`: İşlem sırasında ayrıntılı bilgi verir.

## Yaygın Örnekler
Aşağıda `unxz` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Bir XZ dosyasını açmak için:
   ```bash
   unxz dosya.xz
   ```

2. Sıkıştırılmış dosyayı silmeden açmak için:
   ```bash
   unxz -k dosya.xz
   ```

3, Var olan bir dosyanın üzerine yazmak için:
   ```bash
   unxz -f dosya.xz
   ```

4. İşlem sırasında ayrıntılı bilgi almak için:
   ```bash
   unxz -v dosya.xz
   ```

## İpuçları
- `unxz` komutunu kullanmadan önce dosyanızın yedeğini almak iyi bir uygulamadır.
- Sıkıştırılmış dosyaların boyutunu kontrol etmek için `ls -lh` komutunu kullanabilirsiniz.
- Eğer birden fazla dosyayı aynı anda açmak istiyorsanız, dosya isimlerini boşlukla ayırarak yazabilirsiniz:
  ```bash
  unxz dosya1.xz dosya2.xz
  ```