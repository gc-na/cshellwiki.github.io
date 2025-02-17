# [Linux] Bash script Kullanımı: Komutların kaydını tutma

## Overview
`script` komutu, terminal oturumlarınızı kaydetmenizi sağlar. Bu komut, kullanıcıların terminalde gerçekleştirdiği tüm etkileşimleri ve çıktıları bir dosyaya yazmak için kullanılır. Bu sayede, oturumunuzu daha sonra gözden geçirebilir veya paylaşabilirsiniz.

## Usage
Temel sözdizimi şu şekildedir:
```bash
script [options] [file]
```

## Common Options
- `-a`: Mevcut bir dosyaya ekleme yapar, yeni bir dosya oluşturmak yerine.
- `-q`: Çıktıyı sessiz modda kaydeder; kullanıcıya bilgi vermez.
- `-t`: Zaman damgalarını kaydeder; bu, oturum süresini analiz etmek için yararlıdır.

## Common Examples
Aşağıda `script` komutunun bazı pratik örnekleri verilmiştir:

1. Basit bir oturum kaydı başlatma:
   ```bash
   script oturum.txt
   ```
   Bu komut, `oturum.txt` adlı bir dosyaya terminal oturumunu kaydetmeye başlar.

2. Mevcut bir dosyaya ekleme yapma:
   ```bash
   script -a ekleme.txt
   ```
   Bu komut, `ekleme.txt` dosyasına yeni bir oturum ekler.

3. Sessiz modda oturum kaydetme:
   ```bash
   script -q sessiz.txt
   ```
   Bu komut, `sessiz.txt` dosyasına kaydetme yaparken kullanıcıya bilgi vermez.

4. Zaman damgaları ile oturum kaydetme:
   ```bash
   script -t 2> zaman.txt zaman_kaydi.txt
   ```
   Bu komut, `zaman_kaydi.txt` dosyasına oturumu kaydederken, zaman damgalarını `zaman.txt` dosyasına kaydeder.

## Tips
- Kaydettiğiniz dosyaların adlarını anlamlı bir şekilde seçin, böylece daha sonra ne içerdiğini kolayca hatırlayabilirsiniz.
- `script` komutunu kullanırken, oturumunuzu bitirmek için `exit` komutunu kullanmayı unutmayın.
- Kayıtlı oturum dosyalarını gözden geçirirken, `less` veya `cat` gibi komutları kullanarak içeriği görüntüleyebilirsiniz.