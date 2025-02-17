# [Linux] Bash psql Kullanımı: PostgreSQL veritabanına erişim

## Genel Bakış
`psql`, PostgreSQL veritabanı yönetim sistemine komut satırı üzerinden erişim sağlayan bir araçtır. Kullanıcıların veritabanlarıyla etkileşimde bulunmasına, SQL sorguları çalıştırmasına ve veritabanı yönetim görevlerini yerine getirmesine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
psql [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: Veritabanı sunucusunun adresini belirtir.
- `-U`: Veritabanı kullanıcı adını belirtir.
- `-d`: Bağlanılacak veritabanının adını belirtir.
- `-p`: Veritabanı sunucusunun port numarasını belirtir.
- `-f`: Bir dosyadan SQL komutlarını çalıştırmak için kullanılır.

## Yaygın Örnekler
1. PostgreSQL veritabanına bağlanma:
   ```bash
   psql -h localhost -U kullanici_adi -d veritabani_adi
   ```

2. SQL dosyasını çalıştırma:
   ```bash
   psql -U kullanici_adi -d veritabani_adi -f dosya.sql
   ```

3. Veritabanındaki tüm tabloları listeleme:
   ```bash
   psql -U kullanici_adi -d veritabani_adi -c "\dt"
   ```

4. Belirli bir SQL sorgusunu çalıştırma:
   ```bash
   psql -U kullanici_adi -d veritabani_adi -c "SELECT * FROM tablo_adi;"
   ```

## İpuçları
- `psql` oturumunu başlatmadan önce veritabanı kullanıcı adınızı ve şifrenizi kontrol edin.
- Sık kullandığınız sorguları bir dosyaya kaydedip `-f` seçeneği ile çalıştırarak zaman kazanabilirsiniz.
- `\help` komutunu kullanarak `psql` içindeki komutlar hakkında bilgi alabilirsiniz.