# [Linux] Bash talk Kullanımı: İki kullanıcı arasında iletişim kurma

## Overview
`talk` komutu, iki kullanıcı arasında terminal tabanlı bir iletişim kurmak için kullanılır. Bu komut, kullanıcıların birbirleriyle gerçek zamanlı olarak metin mesajları göndermesine olanak tanır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
talk [options] [user]
```

## Common Options
- `-a`: Kullanıcının oturum açtığı terminali belirtir.
- `-m`: Mesajları yalnızca bir kez gösterir.
- `-s`: Sesli bildirimleri kapatır.

## Common Examples
1. Başka bir kullanıcıyla konuşmak için:
   ```bash
   talk kullanıcı_adı
   ```
   Bu komut, belirtilen kullanıcıyla bir konuşma penceresi açar.

2. Belirli bir terminaldeki kullanıcıyla konuşmak için:
   ```bash
   talk -a kullanıcı_adı
   ```

3. Mesajları yalnızca bir kez göstermek için:
   ```bash
   talk -m kullanıcı_adı
   ```

## Tips
- `talk` komutunu kullanmadan önce, diğer kullanıcının sistemde oturum açmış olduğundan emin olun.
- Konuşma sırasında, yazdığınız metin anında karşı tarafa iletilir, bu nedenle dikkatli olun.
- Eğer `talk` komutunu kullanamıyorsanız, kullanıcıların `write` iznine sahip olduğundan emin olun.