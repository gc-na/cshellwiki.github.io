# [Linux] Bash wget Kullanımı: Dosya indirme aracı

## Genel Bakış
`wget`, web üzerinden dosya indirmek için kullanılan güçlü bir komut satırı aracıdır. HTTP, HTTPS ve FTP protokollerini destekler, bu sayede kullanıcıların internetten dosya indirmelerini kolaylaştırır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
wget [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-O [dosya_adı]`: İndirilen dosyanın adını belirler.
- `-c`: Kesilen bir indirmeyi devam ettirir.
- `-r`: Belirtilen URL'den tüm bağlantıları takip ederek indirme işlemi yapar (rekürsif indirme).
- `-q`: Sessiz modda çalışır, yalnızca hata mesajlarını gösterir.
- `--limit-rate=[hız]`: İndirme hızını sınırlar.

## Yaygın Örnekler
1. Basit bir dosya indirme:
   ```bash
   wget https://example.com/dosya.zip
   ```

2. İndirilen dosyaya özel bir ad verme:
   ```bash
   wget -O yeni_ad.zip https://example.com/dosya.zip
   ```

3. Kesilen bir indirmeyi devam ettirme:
   ```bash
   wget -c https://example.com/dosya.zip
   ```

4. Rekürsif indirme:
   ```bash
   wget -r https://example.com/
   ```

5. İndirme hızını sınırlama:
   ```bash
   wget --limit-rate=200k https://example.com/dosya.zip
   ```

## İpuçları
- İndirme işlemi sırasında internet bağlantınız kesilirse, `-c` seçeneği ile indirmeyi kaldığınız yerden devam ettirebilirsiniz.
- Büyük dosyalar indirirken `--limit-rate` seçeneği ile ağ trafiğinizi yönetebilirsiniz.
- `-q` seçeneği ile gereksiz bilgi akışını azaltarak daha temiz bir çıktı alabilirsiniz.