# [Linux] Bash traceroute6 Kullanımı: IPv6 ağ yolunu izleme aracı

## Genel Bakış
`traceroute6`, IPv6 ağlarında veri paketlerinin hedefe ulaşırken geçtiği yolları izlemek için kullanılan bir komuttur. Bu komut, ağ bağlantılarının durumunu analiz etmek ve ağ sorunlarını teşhis etmek için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
traceroute6 [seçenekler] [hedef]
```

## Yaygın Seçenekler
- `-m <sayı>`: Maksimum atlama sayısını belirler.
- `-p <port>`: Hedefe gönderilecek UDP paketinin port numarasını ayarlar.
- `-w <saniye>`: Her bir atlama için zaman aşımını saniye cinsinden ayarlar.
- `-q <sayı>`: Her bir atlama için gönderilecek sorgu sayısını belirler.

## Yaygın Örnekler
Aşağıda `traceroute6` komutunun bazı pratik kullanımları bulunmaktadır:

### Temel Kullanım
Belirli bir hedefe giden yolu izlemek için:
```bash
traceroute6 example.com
```

### Maksimum Atlamayı Belirleme
Maksimum 15 atlama ile izleme yapmak için:
```bash
traceroute6 -m 15 example.com
```

### Belirli Bir Port ile İzleme
UDP paketini 80 numaralı port üzerinden göndermek için:
```bash
traceroute6 -p 80 example.com
```

### Zaman Aşımını Ayarlama
Her bir atlama için zaman aşımını 2 saniye olarak ayarlamak için:
```bash
traceroute6 -w 2 example.com
```

## İpuçları
- `traceroute6` komutunu çalıştırmadan önce ağ bağlantınızın aktif olduğundan emin olun.
- Hedefin IPv6 adresini kullanmak, daha doğru sonuçlar elde etmenizi sağlar.
- Ağ sorunlarını teşhis ederken, farklı seçenekleri deneyerek daha fazla bilgi edinebilirsiniz.