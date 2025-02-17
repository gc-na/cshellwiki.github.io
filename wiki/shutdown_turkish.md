# [Linux] Bash kapatma kullanımı: Sistemi kapatmak için kullanılır

## Genel Bakış
`shutdown` komutu, bir Linux veya Unix tabanlı sistemin güvenli bir şekilde kapatılmasını sağlar. Bu komut, sistem yöneticilerine belirli bir süre içinde veya hemen kapatma işlemi gerçekleştirme imkanı sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
shutdown [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: Sistemi kapatır.
- `-r`: Sistemi yeniden başlatır.
- `now`: Anında kapatma işlemi yapar.
- `+m`: M dakika sonra kapatma işlemi yapar (örneğin, `+5` 5 dakika sonra kapatır).
- `hh:mm`: Belirtilen saatte kapatma işlemi yapar (örneğin, `23:00` 11:00'de kapatır).

## Yaygın Örnekler
Aşağıda `shutdown` komutunun bazı pratik örnekleri verilmiştir:

1. Sistemi hemen kapatmak için:
   ```bash
   shutdown now
   ```

2. Sistemi 5 dakika sonra kapatmak için:
   ```bash
   shutdown +5
   ```

3. Sistemi belirli bir saatte kapatmak için:
   ```bash
   shutdown 23:00
   ```

4. Sistemi yeniden başlatmak için:
   ```bash
   shutdown -r now
   ```

## İpuçları
- Kapatma işlemi yapmadan önce açık olan uygulamaları kontrol edin, böylece veri kaybını önleyebilirsiniz.
- `shutdown` komutunu kullanmadan önce, sistemdeki diğer kullanıcıları bilgilendirmek için `wall` komutunu kullanarak bir mesaj gönderebilirsiniz.
- Kapatma işlemini iptal etmek için `shutdown -c` komutunu kullanabilirsiniz.