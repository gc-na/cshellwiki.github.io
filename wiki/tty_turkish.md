# [Linux] Bash tty Kullanımı: Terminal cihazının adını gösterir

## Overview
`tty` komutu, terminal cihazının adını gösteren bir Bash komutudur. Terminalin hangi cihazla iletişim kurduğunu belirlemek için kullanılır. Genellikle, bir terminal oturumu açıldığında hangi cihaz üzerinden çalıştığınızı anlamak için faydalıdır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
tty [options] [arguments]
```

## Common Options
- `-s`: Çıktıyı sessiz modda gösterir, yani yalnızca bir çıkış kodu döner.
- `--help`: Komutun kullanımına dair yardım bilgilerini gösterir.
- `--version`: `tty` komutunun sürüm bilgilerini gösterir.

## Common Examples
Aşağıda `tty` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Terminal cihazının adını öğrenmek için:
   ```bash
   tty
   ```

2. Sessiz modda çalıştırarak sadece çıkış kodunu almak için:
   ```bash
   tty -s
   ```

3. Yardım bilgilerini görüntülemek için:
   ```bash
   tty --help
   ```

4. Sürüm bilgilerini kontrol etmek için:
   ```bash
   tty --version
   ```

## Tips
- `tty` komutunu, birden fazla terminal oturumu açtığınızda hangi terminalde çalıştığınızı belirlemek için kullanabilirsiniz.
- Eğer bir komutun hangi terminalden çalıştığını bilmek istiyorsanız, `tty` komutunu o terminalde çalıştırarak kolayca öğrenebilirsiniz.
- Script yazarken, terminalin hangi cihaz üzerinden çalıştığını kontrol etmek için `tty` komutunu kullanmak, hata ayıklama sürecinde faydalı olabilir.