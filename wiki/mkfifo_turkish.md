# [Linux] Bash mkfifo Kullanımı: İletişim için özel dosyalar oluşturma

## Overview
`mkfifo` komutu, özel dosyalar (FIFO - First In, First Out) oluşturmak için kullanılır. Bu dosyalar, birden fazla işlem arasında veri iletimi sağlamak için kullanılır ve veri akışını yönetmekte oldukça etkilidir.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE`: Oluşturulan FIFO dosyasının izinlerini belirler. MODE, dosya izinlerini belirtmek için kullanılabilir.
- `--help`: Komut hakkında yardım bilgilerini gösterir.
- `--version`: Komutun sürüm bilgilerini gösterir.

## Common Examples
Aşağıda `mkfifo` komutunun bazı pratik örnekleri bulunmaktadır:

1. Basit bir FIFO dosyası oluşturma:
   ```bash
   mkfifo myfifo
   ```

2. Belirli izinlerle FIFO dosyası oluşturma:
   ```bash
   mkfifo -m 644 myfifo
   ```

3. Bir FIFO dosyasını kullanarak veri gönderme ve alma:
   - Bir terminalde veri göndermek için:
     ```bash
     echo "Merhaba, FIFO!" > myfifo
     ```
   - Diğer bir terminalde veriyi okumak için:
     ```bash
     cat myfifo
     ```

4. Arka planda bir işlemle FIFO kullanma:
   ```bash
   mkfifo myfifo
   (cat myfifo) &   # Arka planda okuma işlemi
   echo "Veri gönderiliyor..." > myfifo
   ```

## Tips
- FIFO dosyalarını oluşturduktan sonra, bir işlem veriyi yazmadan önce diğer bir işlemin veriyi okumaya hazır olduğundan emin olun.
- FIFO dosyalarını yönetirken, dosya izinlerini dikkatlice ayarlamak, güvenlik açısından önemlidir.
- FIFO dosyaları, çoklu işlem senkronizasyonu için etkili bir yöntemdir; bu nedenle, karmaşık uygulamalarda kullanmayı düşünün.