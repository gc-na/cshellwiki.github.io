# [Linux] C Shell (csh) sftp Kullanımı: Dosya transferi için güvenli bir protokol

## Genel Bakış
`sftp` (Secure File Transfer Protocol), dosyaları güvenli bir şekilde bir ağ üzerinden aktarmak için kullanılan bir komuttur. SSH (Secure Shell) protokolü üzerine inşa edilmiştir ve dosya transferi sırasında verilerin şifrelenmesini sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
sftp [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-o`: Belirli bir seçenek ayarlamak için kullanılır.
- `-P`: Bağlantı için kullanılacak port numarasını belirtir.
- `-v`: Ayrıntılı çıktı almak için kullanılır; hata ayıklama amacıyla faydalıdır.

## Yaygın Örnekler
Aşağıda `sftp` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Bir sunucuya bağlanmak:**
   ```bash
   sftp kullanıcı_adı@sunucu_adresi
   ```

2. **Bir dosyayı indirmek:**
   ```bash
   sftp kullanıcı_adı@sunucu_adresi:/uzak/dosya.txt /yerel/dosya.txt
   ```

3. **Bir dosyayı yüklemek:**
   ```bash
   sftp /yerel/dosya.txt kullanıcı_adı@sunucu_adresi:/uzak/dosya.txt
   ```

4. **Bir dizini listelemek:**
   ```bash
   sftp kullanıcı_adı@sunucu_adresi
   ls
   ```

## İpuçları
- Bağlantı sırasında sık sık hata alıyorsanız, sunucu adresini ve kullanıcı adını kontrol edin.
- Dosya transferi yapmadan önce, dosya izinlerini kontrol etmek iyi bir uygulamadır.
- `-v` seçeneğini kullanarak bağlantı sürecini daha iyi anlayabilir ve sorunları daha kolay tespit edebilirsiniz.