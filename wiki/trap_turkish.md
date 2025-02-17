# [Linux] Bash trap Kullanımı: Hataları ve sinyalleri yakalama

## Overview
`trap` komutu, bir Bash betiği çalışırken belirli sinyalleri veya hata durumlarını yakalamak için kullanılır. Bu sayede, programın beklenmedik bir şekilde sonlanmasını önleyebilir ve temizleme işlemleri yapabilirsiniz.

## Usage
Temel sözdizimi şu şekildedir:
```bash
trap [options] [arguments]
```

## Common Options
- `SIGINT`: Kullanıcı tarafından Ctrl+C ile gönderilen kesme sinyali.
- `SIGTERM`: Programın sonlandırılması için gönderilen sinyal.
- `EXIT`: Betik sona erdiğinde çalıştırılacak komutlar.
- `ERR`: Bir hata oluştuğunda çalıştırılacak komutlar.

## Common Examples

### Örnek 1: Basit bir sinyal yakalama
Aşağıdaki örnekte, `SIGINT` sinyali yakalanır ve kullanıcı Ctrl+C tuşuna bastığında bir mesaj yazdırılır.
```bash
#!/bin/bash
trap 'echo "Ctrl+C tuşuna basıldı!"' SIGINT
while true; do
    sleep 1
done
```

### Örnek 2: Betik sona erdiğinde temizleme işlemi
Bu örnekte, betik sona erdiğinde geçici dosyaların silinmesi sağlanır.
```bash
#!/bin/bash
trap 'rm -f /tmp/tempfile; echo "Geçici dosya silindi."' EXIT
touch /tmp/tempfile
echo "Betik çalışıyor..."
sleep 5
```

### Örnek 3: Hata durumunda işlem yapma
Aşağıdaki örnekte, bir hata oluştuğunda bir mesaj yazdırılır.
```bash
#!/bin/bash
trap 'echo "Bir hata oluştu!"' ERR
false  # Bu komut hata döndürür
```

## Tips
- `trap` komutunu kullanarak betiklerinizin daha dayanıklı olmasını sağlayabilirsiniz.
- Hangi sinyalleri yakalamak istediğinizi iyi belirleyin; gereksiz sinyalleri yakalamak karmaşaya neden olabilir.
- Temizleme işlemlerini `EXIT` ile tanımlamak, betik sona erdiğinde kaynakların düzgün bir şekilde serbest bırakılmasını sağlar.