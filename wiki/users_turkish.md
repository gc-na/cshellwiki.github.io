# [Linux] Bash kullanıcıları kullanıcıları: Kullanıcı bilgilerini görüntüleme

## Genel Bakış
`users` komutu, sistemde oturum açmış olan kullanıcıların adlarını listelemek için kullanılır. Bu komut, birden fazla kullanıcı oturumu olduğunda, hangi kullanıcıların aktif olduğunu hızlı bir şekilde görmenizi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
users [seçenekler]
```

## Yaygın Seçenekler
- `-n`: Kullanıcı adlarını yalnızca bir kez gösterir, tekrar eden kullanıcı adlarını filtreler.
- `-r`: Sistem kullanıcılarını listelemek için kullanılır.

## Yaygın Örnekler
Aşağıda `users` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Tüm aktif kullanıcıları listeleme:**
   ```bash
   users
   ```

2. **Tekil kullanıcıları listeleme:**
   ```bash
   users -n
   ```

3. **Sistem kullanıcılarını listeleme:**
   ```bash
   users -r
   ```

## İpuçları
- `users` komutunu, sistemdeki kullanıcı etkinliğini izlemek için sık sık kullanabilirsiniz.
- Eğer kullanıcıların hangi terminalde oturum açtığını görmek isterseniz, `who` komutunu kullanmayı düşünebilirsiniz.
- `users` komutunu bir betik içinde kullanarak, belirli bir kullanıcı oturumunun aktif olup olmadığını kontrol edebilirsiniz.