# [Linux] Bash yazma komutu: Kullanıcılarla mesajlaşma

## Genel Bakış
`write` komutu, bir terminal oturumundaki kullanıcılarla doğrudan mesajlaşmanızı sağlar. Bu komut, belirli bir kullanıcıya veya tüm kullanıcılara metin göndermenize olanak tanır. Mesajlar, alıcı kullanıcının terminalinde anında görüntülenir.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
write [kullanıcı_adı] [terminal]
```

Eğer terminal belirtilmezse, varsayılan terminal kullanılır.

## Yaygın Seçenekler
- `-n`: Kullanıcı adını belirtmeden mesaj gönderir.
- `-h`: Mesajın hangi terminalde gönderileceğini belirtir.

## Yaygın Örnekler
1. Belirli bir kullanıcıya mesaj göndermek:
   ```bash
   write ahmet
   Merhaba Ahmet, nasılsın?
   ```

2. Kullanıcının terminaline mesaj göndermek için:
   ```bash
   write ahmet pts/1
   Toplantı saat 3'te başlayacak.
   ```

3. Tüm kullanıcılara mesaj göndermek için:
   ```bash
   wall
   Dikkat! Sistem bakımı nedeniyle 10 dakika içinde hizmet kesintisi olacaktır.
   ```

## İpuçları
- `write` komutunu kullanmadan önce, alıcı kullanıcının terminalinin açık olduğundan emin olun.
- Mesaj göndermeden önce, alıcı kullanıcının `mesg` komutunu kullanarak mesaj almayı kabul ettiğinden emin olun.
- Mesajınızı kısa ve öz tutarak, alıcıyı rahatsız etmemeye çalışın.