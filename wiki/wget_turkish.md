# [Linux] C Shell (csh) wget Kullanımı: Dosya indirme aracı

## Genel Bakış
`wget`, web üzerinden dosya indirmek için kullanılan güçlü bir komuttur. HTTP, HTTPS ve FTP protokollerini destekler ve kullanıcıların dosyaları kolayca indirmesine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
wget [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-O [dosya_adı]`: İndirilen dosyayı belirtilen isimle kaydeder.
- `-c`: Kesilen bir indirmeyi devam ettirir.
- `-r`: Belirtilen URL'den tüm bağlantılı dosyaları indirir (rekürsif).
- `-q`: Sessiz modda çalışır, yalnızca hata mesajlarını gösterir.
- `--limit-rate=[hız]`: İndirme hızını sınırlar.

## Yaygın Örnekler
- Basit bir dosya indirme:
```bash
wget http://example.com/dosya.zip
```

- İndirilen dosyayı farklı bir isimle kaydetme:
```bash
wget -O yeni_dosya.zip http://example.com/dosya.zip
```

- İndirilen dosyayı kesintiden sonra devam ettirme:
```bash
wget -c http://example.com/büyük_dosya.zip
```

- Rekürsif olarak bir web sitesinden tüm dosyaları indirme:
```bash
wget -r http://example.com/
```

- İndirme hızını sınırlama:
```bash
wget --limit-rate=200k http://example.com/dosya.zip
```

## İpuçları
- İndirme işlemlerini arka planda gerçekleştirmek için `-b` seçeneğini kullanabilirsiniz.
- İndirme işlemlerini bir dosyaya kaydetmek için `-o [log_dosya]` seçeneğini kullanarak hata ve bilgi mesajlarını takip edebilirsiniz.
- Büyük dosyaları indirirken `-c` seçeneği ile kesintisiz bir deneyim sağlayabilirsiniz.