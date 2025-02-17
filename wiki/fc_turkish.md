# [Linux] Bash fc Kullanımı: Geçmişteki komutları düzenleme ve çalıştırma

## Overview
`fc` komutu, Bash kabuğunda daha önce çalıştırılan komutları düzenlemenizi ve tekrar çalıştırmanızı sağlar. Bu komut, geçmişteki komutların daha kolay bir şekilde gözden geçirilmesine ve gerektiğinde düzeltilmesine olanak tanır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
fc [options] [arguments]
```

## Common Options
- `-l`: Geçmişteki komutları listelemek için kullanılır.
- `-r`: Komutları ters sırada listelemek için kullanılır.
- `-s`: Belirtilen komutu çalıştırmadan önce düzenlemek için kullanılır.

## Common Examples
- Geçmişteki son 10 komutu listelemek için:
```bash
fc -l -n -10
```

- Belirli bir komutu düzenlemek için (örneğin, son komut):
```bash
fc
```

- Geçmişteki komutları ters sırada listelemek için:
```bash
fc -l -r
```

- Belirli bir komutu düzenleyip çalıştırmak için:
```bash
fc -s ls
```

## Tips
- `fc` komutunu kullanarak, hatalı yazılmış komutları hızlıca düzeltebilir ve zaman kazanabilirsiniz.
- Komutları düzenlerken, metin düzenleyici olarak varsayılan ayarları kullanabilirsiniz; bu, düzenlemeleri daha kolay hale getirir.
- Geçmişteki komutları gözden geçirerek, sık kullandığınız komutları öğrenebilir ve bunları bir betik dosyasına ekleyebilirsiniz.