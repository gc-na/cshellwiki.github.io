# [Linux] Bash mtr Kullanımı: Ağ bağlantı durumu ve yol izleme

## Overview
mtr (My Traceroute), ağ bağlantı durumu ve yol izleme aracı olarak kullanılan bir komut satırı aracıdır. mtr, bir hedefe olan bağlantının kalitesini ve yolunu analiz ederek, ağdaki olası sorunları tespit etmeye yardımcı olur.

## Usage
Temel komut yapısı aşağıdaki gibidir:

```
mtr [options] [arguments]
```

## Common Options
- `-r`: Rapor modunu etkinleştirir, sonuçları bir rapor şeklinde gösterir.
- `-c <count>`: Belirtilen sayıda ping gönderir ve ardından çıkış yapar.
- `-i <interval>`: Ping gönderme aralığını saniye cinsinden ayarlar.
- `-p`: Port numarasını belirtir, varsayılan olarak 33434 kullanılır.
- `-n`: IP adreslerini çözümlemeden gösterir, bu sayede daha hızlı sonuç alırsınız.

## Common Examples
Aşağıda mtr komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### Temel Kullanım
Belirli bir hedefe (örneğin, google.com) mtr ile bağlantı durumu kontrolü:
```bash
mtr google.com
```

### Rapor Modu
Sonuçları rapor formatında almak için:
```bash
mtr -r google.com
```

### Belirli Sayıda Ping Gönderme
5 ping gönderip sonuçları gösterme:
```bash
mtr -c 5 google.com
```

### IP Çözümlemesi Yapmadan Kullanma
IP adreslerini çözümlemeden doğrudan kullanmak için:
```bash
mtr -n google.com
```

## Tips
- mtr komutunu kullanırken, ağ bağlantı sorunlarını tespit etmek için farklı hedefler üzerinde denemeler yapın.
- Sonuçları daha iyi analiz edebilmek için `-r` seçeneği ile rapor modunu kullanın.
- Ping aralığını ayarlamak için `-i` seçeneğini kullanarak belirli bir süre aralığında test yapabilirsiniz.