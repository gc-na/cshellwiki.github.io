# [Linux] C Shell (csh) dig Kullanımı: DNS sorgulama aracı

## Genel Bakış
`dig` (Domain Information Groper), DNS (Domain Name System) sorguları yapmak için kullanılan bir komut satırı aracıdır. Bu araç, belirli bir alan adı hakkında bilgi almak için kullanılır ve DNS sunucularıyla etkileşimde bulunarak alan adı ile ilgili çeşitli verileri döndürür.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
dig [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `@sunucu`: Belirtilen DNS sunucusuna sorgu gönderir.
- `-t tür`: Sorgulamak istediğiniz kayıt türünü belirtir (örneğin, A, MX, CNAME).
- `+short`: Sonuçları daha kısa ve öz bir formatta gösterir.
- `+trace`: Sorgunun nasıl işlendiğini adım adım gösterir.

## Yaygın Örnekler
Aşağıda `dig` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Basit Alan Adı Sorgusu
```
dig example.com
```
Bu komut, `example.com` alan adı için varsayılan DNS kayıtlarını sorgular.

### 2. Belirli Bir DNS Sunucusuna Sorgu Göndermek
```
dig @8.8.8.8 example.com
```
Bu komut, Google'ın DNS sunucusu olan `8.8.8.8` üzerinden `example.com` için sorgu yapar.

### 3. MX Kayıtlarını Sorgulamak
```
dig -t MX example.com
```
Bu komut, `example.com` alan adı için e-posta sunucularını gösteren MX kayıtlarını sorgular.

### 4. Kısa Formatda Sonuç Alma
```
dig +short example.com
```
Bu komut, `example.com` için daha kısa ve öz bir sonuç döndürür.

### 5. Sorgu İzleme
```
dig +trace example.com
```
Bu komut, `example.com` alan adı için DNS sorgusunun nasıl işlendiğini adım adım gösterir.

## İpuçları
- Sık kullanılan DNS sunucularını (örneğin, Google DNS veya Cloudflare DNS) kullanarak sorgularınızı hızlandırabilirsiniz.
- Sorgu sonuçlarını analiz etmek için `+short` seçeneğini kullanarak daha okunabilir hale getirin.
- DNS kayıt türlerini iyi bilmek, doğru sorguları yapmanıza yardımcı olur; A, AAAA, MX, CNAME gibi kayıt türlerini öğrenin.