# [Linux] C Shell (csh) od komutu: Verileri farklı formatlarda görüntüleme

## Overview
`od` komutu, bir dosyanın içeriğini farklı formatlarda (örneğin, onaltılık, ikilik veya ASCII) görüntülemek için kullanılır. Bu komut, özellikle dosya içeriğini analiz etmek veya hata ayıklamak için faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
od [options] [arguments]
```

## Common Options
- `-A, --address-radix=RADIX`: Adreslerin gösterim biçimini belirler. RADIX değerleri `d` (onluk), `o` (sekizlik), `x` (onaltılık) veya `n` (hiçbir şey) olabilir.
- `-t, --format=TYPE`: Çıktı formatını belirler. Örneğin, `-t x1` onaltılık tek bayt gösterimi yapar.
- `-v, --output-duplicates`: Tekrar eden verileri de gösterir.
- `-N, --read-bytes=N`: Sadece ilk N baytı okur.

## Common Examples
Aşağıda `od` komutunun bazı pratik örnekleri bulunmaktadır:

1. Bir dosyanın içeriğini onaltılık formatta görüntülemek:
   ```bash
   od -x dosya.txt
   ```

2. Bir dosyanın içeriğini ASCII formatında görüntülemek:
   ```bash
   od -c dosya.txt
   ```

3. Sadece ilk 16 baytı onaltılık formatta görüntülemek:
   ```bash
   od -N 16 -x dosya.txt
   ```

4. Bir dosyanın içeriğini sekizlik formatta görüntülemek:
   ```bash
   od -o dosya.txt
   ```

## Tips
- `od` komutunu kullanırken, dosya boyutunu ve içeriğini göz önünde bulundurun; büyük dosyalar için çıktıyı filtrelemek yararlı olabilir.
- Çıktıyı daha okunabilir hale getirmek için farklı format seçeneklerini deneyin.
- Hata ayıklama sırasında, `-v` seçeneğini kullanarak tüm verileri görmek, sorunları tespit etmenize yardımcı olabilir.