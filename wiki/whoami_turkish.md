# [Linux] Bash whoami Kullanımı: Kullanıcı adını gösterir

## Genel Bakış
`whoami` komutu, mevcut oturumda oturum açmış olan kullanıcının adını gösterir. Bu komut, kullanıcı kimliğini doğrulamak veya sistemdeki kullanıcı bilgilerini kontrol etmek için sıklıkla kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
whoami [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `--help`: Komutun kullanımını ve seçeneklerini gösterir.
- `--version`: Komutun sürüm bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `whoami` komutunun bazı pratik kullanımları bulunmaktadır:

1. Mevcut kullanıcı adını görüntüleme:
   ```bash
   whoami
   ```

2. Komutun yardım bilgilerini görüntüleme:
   ```bash
   whoami --help
   ```

3. Komutun sürüm bilgilerini kontrol etme:
   ```bash
   whoami --version
   ```

## İpuçları
- `whoami` komutunu, bir betik veya otomasyon sürecinde kullanarak hangi kullanıcı altında çalıştığınızı kontrol edebilirsiniz.
- Eğer birden fazla kullanıcı ile çalışıyorsanız, `whoami` komutunu kullanarak hangi kullanıcı ile oturum açtığınızı hızlıca öğrenebilirsiniz.