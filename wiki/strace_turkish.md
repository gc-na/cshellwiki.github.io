# [Linux] Bash strace Kullanımı: Sistem çağrılarını izleme aracı

## Genel Bakış
`strace`, bir programın sistem çağrılarını ve sinyallerini izlemek için kullanılan güçlü bir araçtır. Bu komut, bir uygulamanın nasıl çalıştığını anlamak, hataları ayıklamak veya performans sorunlarını teşhis etmek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
strace [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-o <dosya>`: Çıktıyı belirtilen dosyaya yönlendirir.
- `-e <ifade>`: Belirli bir sistem çağrısını izlemek için filtre uygular.
- `-p <pid>`: Belirtilen işlem kimliğine (PID) bağlanır ve onu izler.
- `-c`: Sistem çağrılarının istatistiklerini toplar ve özetler.
- `-f`: Alt süreçleri de izler.

## Yaygın Örnekler
Aşağıda `strace` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Basit bir programı izlemek:**
   ```bash
   strace ls
   ```
   Bu komut, `ls` komutunun çalışması sırasında yaptığı sistem çağrılarını gösterir.

2. **Çıktıyı bir dosyaya yönlendirmek:**
   ```bash
   strace -o output.txt ls
   ```
   `ls` komutunun sistem çağrılarını `output.txt` dosyasına kaydeder.

3. **Belirli bir sistem çağrısını izlemek:**
   ```bash
   strace -e trace=open ls
   ```
   Sadece `open` sistem çağrılarını izler.

4. **Bir işlemi izlemek:**
   ```bash
   strace -p 1234
   ```
   PID'si 1234 olan bir işlemi izler.

5. **Sistem çağrılarının istatistiklerini toplamak:**
   ```bash
   strace -c ls
   ```
   `ls` komutunun sistem çağrılarıyla ilgili istatistikleri toplar ve özetler.

## İpuçları
- `strace` kullanırken, çıktının büyük olabileceğini unutmayın. Çıktıyı bir dosyaya yönlendirmek, incelemeyi kolaylaştırabilir.
- Belirli bir sistem çağrısını izlemek için `-e` seçeneğini kullanarak çıktıyı daraltabilirsiniz.
- Uzun süreli çalışan işlemleri izlerken, `-p` seçeneği ile işlem kimliğini belirlemek faydalı olabilir.
- `strace` çıktısını analiz ederken, sistem çağrılarının sırasını ve hangi hataların meydana geldiğini dikkatlice gözlemleyin.