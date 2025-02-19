# [Linux] C Shell (csh) mkfifo Kullanımı: İletişim için özel dosyalar oluşturma

## Overview
`mkfifo` komutu, adlandırılmış bir boru (FIFO - First In First Out) oluşturmak için kullanılır. Bu, birden fazla işlem arasında veri iletimi sağlamak için kullanılan özel bir dosya türüdür.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
mkfifo [options] [arguments]
```

## Common Options
- `-m` : Oluşturulan FIFO dosyasının izinlerini belirtmek için kullanılır.
- `-Z` : SELinux güvenlik bağlamı ayarlamak için kullanılır.

## Common Examples
Aşağıda `mkfifo` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Basit bir FIFO dosyası oluşturma:
   ```csh
   mkfifo myfifo
   ```

2. Belirli izinlerle FIFO dosyası oluşturma:
   ```csh
   mkfifo -m 644 myfifo
   ```

3. Birden fazla FIFO dosyası oluşturma:
   ```csh
   mkfifo fifo1 fifo2 fifo3
   ```

4. SELinux güvenlik bağlamı ile FIFO dosyası oluşturma:
   ```csh
   mkfifo -Z myfifo
   ```

## Tips
- FIFO dosyalarını kullanırken, bir işlem veriyi yazmadan önce diğerinin okuma işlemini başlatmış olması gerektiğini unutmayın.
- FIFO dosyalarını temizlemek için `rm` komutunu kullanabilirsiniz.
- FIFO dosyaları, özellikle çoklu işlem iletişimi gerektiren durumlarda oldukça faydalıdır.