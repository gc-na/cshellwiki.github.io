# [Linux] Bash mysql Kullanımı: MySQL veritabanı yönetimi

## Genel Bakış
`mysql` komutu, MySQL veritabanı sunucusuna bağlanmak ve SQL sorguları çalıştırmak için kullanılan bir komuttur. Kullanıcıların veritabanları üzerinde sorgular yapmasına, veri eklemesine, güncellemesine ve silmesine olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
mysql [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u [kullanıcı_adı]`: MySQL sunucusuna bağlanmak için kullanıcı adını belirtir.
- `-p`: Şifre girişi için bir istem oluşturur.
- `-h [sunucu_adresi]`: Bağlanılacak MySQL sunucusunun adresini belirtir.
- `-D [veritabanı_adı]`: Belirtilen veritabanına doğrudan bağlanır.
- `--execute`: Verilen SQL komutunu çalıştırır ve çıkış yapar.

## Yaygın Örnekler
1. MySQL sunucusuna bağlanmak:
   ```bash
   mysql -u root -p
   ```

2. Belirli bir veritabanına bağlanmak:
   ```bash
   mysql -u kullanıcı_adı -p -D veritabanı_adı
   ```

3. SQL sorgusu çalıştırmak:
   ```bash
   mysql -u kullanıcı_adı -p -e "SELECT * FROM tablo_adı;"
   ```

4. Veritabanı oluşturmak:
   ```bash
   mysql -u kullanıcı_adı -p -e "CREATE DATABASE yeni_veritabani;"
   ```

## İpuçları
- Şifreyi komut satırında girmemek için `-p` seçeneğini kullanın, bu şekilde güvenliğiniz artar.
- Sık kullandığınız SQL sorgularını bir dosyaya yazıp, `mysql` komutuyla bu dosyayı çalıştırarak zaman kazanabilirsiniz.
- Veritabanı yedeklemeleri için `mysqldump` komutunu kullanmayı unutmayın.