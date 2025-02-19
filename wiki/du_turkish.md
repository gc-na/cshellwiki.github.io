# [Linux] C Shell (csh) du Kullanımı: Disk kullanımını gösterir

## Overview
`du` (disk usage) komutu, dosya ve dizinlerin disk üzerindeki kullanım alanını gösterir. Bu komut, sistem yöneticileri ve kullanıcılar için disk alanını yönetmek ve hangi dosyaların veya dizinlerin ne kadar yer kapladığını anlamak açısından oldukça faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
du [options] [arguments]
```

## Common Options
- `-h`: İnsan tarafından okunabilir formatta çıktı verir (örneğin, KB, MB).
- `-s`: Toplam boyutu gösterir, alt dizinleri listelemez.
- `-a`: Tüm dosyaların boyutlarını gösterir, yalnızca dizinleri değil.
- `-c`: Toplam boyutu da dahil olmak üzere bir özet verir.

## Common Examples
Aşağıda `du` komutunun bazı pratik örnekleri bulunmaktadır:

1. Belirli bir dizinin disk kullanımını gösterme:
   ```csh
   du /path/to/directory
   ```

2. İnsan tarafından okunabilir formatta disk kullanımını gösterme:
   ```csh
   du -h /path/to/directory
   ```

3. Sadece toplam boyutu gösterme:
   ```csh
   du -sh /path/to/directory
   ```

4. Tüm dosyaların boyutlarını gösterme:
   ```csh
   du -a /path/to/directory
   ```

5. Toplam boyut ile birlikte özet bilgisi alma:
   ```csh
   du -ch /path/to/directory
   ```

## Tips
- Disk kullanımını analiz etmek için `du` komutunu düzenli olarak kullanmak, gereksiz dosyaları temizlemenize yardımcı olabilir.
- `du` komutunu `sort` ile birleştirerek en fazla yer kaplayan dosyaları veya dizinleri sıralayabilirsiniz:
  ```csh
  du -h /path/to/directory | sort -hr
  ```
- Büyük dizinlerde `du` komutunun çalışması zaman alabilir, bu nedenle belirli alt dizinlerle çalışmak daha hızlı sonuçlar verebilir.