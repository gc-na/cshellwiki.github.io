# [Linux] Bash exec Kullanımı: Komutları çalıştırma

## Genel Bakış
`exec` komutu, mevcut shell oturumunda yeni bir komut çalıştırmak için kullanılır. Bu komut, mevcut shell sürecini yeni bir komut ile değiştirir, yani yeni bir shell başlatmaz. Bu sayede, çalıştırılan komut tamamlandığında shell oturumu da sonlanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
exec [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Belirtilen komutun farklı bir isimle çalıştırılmasını sağlar.
- `-l`: Yeni bir login shell başlatır.
- `-p`: Çalıştırılan komutun ortam değişkenlerini korur.

## Yaygın Örnekler
1. Bir komutu çalıştırmak:
   ```bash
   exec ls -l
   ```
   Bu komut, mevcut shell'i `ls -l` komutuyla değiştirir ve sonuçları gösterir.

2. Yeni bir shell başlatmak:
   ```bash
   exec bash
   ```
   Bu komut, mevcut shell'i `bash` ile değiştirir ve yeni bir bash oturumu başlatır.

3. Bir komutu farklı bir isimle çalıştırmak:
   ```bash
   exec -a yeni_isim /path/to/original_command
   ```
   Bu komut, belirtilen komutu `yeni_isim` adıyla çalıştırır.

## İpuçları
- `exec` komutunu kullanmadan önce, mevcut shell oturumunuzda kaydedilmesi gereken herhangi bir değişiklik olup olmadığını kontrol edin, çünkü `exec` mevcut shell'i değiştirecektir.
- `exec` ile çalıştırılan komutlar, shell oturumunu sonlandıracağı için dikkatli kullanılmalıdır.
- `exec` komutunu, betik dosyalarında sonlandırma işlemleri için kullanmak, daha temiz bir çıkış sağlar.