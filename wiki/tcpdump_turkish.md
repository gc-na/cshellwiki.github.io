# [Linux] C Shell (csh) tcpdump Kullanımı: Ağ trafiğini analiz etme aracı

## Genel Bakış
tcpdump, ağ trafiğini izlemek ve analiz etmek için kullanılan güçlü bir komuttur. Ağ üzerinde geçen paketleri yakalayarak, bu paketlerin içeriğini incelemenizi sağlar. Genellikle ağ sorunlarını teşhis etmek veya güvenlik denetimleri yapmak için kullanılır.

## Kullanım
tcpdump komutunun temel sözdizimi aşağıdaki gibidir:

```bash
tcpdump [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Hangi ağ arayüzünün kullanılacağını belirtir.
- `-n`: IP adreslerini ve port numaralarını sayısal olarak gösterir, isim çözümlemesi yapmaz.
- `-c`: Belirtilen sayıda paketi yakaladıktan sonra tcpdump'ı durdurur.
- `-w`: Yakalanan verileri bir dosyaya yazmak için kullanılır.
- `-r`: Daha önce kaydedilmiş bir dosyadan paketleri okumak için kullanılır.

## Yaygın Örnekler
Aşağıda tcpdump komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm ağ trafiğini izlemek için:
   ```bash
   tcpdump -i eth0
   ```

2. Belirli bir IP adresine gelen trafiği izlemek için:
   ```bash
   tcpdump -i eth0 host 192.168.1.1
   ```

3. İlk 10 paketi yakalayıp durdurmak için:
   ```bash
   tcpdump -c 10 -i eth0
   ```

4. Yakalanan verileri bir dosyaya yazmak için:
   ```bash
   tcpdump -i eth0 -w trafi.pcap
   ```

5. Daha önce kaydedilmiş bir dosyayı okumak için:
   ```bash
   tcpdump -r trafi.pcap
   ```

## İpuçları
- tcpdump kullanırken, ağ trafiğinin yoğun olduğu zamanlarda çalıştırmak, daha fazla veri toplamanıza yardımcı olabilir.
- Yakalanan verileri analiz etmek için Wireshark gibi grafiksel araçlarla birlikte kullanabilirsiniz.
- Ağ güvenliği için tcpdump ile birlikte filtreleme seçeneklerini kullanarak yalnızca ilginç paketleri yakalayabilirsiniz.