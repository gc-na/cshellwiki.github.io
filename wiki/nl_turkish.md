# [Linux] Bash nl Kullanımı: Satır numaraları ekler

## Overview
`nl` komutu, bir dosyadaki her satıra satır numarası ekleyerek çıktısını düzenler. Bu, metin dosyalarını daha okunabilir hale getirmek ve belirli satırları kolayca referans almak için yararlıdır.

## Usage
Temel sözdizimi şu şekildedir:
```
nl [options] [arguments]
```

## Common Options
- `-b`: Satır numaralarının hangi satırlara ekleneceğini belirler. Örneğin, `-b a` tüm satırlara, `-b t` yalnızca boş olmayan satırlara numara ekler.
- `-f`: Her dosyanın başlangıcında satır numaralarını sıfırlamak için kullanılır.
- `-n`: Satır numaralarının biçimini belirler. `-n ln` (sola hizalı), `-n rn` (sağa hizalı) veya `-n rz` (sıfırlı) seçenekleri mevcuttur.
- `-w`: Satır numaralarının genişliğini ayarlar. Örneğin, `-w 5` satır numaralarının 5 karakter genişliğinde olmasını sağlar.

## Common Examples
- Temel kullanım:
  ```bash
  nl dosya.txt
  ```
  Bu komut, `dosya.txt` dosyasındaki her satıra numara ekler.

- Sadece boş olmayan satırlara numara eklemek:
  ```bash
  nl -b t dosya.txt
  ```
  Bu komut, yalnızca boş olmayan satırlara numara ekler.

- Satır numaralarını sıfırlamak:
  ```bash
  nl -f dosya1.txt dosya2.txt
  ```
  Bu komut, `dosya1.txt` ve `dosya2.txt` dosyalarının her birinde satır numaralarını sıfırlayarak başlar.

- Satır numaralarının sağa hizalı olmasını sağlamak:
  ```bash
  nl -n rn dosya.txt
  ```
  Bu komut, satır numaralarını sağa hizalı olarak gösterir.

## Tips
- `nl` komutunu, dosya içeriklerini daha iyi analiz etmek için diğer komutlarla birleştirin. Örneğin, `cat` komutuyla birlikte kullanarak dosyayı görüntüleyebilir ve numaralandırabilirsiniz.
- Büyük dosyalarla çalışırken, çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  nl dosya.txt > numaralandirilmis_dosya.txt
  ```
- Satır numaralarının genişliğini ayarlamak, daha düzenli bir görünüm sağlar. Özellikle uzun dosyalarda bu özelliği kullanmayı düşünün.