# [Unix] C Shell (csh) ftp Kullanımı: Dosya transferi için bir komut

## Genel Bakış
`ftp` komutu, dosyaları bir ağ üzerinden transfer etmek için kullanılan bir protokoldür. Bu komut, kullanıcıların bir FTP sunucusuna bağlanarak dosya yüklemesine veya indirmesine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
ftp [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Etkileşimli moddan çıkış yapar, yani dosya transferi sırasında onay istemez.
- `-v`: Ayrıntılı modda çalışır, daha fazla bilgi gösterir.
- `-n`: Otomatik olarak giriş yapmaz, kullanıcıdan kimlik bilgilerini girmesini ister.

## Yaygın Örnekler
Aşağıda `ftp` komutunun bazı pratik örnekleri bulunmaktadır:

1. FTP sunucusuna bağlanma:
   ```csh
   ftp ftp.example.com
   ```

2. Kullanıcı adı ve şifre ile giriş yapma:
   ```csh
   ftp
   Name (ftp.example.com:user): kullanıcı_adı
   Password: şifre
   ```

3. Dosya indirme:
   ```csh
   get dosya.txt
   ```

4. Dosya yükleme:
   ```csh
   put dosya.txt
   ```

5. Tüm dosyaları indirme:
   ```csh
   mget *
   ```

## İpuçları
- Bağlantı kurmadan önce FTP sunucusunun adresini ve kimlik bilgilerini doğru girdiğinizden emin olun.
- Dosya transferi sırasında bağlantının kesilmemesi için mümkünse kablolu bir bağlantı kullanın.
- `-i` seçeneğini kullanarak çok sayıda dosya transferi yaparken onay istemeden işlemi hızlandırabilirsiniz.