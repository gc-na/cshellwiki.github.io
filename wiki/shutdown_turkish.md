# [Linux] C Shell (csh) shutdown Kullanımı: Sistemi kapatma komutu

## Genel Bakış
`shutdown` komutu, bir Unix veya Linux sistemini güvenli bir şekilde kapatmak için kullanılır. Bu komut, sistemin kapanma sürecini başlatır ve kullanıcıları bilgilendirir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
shutdown [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: Sistemi kapatır.
- `-r`: Sistemi yeniden başlatır.
- `now`: Hemen kapatmayı başlatır.
- `+m`: Belirtilen dakika sayısı sonra kapatır.

## Yaygın Örnekler
Aşağıda `shutdown` komutunun bazı pratik örnekleri verilmiştir:

1. Sistemi hemen kapatmak için:
   ```csh
   shutdown -h now
   ```

2. Sistemi 5 dakika sonra kapatmak için:
   ```csh
   shutdown -h +5
   ```

3. Sistemi hemen yeniden başlatmak için:
   ```csh
   shutdown -r now
   ```

4. Sistemi 10 dakika sonra yeniden başlatmak için:
   ```csh
   shutdown -r +10
   ```

## İpuçları
- Kapatma işlemi öncesinde kullanıcıları bilgilendirmek için bir mesaj ekleyebilirsiniz. Örneğin:
  ```csh
  shutdown -h +5 "Sistem 5 dakika içinde kapanacaktır. Lütfen çalışmanızı kaydedin."
  ```
- Sistem kapanmadan önce açık olan uygulamaları kapatmayı unutmayın, böylece veri kaybını önleyebilirsiniz.
- `shutdown` komutunu kullanmadan önce, yeterli izinlere sahip olduğunuzdan emin olun; genellikle bu komut için yönetici (root) yetkileri gereklidir.