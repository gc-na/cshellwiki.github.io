# [Linux] Bash gzip Kullanımı: Dosyaları sıkıştırma aracı

## Overview
`gzip`, dosyaları sıkıştırmak için kullanılan bir komut satırı aracıdır. Genellikle dosya boyutunu azaltmak ve disk alanından tasarruf sağlamak amacıyla kullanılır. Sıkıştırılmış dosyalar genellikle `.gz` uzantısına sahip olur.

## Usage
Temel kullanım senaryosu aşağıdaki gibidir:

```bash
gzip [options] [arguments]
```

## Common Options
- `-d` veya `--decompress`: Sıkıştırılmış dosyayı açar.
- `-k` veya `--keep`: Sıkıştırma işlemi sırasında orijinal dosyayı korur.
- `-v` veya `--verbose`: İşlem sırasında daha fazla bilgi gösterir.
- `-r` veya `--recursive`: Belirtilen dizindeki tüm alt dizinlerdeki dosyaları sıkıştırır.

## Common Examples
Aşağıda `gzip` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Bir dosyayı sıkıştırmak:
   ```bash
   gzip dosya.txt
   ```

2. Sıkıştırılmış bir dosyayı açmak:
   ```bash
   gzip -d dosya.txt.gz
   ```

3. Orijinal dosyayı koruyarak sıkıştırmak:
   ```bash
   gzip -k dosya.txt
   ```

4. Bir dizindeki tüm dosyaları sıkıştırmak:
   ```bash
   gzip -r dizin_adi/
   ```

5. Sıkıştırma işlemi sırasında bilgi göstermek:
   ```bash
   gzip -v dosya.txt
   ```

## Tips
- Sıkıştırılmış dosyaların boyutunu kontrol etmek için `ls -lh` komutunu kullanabilirsiniz.
- Sıkıştırma işlemi sırasında dosya kaybı olmaması için `-k` seçeneğini kullanarak orijinal dosyayı saklayabilirsiniz.
- Büyük dosyalarla çalışırken, sıkıştırma işleminin zaman alabileceğini unutmayın; bu nedenle işlem sırasında sabırlı olun.