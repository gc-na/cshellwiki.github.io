# [Linux] Bash yes Kullanımı: Sürekli "evet" yanıtı verme

## Overview
`yes` komutu, belirli bir metni sürekli olarak çıktı olarak vermek için kullanılır. Genellikle, diğer komutlarla birlikte otomatik yanıtlar sağlamak amacıyla kullanılır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
yes [options] [arguments]
```

## Common Options
- `-n`, `--no`: "hayır" yanıtı vermek için kullanılır.
- `-h`, `--help`: Komut hakkında yardım bilgisi gösterir.
- `-V`, `--version`: Komutun sürüm bilgisini gösterir.

## Common Examples
Aşağıda `yes` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Sürekli "evet" yanıtı verme:**
   ```bash
   yes
   ```
   Bu komut, sürekli olarak "y" (evet) yanıtını verir.

2. **Belirli bir metni sürekli olarak yazdırma:**
   ```bash
   yes "Devam etmek istiyor musunuz?"
   ```
   Bu komut, "Devam etmek istiyor musunuz?" metnini sürekli olarak çıktılar.

3. **Diğer komutlarla birlikte kullanma:**
   ```bash
   yes | rm -i *.tmp
   ```
   Bu komut, `rm` komutuna sürekli "evet" yanıtı vererek tüm `.tmp` dosyalarını siler.

4. **Hayır yanıtı verme:**
   ```bash
   yes no | rm -i *.tmp
   ```
   Bu komut, `rm` komutuna sürekli "hayır" yanıtı vererek dosyaların silinmesini engeller.

## Tips
- `yes` komutunu kullanırken, dikkatli olun. Yanlışlıkla önemli dosyaları silmekten kaçınmak için komutları dikkatlice kontrol edin.
- `yes` komutunu, etkileşimli komutlarla birlikte kullanmak, otomasyon süreçlerinde oldukça faydalıdır.
- Çıktıyı bir dosyaya yönlendirmek isterseniz, `>` operatörünü kullanabilirsiniz. Örneğin: `yes "Merhaba" > merhaba.txt`.