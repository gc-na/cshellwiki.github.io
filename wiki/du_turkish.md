# [Linux] Bash du Kullanımı: Disk kullanımını analiz etme aracı

## Overview
`du` (disk usage) komutu, bir dosya veya dizinin disk üzerindeki kullanım alanını gösterir. Bu komut, sistem yöneticileri ve kullanıcılar için depolama alanını yönetmek ve analiz etmek amacıyla oldukça faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
du [options] [arguments]
```

## Common Options
- `-h`: İnsan tarafından okunabilir formatta çıktı verir (örneğin, KB, MB).
- `-s`: Sadece toplam boyutu gösterir, alt dizinleri göstermez.
- `-a`: Tüm dosyaların boyutlarını da gösterir, sadece dizinleri değil.
- `-c`: Toplam boyutu da içeren bir özet gösterir.
- `--max-depth=N`: Belirtilen derinlikteki dizinleri gösterir.

## Common Examples
Aşağıda `du` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Belirli bir dizinin disk kullanımını gösterme:
   ```bash
   du /path/to/directory
   ```

2. İnsan tarafından okunabilir formatta çıktı almak:
   ```bash
   du -h /path/to/directory
   ```

3. Sadece toplam boyutu gösterme:
   ```bash
   du -sh /path/to/directory
   ```

4. Tüm dosyaların boyutlarını gösterme:
   ```bash
   du -ah /path/to/directory
   ```

5. Belirli bir derinlikteki dizinleri gösterme:
   ```bash
   du --max-depth=1 /path/to/directory
   ```

## Tips
- Büyük dizinlerde `du` komutunu kullanırken, `-h` seçeneği ile çıktıyı daha okunabilir hale getirin.
- Disk alanını yönetmek için `du` çıktısını `sort` komutuyla birleştirerek en çok yer kaplayan dosya ve dizinleri kolayca bulabilirsiniz:
  ```bash
  du -ah /path/to/directory | sort -hr | head -n 10
  ```
- Düzenli olarak disk kullanımını kontrol etmek, gereksiz dosyaların temizlenmesine yardımcı olabilir.