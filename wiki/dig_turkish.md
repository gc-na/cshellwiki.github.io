# [Linux] Bash dig Kullanımı: DNS sorgulama aracı

## Genel Bakış
`dig` (Domain Information Groper), DNS (Domain Name System) sorguları yapmak için kullanılan bir komut satırı aracıdır. Bu komut, belirli bir alan adı hakkında bilgi almak için DNS sunucularına sorgular gönderir ve yanıtları kullanıcıya sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
dig [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `@sunucu`: Belirli bir DNS sunucusuna sorgu gönderir.
- `-t tür`: Sorgulamak istediğiniz kayıt türünü belirtir (örneğin, A, AAAA, MX).
- `+short`: Yanıtı daha kısa ve öz bir formatta gösterir.
- `-x IP_adresi`: Ters DNS sorgusu yaparak bir IP adresinin alan adını bulur.

## Yaygın Örnekler
Aşağıda `dig` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Temel Alan Adı Sorgulama
```
dig example.com
```
Bu komut, `example.com` alan adı için DNS kayıtlarını sorgular.

### 2. Belirli Bir DNS Sunucusuna Sorgu Gönderme
```
dig @8.8.8.8 example.com
```
Bu komut, Google'ın DNS sunucusu (8.8.8.8) üzerinden `example.com` alan adı için sorgu yapar.

### 3. Ters DNS Sorgusu
```
dig -x 8.8.8.8
```
Bu komut, 8.8.8.8 IP adresinin hangi alan adına ait olduğunu bulmak için ters DNS sorgusu yapar.

### 4. Kısa Yanıt Alma
```
dig +short example.com
```
Bu komut, `example.com` için daha kısa bir yanıt formatında bilgi alır.

### 5. Belirli Kayıt Türünü Sorgulama
```
dig -t MX example.com
```
Bu komut, `example.com` alan adı için e-posta sunucusu (MX) kayıtlarını sorgular.

## İpuçları
- `dig` komutunu sıkça kullanıyorsanız, belirli DNS sunucularını varsayılan olarak ayarlamak için bir alias oluşturabilirsiniz.
- Yanıtları daha iyi anlamak için `+trace` seçeneğini kullanarak DNS sorgusunun nasıl işlendiğini takip edebilirsiniz.
- DNS sorunlarını gidermek için `dig` komutunu kullanarak yanıt sürelerini ve kayıtları analiz edebilirsiniz.