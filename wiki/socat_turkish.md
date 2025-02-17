# [Linux] Bash socat Kullanımı: İletişim kanalları arasında veri aktarımı

## Overview
`socat`, iki veri akışını birleştiren ve bu akışlar arasında veri iletimi sağlayan bir komut satırı aracıdır. Genellikle ağ bağlantıları, dosyalar ve diğer veri kaynakları arasında köprü kurmak için kullanılır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
socat [seçenekler] [argümanlar]
```

## Common Options
- `-u`: UDP bağlantısı için kullanılır.
- `-l`: Dinleyici modunu etkinleştirir.
- `-v`: Ayrıntılı çıktı sağlar.
- `TCP:<host>:<port>`: Belirtilen host ve port'a TCP bağlantısı kurar.
- `FILE:<dosya_adı>`: Belirtilen dosyayı veri akışı olarak kullanır.

## Common Examples
Aşağıda `socat` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Basit bir TCP dinleyici oluşturma:**
   ```bash
   socat TCP-LISTEN:1234,fork EXEC:/bin/cat
   ```
   Bu komut, 1234 numaralı portta dinleyen bir TCP sunucusu oluşturur ve gelen verileri `cat` komutuna yönlendirir.

2. **Bir dosyayı TCP üzerinden iletme:**
   ```bash
   socat TCP:<hedef_ip>:<port> FILE:/path/to/file
   ```
   Belirtilen dosyayı hedef IP ve port üzerinden gönderir.

3. **UDP ile veri gönderme:**
   ```bash
   socat -u FILE:/path/to/file UDP:<hedef_ip>:<port>
   ```
   Dosyadaki verileri belirtilen hedef IP ve port'a UDP protokolü ile gönderir.

4. **İki terminal arasında iletişim kurma:**
   ```bash
   socat PTY,link=/dev/ttyS0,mode=777 PTY,link=/dev/ttyS1,mode=777
   ```
   İki sanal terminal arasında bir bağlantı kurar.

## Tips
- `socat` kullanırken, bağlantıların güvenliğini sağlamak için şifreleme ve kimlik doğrulama yöntemlerini göz önünde bulundurun.
- Dinleyici modunda çalışırken, `fork` seçeneğini kullanarak birden fazla bağlantıyı aynı anda yönetebilirsiniz.
- Hata ayıklama için `-v` seçeneğini kullanarak ayrıntılı çıktı alabilirsiniz.