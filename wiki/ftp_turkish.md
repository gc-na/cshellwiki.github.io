# [Linux] Bash ftp Kullanımı: Dosya transferi için bir protokol

## Overview
`ftp` (File Transfer Protocol), dosyaların bir ağ üzerinden transfer edilmesini sağlayan bir protokoldür. Bu komut, kullanıcıların dosyaları uzak bir sunucuya yüklemesine veya sunucudan indirmesine olanak tanır.

## Usage
Temel kullanım sözdizimi aşağıdaki gibidir:
```bash
ftp [options] [arguments]
```

## Common Options
- `-i`: Etkileşimli moddan çıkış yapar, yani dosya transferi sırasında onay istemez.
- `-n`: Oturum açmadan önce otomatik olarak bir bağlantı kurmaz.
- `-v`: Ayrıntılı modda çalışır, daha fazla bilgi gösterir.
- `-p`: Pasif modda bağlantı kurar, bazı ağ yapılandırmaları için gereklidir.

## Common Examples
Aşağıda `ftp` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### Sunucuya Bağlanma
Bir FTP sunucusuna bağlanmak için:
```bash
ftp ftp.example.com
```

### Kullanıcı Adı ve Şifre ile Bağlanma
Kullanıcı adı ve şifre ile bağlanmak için:
```bash
ftp -n ftp.example.com
```
Ardından, `user` komutunu kullanarak kullanıcı adınızı ve şifrenizi girebilirsiniz.

### Dosya İndirme
Bir dosyayı sunucudan indirmek için:
```bash
get dosya.txt
```

### Dosya Yükleme
Bir dosyayı sunucuya yüklemek için:
```bash
put dosya.txt
```

### Tüm Dosyaları İndirme
Bir dizindeki tüm dosyaları indirmek için:
```bash
mget *
```

## Tips
- FTP bağlantısı sırasında güvenlik için mümkünse SFTP (Secure FTP) kullanmayı tercih edin.
- Dosya transferi yapmadan önce bağlantı ayarlarını kontrol edin.
- Büyük dosyalar için `-i` seçeneğini kullanarak onay istemeden transfer yapabilirsiniz.