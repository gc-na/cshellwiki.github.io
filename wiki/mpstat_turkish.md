# [Linux] Bash mpstat Kullanımı: CPU istatistiklerini görüntüleme

## Genel Bakış
`mpstat` komutu, çok çekirdekli sistemlerde CPU kullanım istatistiklerini görüntülemek için kullanılır. Bu komut, her bir CPU çekirdeği için ayrı ayrı istatistikler sunarak sistem performansını analiz etmenize yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
mpstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-P ALL`: Tüm CPU çekirdekleri için istatistikleri gösterir.
- `-u`: CPU kullanım yüzdelerini görüntüler.
- `-h`: Çıktıyı daha okunabilir hale getirir.
- `-o`: Çıktıyı belirtilen dosyaya kaydeder.

## Yaygın Örnekler
Aşağıda `mpstat` komutunun bazı pratik kullanımları verilmiştir:

1. Tüm CPU çekirdekleri için istatistikleri görüntüleme:
   ```bash
   mpstat -P ALL
   ```

2. CPU kullanım yüzdelerini gösterme:
   ```bash
   mpstat -u
   ```

3. Çıktıyı daha okunabilir hale getirme:
   ```bash
   mpstat -h
   ```

4. Çıktıyı bir dosyaya kaydetme:
   ```bash
   mpstat -o JSON > cpu_stats.json
   ```

## İpuçları
- `mpstat` komutunu belirli aralıklarla çalıştırarak CPU kullanımını zaman içinde izleyebilirsiniz. Örneğin, her 5 saniyede bir güncel verileri görmek için:
  ```bash
  mpstat 5
  ```
- Uzun süreli izleme için çıktıyı bir dosyaya yönlendirmek, verileri daha sonra analiz etmenizi sağlar.
- CPU performansını etkileyen diğer süreçleri belirlemek için `top` veya `htop` gibi araçlarla birlikte kullanabilirsiniz.