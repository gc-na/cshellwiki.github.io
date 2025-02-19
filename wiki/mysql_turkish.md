# [Linux] C Shell (csh) mysql Kullanımı: Veritabanı yönetimi için bir komut

## Overview
`mysql` komutu, MySQL veritabanı yönetim sistemine bağlanmak ve SQL sorguları çalıştırmak için kullanılan bir komuttur. Kullanıcıların veritabanlarıyla etkileşimde bulunmalarını sağlar.

## Usage
Temel sözdizimi şu şekildedir:

```csh
mysql [options] [arguments]
```

## Common Options
- `-u [kullanıcı_adı]`: MySQL veritabanına bağlanmak için kullanıcı adını belirtir.
- `-p`: Parola girişi için bir istem oluşturur.
- `-h [sunucu_adresi]`: Bağlanılacak MySQL sunucusunun adresini belirtir.
- `-D [veritabanı_adı]`: Belirli bir veritabanına doğrudan bağlanmak için kullanılır.
- `--execute="[sorgu]"`: Belirtilen SQL sorgusunu doğrudan çalıştırır.

## Common Examples
Aşağıda `mysql` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. MySQL sunucusuna bağlanmak:
   ```csh
   mysql -u root -p
   ```

2. Belirli bir veritabanına bağlanmak:
   ```csh
   mysql -u kullanıcı_adı -p -D veritabanı_adı
   ```

3. SQL sorgusu çalıştırmak:
   ```csh
   mysql -u kullanıcı_adı -p --execute="SELECT * FROM tablo_adı;"
   ```

4. Veritabanı listesini görüntülemek:
   ```csh
   mysql -u kullanıcı_adı -p -e "SHOW DATABASES;"
   ```

## Tips
- Kullanıcı adınızı ve parolanızı güvenli bir şekilde saklayın; parolayı komut satırında yazmak yerine `-p` seçeneğini kullanarak istemde girin.
- Sık kullanılan sorguları bir dosyada saklayarak `mysql` komutuyla bu dosyayı çalıştırabilirsiniz.
- Veritabanı yedeklemeleri almak için `mysqldump` komutunu kullanmayı düşünün.