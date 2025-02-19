# [Linux] C Shell (csh) strace Kullanımı: Sistem çağrılarını izleme aracı

## Genel Bakış
`strace`, bir programın sistem çağrılarını ve sinyallerini izlemek için kullanılan bir komuttur. Bu komut, bir uygulamanın hangi sistem kaynaklarına eriştiğini ve hangi işlemleri gerçekleştirdiğini anlamak için oldukça faydalıdır. Hata ayıklama ve performans analizi gibi durumlarda sıklıkla kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
strace [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c`: Sistem çağrılarının istatistiklerini toplar ve özetler.
- `-e`: Belirli bir sistem çağrısını izlemek için kullanılır. Örneğin, `-e trace=open` sadece `open` çağrılarını izler.
- `-o <dosya>`: Çıktıyı belirtilen dosyaya yönlendirir.
- `-p <pid>`: Belirli bir işlem kimliğini izler.

## Yaygın Örnekler
Aşağıda `strace` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Basit bir programı izlemek:
   ```csh
   strace ls
   ```

2. Çıktıyı bir dosyaya yönlendirmek:
   ```csh
   strace -o output.txt ls
   ```

3. Belirli bir sistem çağrısını izlemek:
   ```csh
   strace -e trace=open ls
   ```

4. Çalışan bir işlemi izlemek:
   ```csh
   strace -p 1234
   ```

5. İstatistikleri toplamak:
   ```csh
   strace -c ls
   ```

## İpuçları
- `strace` kullanırken, izlemek istediğiniz programın çıktısını etkileyebileceğini unutmayın. Bu nedenle, kritik uygulamalarda dikkatli olun.
- Çıktıyı dosyaya yönlendirmek, daha sonra analiz yapabilmeniz için faydalı olabilir.
- Belirli sistem çağrılarını izlemek, sorunları daha hızlı çözmenize yardımcı olabilir.