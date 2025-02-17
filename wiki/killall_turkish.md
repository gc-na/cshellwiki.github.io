# [Linux] Bash killall Kullanımı: Birden Fazla Süreci Sonlandırma

## Genel Bakış
`killall` komutu, belirtilen isimle çalışan tüm süreçleri sonlandırmak için kullanılır. Bu komut, belirli bir uygulamanın veya işlemin tüm örneklerini hızlı bir şekilde kapatmak için oldukça etkilidir.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
killall [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u, --user`: Belirtilen kullanıcıya ait süreçleri sonlandırır.
- `-9, --signal SIGKILL`: Süreçleri zorla sonlandırmak için kullanılır.
- `-q, --quiet`: Çıktıyı sessiz hale getirir, yani hata mesajlarını göstermez.
- `-r, --regexp`: Süreç adını bir düzenli ifade olarak yorumlar.

## Yaygın Örnekler
Aşağıda `killall` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Belirli bir uygulamayı sonlandırma**:
   ```bash
   killall firefox
   ```
   Bu komut, çalışan tüm Firefox süreçlerini kapatır.

2. **Bir kullanıcıya ait süreçleri sonlandırma**:
   ```bash
   killall -u kullanıcı_adı
   ```
   Bu, belirtilen kullanıcıya ait tüm süreçleri sonlandırır.

3. **Zorla bir süreci sonlandırma**:
   ```bash
   killall -9 chrome
   ```
   Bu komut, çalışan tüm Chrome süreçlerini zorla kapatır.

4. **Düzenli ifade kullanarak süreçleri sonlandırma**:
   ```bash
   killall -r '^myapp.*'
   ```
   Bu, adı "myapp" ile başlayan tüm süreçleri sonlandırır.

## İpuçları
- `killall` komutunu kullanmadan önce hangi süreçlerin çalıştığını görmek için `ps` veya `pgrep` komutlarını kullanabilirsiniz.
- Süreçleri sonlandırmadan önce, önemli verilerin kaybolmaması için açık olan dosyaları kaydettiğinizden emin olun.
- `killall` komutunu kullanırken dikkatli olun; yanlış bir süreç adı girdiğinizde istemeden önemli bir uygulamayı kapatabilirsiniz.