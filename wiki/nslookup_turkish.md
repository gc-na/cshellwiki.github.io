# [Linux] Bash nslookup Kullanımı: DNS sorgulama aracı

## Genel Bakış
`nslookup`, bir alan adının IP adresini veya bir IP adresinin alan adını sorgulamak için kullanılan bir komut satırı aracıdır. DNS (Domain Name System) ile etkileşimde bulunarak, kullanıcıların alan adları hakkında bilgi almasına olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:
```
nslookup [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-type=tip`: Sorgulamak istediğiniz kayıt türünü belirtir (örneğin, A, AAAA, MX).
- `-timeout=sn`: Zaman aşımı süresini saniye cinsinden ayarlar.
- `-retry=sayısı`: Sorgu için yeniden deneme sayısını belirler.

## Yaygın Örnekler
1. Bir alan adının IP adresini sorgulama:
   ```bash
   nslookup example.com
   ```

2. Belirli bir DNS sunucusu kullanarak sorgulama:
   ```bash
   nslookup example.com 8.8.8.8
   ```

3. MX kayıtlarını sorgulama:
   ```bash
   nslookup -type=MX example.com
   ```

4. Bir IP adresinin alan adını sorgulama:
   ```bash
   nslookup 93.184.216.34
   ```

## İpuçları
- Sorgulama yapmadan önce DNS sunucusunu belirlemek, daha doğru sonuçlar almanıza yardımcı olabilir.
- `nslookup` komutunu sıkça kullanıyorsanız, bir alias oluşturarak işlemlerinizi hızlandırabilirsiniz.
- Hatalı veya geçersiz alan adları sorguladığınızda, `nslookup` hata mesajları verebilir; bu nedenle, alan adının doğru yazıldığından emin olun.