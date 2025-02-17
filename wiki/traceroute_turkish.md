# [Linux] Bash traceroute Kullanımı: Ağ yolunu izleme aracı

## Overview
`traceroute` komutu, bir ağ üzerindeki bir hedefe ulaşmak için geçen yolları ve bu yollar üzerindeki her bir ara noktayı (router) gösterir. Bu, ağ bağlantı sorunlarını teşhis etmek ve ağ performansını analiz etmek için yararlıdır.

## Usage
Temel kullanım sözdizimi aşağıdaki gibidir:

```bash
traceroute [seçenekler] [hedef]
```

## Common Options
- `-m <sayı>`: Maksimum sıçrama sayısını belirler.
- `-p <port>`: Hedefe ulaşmak için kullanılacak port numarasını ayarlar.
- `-n`: IP adreslerini çözümlemeden doğrudan gösterir.
- `-I`: ICMP ECHO isteği kullanarak izleme yapar (varsayılan UDP yerine).
- `-w <saniye>`: Her bir sıçrama için zaman aşımını ayarlar.

## Common Examples
Aşağıda `traceroute` komutunun bazı pratik örnekleri verilmiştir:

1. Temel bir traceroute:
   ```bash
   traceroute example.com
   ```

2. Maksimum 10 sıçrama ile traceroute:
   ```bash
   traceroute -m 10 example.com
   ```

3. Belirli bir port üzerinden traceroute:
   ```bash
   traceroute -p 80 example.com
   ```

4. IP adreslerini çözümlemeden traceroute:
   ```bash
   traceroute -n example.com
   ```

5. ICMP ECHO isteği ile traceroute:
   ```bash
   traceroute -I example.com
   ```

## Tips
- Ağ sorunlarını teşhis ederken, `-n` seçeneğini kullanarak daha hızlı sonuçlar alabilirsiniz.
- Farklı protokollerle (UDP veya ICMP) denemeler yaparak, ağınızdaki sorunları daha iyi anlayabilirsiniz.
- `traceroute` çıktısını analiz ederken, her bir sıçramanın yanındaki süreleri dikkate alarak hangi noktada gecikme yaşandığını belirleyebilirsiniz.