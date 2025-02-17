# [Linux] Bash tcpdump Kullanımı: Ağ trafiğini analiz etme aracı

## Genel Bakış
`tcpdump`, ağ trafiğini analiz etmek için kullanılan bir komut satırı aracıdır. Ağ üzerinden geçen paketleri yakalayarak, bu paketlerin içeriğini incelemenizi sağlar. Ağ sorunlarını teşhis etmek, güvenlik analizi yapmak veya ağ trafiğini izlemek için oldukça yararlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
tcpdump [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i [arayüz]`: Hangi ağ arayüzünün dinleneceğini belirtir.
- `-n`: IP adreslerini ve port numaralarını sayısal olarak gösterir, isim çözümlemesi yapmaz.
- `-v`, `-vv`, `-vvv`: Çıktının ayrıntı düzeyini artırır.
- `-c [sayı]`: Belirtilen sayıda paketi yakaladıktan sonra işlemi durdurur.
- `-w [dosya]`: Yakalanan paketleri belirtilen dosyaya yazar.

## Yaygın Örnekler
Aşağıda `tcpdump` komutunun bazı pratik kullanımları verilmiştir:

### 1. Tüm ağ trafiğini dinleme
```bash
tcpdump
```

### 2. Belirli bir arayüzde dinleme
```bash
tcpdump -i eth0
```

### 3. IP adresi çözümlemesi yapmadan dinleme
```bash
tcpdump -n
```

### 4. Belirli bir sayıda paketi yakalama
```bash
tcpdump -c 10
```

### 5. Yakalanan verileri bir dosyaya yazma
```bash
tcpdump -w yakalanan_paketler.pcap
```

## İpuçları
- `tcpdump` kullanırken, yalnızca gerekli verileri yakalamak için filtreler eklemeyi düşünün. Bu, çıktıyı daha yönetilebilir hale getirir.
- Ağ trafiğini analiz ederken, ağ güvenliği ile ilgili bilgileri gizli tutmaya özen gösterin.
- Yakalanan verileri analiz etmek için Wireshark gibi grafiksel araçlarla birlikte kullanabilirsiniz.