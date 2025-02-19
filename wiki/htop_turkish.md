# [Linux] C Shell (csh) htop Kullanımı: Sistem kaynaklarını izleme aracı

## Genel Bakış
htop, sistem kaynaklarını gerçek zamanlı olarak izlemek için kullanılan bir komut satırı aracıdır. Kullanıcı dostu bir arayüze sahip olan htop, CPU, bellek ve işlem bilgilerini görsel olarak sunar.

## Kullanım
htop komutunun temel sözdizimi aşağıdaki gibidir:

```csh
htop [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`, `--help`: Yardım bilgilerini gösterir.
- `-s`, `--sort`: İşlemleri belirli bir kritere göre sıralar (örneğin, CPU veya bellek kullanımı).
- `-p`, `--pid`: Belirli bir işlem kimliğini izler.
- `-u`, `--user`: Belirli bir kullanıcıya ait işlemleri gösterir.

## Yaygın Örnekler
- htop'u başlatmak için:
  ```csh
  htop
  ```

- İşlemleri CPU kullanımına göre sıralamak için:
  ```csh
  htop -s PERCENT_CPU
  ```

- Belirli bir işlem kimliğini izlemek için (örneğin, PID 1234):
  ```csh
  htop -p 1234
  ```

- Belirli bir kullanıcıya ait işlemleri görüntülemek için (örneğin, kullanıcı adı "kullanici"):
  ```csh
  htop -u kullanici
  ```

## İpuçları
- htop arayüzünde, işlemleri seçip `F9` tuşuna basarak sonlandırabilirsiniz.
- Arayüzdeki renk kodları, kaynak kullanımını hızlıca anlamanızı sağlar; yeşil CPU, mavi bellek ve kırmızı swap kullanımını temsil eder.
- htop'u daha verimli kullanmak için klavye kısayollarını öğrenmek faydalıdır; örneğin, `F3` ile arama yapabilir, `F6` ile sıralama kriterini değiştirebilirsiniz.