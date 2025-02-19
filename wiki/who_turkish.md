# [Linux] C Shell (csh) who Kullanımı: Kullanıcı bilgilerini görüntüler

## Overview
`who` komutu, sistemde oturum açmış olan kullanıcıların listesini gösterir. Bu komut, kullanıcı adı, oturum açma zamanı ve terminal bilgileri gibi detayları sağlar.

## Usage
Temel sözdizimi şu şekildedir:
```
who [options] [arguments]
```

## Common Options
- `-a`: Tüm bilgileri gösterir, yani kullanıcılar hakkında daha fazla detay sunar.
- `-b`: Sistemin en son yeniden başlatıldığı zamanı gösterir.
- `-q`: Sadece kullanıcı adlarını ve toplam kullanıcı sayısını gösterir.
- `-H`: Başlık satırını gösterir.

## Common Examples
Aşağıda `who` komutunun bazı pratik örnekleri bulunmaktadır:

1. Sistemdeki tüm kullanıcıları listeleme:
   ```csh
   who
   ```

2. Tüm bilgileri gösterme:
   ```csh
   who -a
   ```

3. Sistemin en son ne zaman yeniden başlatıldığını öğrenme:
   ```csh
   who -b
   ```

4. Sadece kullanıcı adlarını ve toplam sayısını gösterme:
   ```csh
   who -q
   ```

5. Başlık satırını göstererek kullanıcıları listeleme:
   ```csh
   who -H
   ```

## Tips
- `who` komutunu sık sık kullanarak sistemdeki aktif kullanıcıları takip edebilirsiniz.
- Komutu belirli bir dosya ile kullanarak, kullanıcıların oturum açma bilgilerini daha detaylı inceleyebilirsiniz.
- `who` komutunu `grep` ile birleştirerek belirli bir kullanıcıyı aramak için kullanabilirsiniz. Örneğin:
  ```csh
  who | grep kullanıcı_adı
  ```