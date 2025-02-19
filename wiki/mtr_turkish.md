# [Linux] C Shell (csh) mtr Kullanımı: Ağ bağlantılarını izleme aracı

## Genel Bakış
mtr (My Traceroute), ağ bağlantılarını izlemek ve analiz etmek için kullanılan bir araçtır. Hem ping hem de traceroute işlevlerini bir araya getirerek, bir hedefe olan bağlantının kalitesini ve yolunu görsel olarak sunar.

## Kullanım
Temel komut yapısı aşağıdaki gibidir:

```csh
mtr [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-r`: Rapor modunda çalışır ve sonuçları daha düzenli bir formatta gösterir.
- `-c [sayı]`: Belirtilen sayıda paket gönderir ve ardından durur.
- `-i [saniye]`: Paketler arasında bekleme süresini ayarlar.
- `-p`: Port numarasını belirtir; varsayılan olarak 33434 kullanılır.

## Yaygın Örnekler
Aşağıda mtr komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Basit bir mtr komutu ile bir hedefe bağlanmak:
   ```csh
   mtr example.com
   ```

2. Rapor modunda çalıştırmak:
   ```csh
   mtr -r example.com
   ```

3. Belirli bir sayıda paket göndererek test yapmak:
   ```csh
   mtr -c 10 example.com
   ```

4. Paketler arasında 1 saniye bekleyerek izleme yapmak:
   ```csh
   mtr -i 1 example.com
   ```

## İpuçları
- mtr komutunu çalıştırmadan önce ağ bağlantınızın aktif olduğundan emin olun.
- Sonuçları daha iyi analiz edebilmek için `-r` seçeneğini kullanarak rapor modunda çalıştırmayı deneyin.
- Ağ sorunlarını tespit ederken, farklı hedeflerle test yaparak karşılaştırmalar yapabilirsiniz.