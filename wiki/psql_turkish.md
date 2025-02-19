# [Linux] C Shell (csh) psql Kullanımı: Veritabanı sorgulama aracı

## Genel Bakış
`psql`, PostgreSQL veritabanı yönetim sistemi için bir komut satırı arayüzüdür. Kullanıcıların veritabanlarına bağlanmasına, SQL sorguları çalıştırmasına ve veritabanı nesneleri üzerinde işlem yapmasına olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
psql [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: Veritabanı sunucusunun adresini belirtir.
- `-U`: Veritabanı kullanıcı adını belirtir.
- `-d`: Bağlanılacak veritabanının adını belirtir.
- `-p`: Veritabanı sunucusunun port numarasını belirtir.
- `-W`: Şifre girişi için kullanıcıdan onay ister.

## Yaygın Örnekler
Aşağıda `psql` komutunun bazı pratik örnekleri verilmiştir:

1. Belirli bir veritabanına bağlanmak:
   ```bash
   psql -h localhost -U kullaniciadi -d veritabaniadi
   ```

2. SQL sorgusu çalıştırmak:
   ```bash
   psql -d veritabaniadi -c "SELECT * FROM tablo_adi;"
   ```

3. Veritabanındaki tüm tabloları listelemek:
   ```bash
   psql -d veritabaniadi -c "\dt"
   ```

4. Bir SQL dosyasını çalıştırmak:
   ```bash
   psql -d veritabaniadi -f dosya.sql
   ```

## İpuçları
- `psql` oturumunu başlatmadan önce veritabanı bağlantı bilgilerini doğru girdiğinizden emin olun.
- Sık kullanılan sorguları bir dosyada saklayarak `-f` seçeneği ile kolayca çalıştırabilirsiniz.
- `\?` komutunu kullanarak `psql` içindeki komutların listesini görüntüleyebilirsiniz.