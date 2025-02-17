# [Linux] Bash sftp Kullanımı: Dosya aktarımı için güvenli bir protokol

## Genel Bakış
`sftp` (Secure File Transfer Protocol), güvenli bir dosya aktarım protokolüdür. SSH (Secure Shell) üzerinden çalışarak, kullanıcıların dosyaları güvenli bir şekilde uzak sunuculara yüklemelerine veya bu sunuculardan indirmelerine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
sftp [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-o`: Seçenekleri belirtmek için kullanılır.
- `-P`: Uzak sunucunun port numarasını belirtir.
- `-v`: Ayrıntılı hata ayıklama çıktısı sağlar.

## Yaygın Örnekler
1. Uzak bir sunucuya bağlanmak:
   ```bash
   sftp kullanıcı_adı@sunucu_adresi
   ```

2. Dosya indirmek:
   ```bash
   sftp kullanıcı_adı@sunucu_adresi:/uzak/dosya.txt /yerel/dosya.txt
   ```

3. Dosya yüklemek:
   ```bash
   sftp /yerel/dosya.txt kullanıcı_adı@sunucu_adresi:/uzak/dosya.txt
   ```

4. Tüm dosyaları bir dizinden indirmek:
   ```bash
   sftp kullanıcı_adı@sunucu_adresi
   get * /yerel/dizin/
   ```

## İpuçları
- Bağlantı kurmadan önce SSH anahtarınızı ayarlamak, şifre girmeden bağlanmanıza yardımcı olur.
- `lcd` komutunu kullanarak yerel dizini değiştirebilir ve dosyaları daha kolay yönetebilirsiniz.
- `exit` veya `bye` komutları ile sftp oturumunu kapatmayı unutmayın.