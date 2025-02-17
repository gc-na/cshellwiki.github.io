# [Linux] Bash netcat Kullanımı: Ağ bağlantıları oluşturma ve veri iletimi

## Genel Bakış
Netcat, ağ bağlantıları oluşturmak ve veri iletimi yapmak için kullanılan güçlü bir araçtır. TCP veya UDP protokollerini kullanarak, iki bilgisayar arasında veri göndermek veya almak için kullanılabilir. Genellikle ağ testleri, hata ayıklama ve güvenlik araştırmaları için tercih edilir.

## Kullanım
Netcat komutunun temel sözdizimi aşağıdaki gibidir:

```bash
netcat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Dinleme modunu etkinleştirir. Gelen bağlantıları bekler.
- `-p`: Dinleme portunu belirtir.
- `-u`: UDP protokolünü kullanır.
- `-v`: Ayrıntılı (verbose) modda çalışır, daha fazla bilgi gösterir.
- `-z`: Sadece bağlantı kontrolü yapar, veri göndermez.

## Yaygın Örnekler

### 1. Basit bir TCP bağlantısı oluşturma
Aşağıdaki komut, belirtilen bir IP adresine ve porta TCP bağlantısı kurar:

```bash
netcat 192.168.1.10 8080
```

### 2. Dinleyici oluşturma
Aşağıdaki komut, 1234 numaralı portta dinleyen bir netcat örneği başlatır:

```bash
netcat -l -p 1234
```

### 3. UDP ile veri gönderme
UDP protokolü kullanarak veri göndermek için aşağıdaki komutu kullanabilirsiniz:

```bash
echo "Merhaba, dünya!" | netcat -u 192.168.1.10 1234
```

### 4. Dosya transferi
Bir dosyayı başka bir makineye göndermek için şu adımları izleyebilirsiniz:

**Gönderen:**
```bash
netcat -l -p 1234 < dosya.txt
```

**Alıcı:**
```bash
netcat 192.168.1.10 1234 > dosya.txt
```

## İpuçları
- Netcat'i güvenlik testleri için kullanırken dikkatli olun; yetkisiz erişim veya veri sızıntısına neden olabilirsiniz.
- Dinleyici modda çalışırken, port numarasının başka bir uygulama tarafından kullanılmadığından emin olun.
- Netcat'i bir arka plan süreci olarak çalıştırmak için `&` işaretini kullanabilirsiniz. Örneğin: `netcat -l -p 1234 &`
- Ağ trafiğini izlemek için `-v` seçeneğini ekleyerek daha fazla bilgi alabilirsiniz.