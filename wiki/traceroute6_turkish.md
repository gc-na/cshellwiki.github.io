# [Linux] C Shell (csh) traceroute6 Kullanımı: IPv6 ağ yollarını izleme aracı

## Genel Bakış
traceroute6 komutu, IPv6 ağları üzerinden bir hedefe giden yolun izlenmesini sağlar. Bu komut, ağdaki yönlendiricilerin ve geçiş noktalarının listesini göstererek, veri paketlerinin hedefe ulaşırken hangi yolları izlediğini anlamaya yardımcı olur.

## Kullanım
Komutun temel sözdizimi aşağıdaki gibidir:

```bash
traceroute6 [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-m <sayı>`: Maksimum atlama sayısını belirler.
- `-p <port>`: Hedefe gönderilecek UDP paketinin port numarasını ayarlar.
- `-w <saniye>`: Her bir atlama için bekleme süresini ayarlar.
- `-q <sayı>`: Her bir atlama için gönderilecek sorgu sayısını belirler.

## Yaygın Örnekler
Aşağıda traceroute6 komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Temel Kullanım
IPv6 adresine temel bir traceroute6 komutu ile ulaşmak için:

```bash
traceroute6 2001:db8::1
```

### Örnek 2: Maksimum Atlama Sayısını Ayarlama
Maksimum 10 atlama ile bir hedefe ulaşmak için:

```bash
traceroute6 -m 10 2001:db8::1
```

### Örnek 3: Port Numarası Belirleme
Belirli bir port numarası ile traceroute6 yapmak için:

```bash
traceroute6 -p 80 2001:db8::1
```

### Örnek 4: Bekleme Süresini Ayarlama
Her atlama için 2 saniye beklemek için:

```bash
traceroute6 -w 2 2001:db8::1
```

## İpuçları
- Ağ bağlantı sorunlarını teşhis etmek için traceroute6 komutunu kullanın; bu, sorunlu yönlendiricileri belirlemenize yardımcı olabilir.
- Hedefin IPv6 adresini doğru girdiğinizden emin olun; yanlış bir adres, sonuçları etkileyebilir.
- Daha fazla bilgi için `man traceroute6` komutunu kullanarak kılavuz sayfalarına erişebilirsiniz.