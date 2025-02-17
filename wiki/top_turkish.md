# [Linux] Bash top Kullanımı: Sistem kaynaklarını izleme aracı

## Genel Bakış
`top` komutu, sistemdeki işlemci ve bellek kullanımını gerçek zamanlı olarak izlemek için kullanılan bir araçtır. Bu komut, sistemdeki aktif işlemleri ve bu işlemlerin kaynak tüketimini gösterir, böylece kullanıcılar sistem performansını değerlendirebilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
top [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-d [saniye]`: Güncellemelerin ne sıklıkta yapılacağını belirler. Varsayılan değer 3 saniyedir.
- `-p [PID]`: Belirtilen işlem kimliğini (PID) izler.
- `-u [kullanıcı]`: Belirtilen kullanıcıya ait işlemleri gösterir.
- `-n [sayı]`: Belirtilen sayıda güncelleme yaparak çıkış yapar.

## Yaygın Örnekler
1. **Temel top komutu**: Sistemdeki tüm işlemleri ve kaynak kullanımını görüntülemek için:
   ```bash
   top
   ```

2. **Güncelleme süresini ayarlamak**: Her 5 saniyede bir güncelleme yapmak için:
   ```bash
   top -d 5
   ```

3. **Belirli bir PID'yi izlemek**: PID'si 1234 olan işlemi izlemek için:
   ```bash
   top -p 1234
   ```

4. **Belirli bir kullanıcıya ait işlemleri görüntülemek**: "kullanici1" adlı kullanıcıya ait işlemleri görmek için:
   ```bash
   top -u kullanici1
   ```

5. **Sadece 10 güncelleme yaparak çıkmak**: 10 güncelleme yaptıktan sonra çıkmak için:
   ```bash
   top -n 10
   ```

## İpuçları
- `top` arayüzünde, `h` tuşuna basarak yardım alabilirsiniz.
- `k` tuşuna basarak bir işlemi sonlandırmak için PID'yi girebilirsiniz.
- `M` tuşuna basarak işlemleri bellek kullanımına göre sıralayabilirsiniz.
- `P` tuşuna basarak işlemleri CPU kullanımına göre sıralayabilirsiniz.

Bu bilgilerle `top` komutunu etkili bir şekilde kullanarak sisteminizin performansını izleyebilirsiniz.