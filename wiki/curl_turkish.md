# [Linux] C Shell (csh) curl Kullanımı: Web'den veri almak için kullanılan bir komut

## Genel Bakış
`curl`, URL'ler üzerinden veri transferi yapmak için kullanılan bir komuttur. HTTP, HTTPS, FTP gibi çeşitli protokolleri destekler ve genellikle web'den dosya indirmek veya API'lerle etkileşimde bulunmak için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
curl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-O`: İndirilen dosyayı URL'deki adıyla kaydeder.
- `-L`: Yönlendirmeleri takip eder.
- `-d`: POST isteği ile veri gönderir.
- `-H`: HTTP başlıkları ekler.
- `-u`: Kullanıcı adı ve şifre ile kimlik doğrulaması yapar.

## Yaygın Örnekler
Aşağıda `curl` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Basit bir GET isteği
```bash
curl http://example.com
```

### 2. Dosyayı URL'den indirmek
```bash
curl -O http://example.com/dosya.txt
```

### 3. Yönlendirmeleri takip etmek
```bash
curl -L http://example.com
```

### 4. POST isteği ile veri gönderme
```bash
curl -d "param1=deger1&param2=deger2" http://example.com/api
```

### 5. Özel başlık ekleme
```bash
curl -H "Authorization: Bearer TOKEN" http://example.com/api
```

## İpuçları
- `curl` komutunu kullanırken, indirdiğiniz dosyaların güvenilir kaynaklardan geldiğinden emin olun.
- `-v` seçeneği ile ayrıntılı bilgi alarak hata ayıklama yapabilirsiniz.
- API ile çalışırken, genellikle `-H` seçeneği ile gerekli kimlik doğrulama başlıklarını eklemeyi unutmayın.