# [Linux] C Shell (csh) nslookup Kullanımı: DNS sorgulama aracı

## Genel Bakış
`nslookup`, bir alan adının IP adresini veya bir IP adresinin alan adını sorgulamak için kullanılan bir komuttur. DNS (Domain Name System) ile etkileşimde bulunarak, kullanıcıların internet üzerindeki kaynaklara erişimini kolaylaştırır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
nslookup [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-type=tip`: Sorgulamak istediğiniz DNS kaynağının türünü belirtir (örneğin, A, MX, CNAME).
- `-timeout=sn`: Sorgu zaman aşımını belirler (sn saniye cinsinden).
- `-debug`: Sorgu sırasında daha fazla bilgi verir, hata ayıklama için kullanışlıdır.

## Yaygın Örnekler
1. Bir alan adının IP adresini sorgulamak:
   ```csh
   nslookup www.example.com
   ```

2. Belirli bir DNS sunucusunu kullanarak sorgulama yapmak:
   ```csh
   nslookup www.example.com 8.8.8.8
   ```

3. Bir IP adresinin alan adını sorgulamak:
   ```csh
   nslookup 93.184.216.34
   ```

4. MX kayıtlarını sorgulamak:
   ```csh
   nslookup -type=MX example.com
   ```

## İpuçları
- Sorgulama yapmadan önce DNS sunucusunun doğru olduğundan emin olun.
- `-debug` seçeneğini kullanarak sorgularınızın nasıl işlendiğini görebilir ve sorunları daha kolay tespit edebilirsiniz.
- Sık kullanılan alan adlarını ve IP adreslerini not alarak, hızlı erişim için bir dosyada saklayabilirsiniz.