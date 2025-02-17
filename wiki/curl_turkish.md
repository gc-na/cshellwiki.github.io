# [Linux] Bash curl Kullanımı: HTTP istekleri yapmak için kullanılan bir araç

## Genel Bakış
`curl`, URL'ler üzerinden veri transferi yapmak için kullanılan bir komut satırı aracıdır. HTTP, HTTPS, FTP gibi çeşitli protokollerle çalışabilir ve genellikle web API'leri ile etkileşimde bulunmak için kullanılır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
curl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-X, --request`: Belirtilen HTTP metodunu kullanır (GET, POST, PUT, DELETE vb.).
- `-d, --data`: POST isteği ile gönderilecek veriyi belirtir.
- `-H, --header`: İsteğe özel başlık ekler.
- `-o, --output`: Yanıtı belirtilen dosyaya kaydeder.
- `-I, --head`: Sadece başlık bilgilerini alır.

## Yaygın Örnekler
Aşağıda `curl` komutunun bazı pratik kullanım örnekleri verilmiştir:

### 1. Basit GET İsteği
Bir web sayfasının içeriğini almak için:
```bash
curl https://www.example.com
```

### 2. POST İsteği ile Veri Gönderme
Bir API'ye veri göndermek için:
```bash
curl -X POST -d "name=John&age=30" https://api.example.com/users
```

### 3. Özel Başlık Ekleme
Bir isteğe özel başlık eklemek için:
```bash
curl -H "Authorization: Bearer TOKEN" https://api.example.com/protected
```

### 4. Yanıtı Dosyaya Kaydetme
Bir dosyayı indirmek için:
```bash
curl -o dosya.txt https://www.example.com/dosya.txt
```

### 5. Sadece Başlık Bilgilerini Alma
Bir URL'nin başlık bilgilerini almak için:
```bash
curl -I https://www.example.com
```

## İpuçları
- `-s` seçeneğini kullanarak `curl` çıktısını sessiz hale getirebilirsiniz. Bu, yalnızca yanıtı görmek istediğinizde faydalıdır.
- `-L` seçeneği, yönlendirmeleri takip etmenizi sağlar. Bir URL başka bir URL'ye yönlendiriliyorsa, bu seçeneği kullanmalısınız.
- API'lerle çalışırken, genellikle JSON formatında veri gönderip alırsınız. Bu durumda, `-H "Content-Type: application/json"` başlığını eklemeyi unutmayın.