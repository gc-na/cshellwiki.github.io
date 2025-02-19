# [Linux] C Shell (csh) umask Kullanımı: Dosya izinlerini ayarlamak

## Overview
`umask` komutu, yeni oluşturulan dosyaların ve dizinlerin varsayılan izinlerini ayarlamak için kullanılır. Bu komut, kullanıcıların dosya ve dizin izinlerini kontrol etmelerine olanak tanır.

## Usage
Temel sözdizimi şu şekildedir:
```
umask [options] [arguments]
```

## Common Options
- `-S`: Mevcut umask değerini sembolik biçimde gösterir.
- `-p`: Mevcut umask değerini gösterir, ancak değişiklik yapmaz.

## Common Examples
1. Mevcut umask değerini görüntüleme:
   ```csh
   umask
   ```

2. Umask değerini 022 olarak ayarlama (grup ve diğer kullanıcılar için yazma iznini kaldırır):
   ```csh
   umask 022
   ```

3. Umask değerini sembolik olarak görüntüleme:
   ```csh
   umask -S
   ```

4. Umask değerini 007 olarak ayarlama (sadece sahibi için tam izin, grup ve diğerleri için hiç izin yok):
   ```csh
   umask 007
   ```

## Tips
- Umask değerini ayarladıktan sonra, yeni oluşturulan dosyaların izinlerini kontrol etmek için `ls -l` komutunu kullanın.
- Umask ayarlarını kalıcı hale getirmek için, bu komutu kullanıcı profil dosyanıza ekleyin (örneğin, `.cshrc`).
- Farklı projeler için farklı umask değerleri kullanarak, dosya izinlerini daha iyi yönetebilirsiniz.