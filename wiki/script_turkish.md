# [Linux] C Shell (csh) script Kullanımı: Komutların kaydını tutma

## Overview
`script` komutu, terminal oturumlarınızı kaydetmek için kullanılır. Bu komut, terminaldeki tüm çıktıyı bir dosyaya yazarak, daha sonra bu oturumu incelemenizi sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
script [options] [arguments]
```

## Common Options
- `-a`: Mevcut bir dosyaya ekleme yapar. Eğer dosya zaten varsa, yeni çıktılar mevcut içeriğin sonuna eklenir.
- `-f`: Çıktıyı anında gösterir. Bu seçenek, terminaldeki çıktının hemen görünmesini sağlar.
- `-q`: Sessiz modda çalışır. Bu seçenek ile başlangıç ve bitiş mesajları gösterilmez.

## Common Examples
Aşağıda `script` komutunun bazı pratik örnekleri bulunmaktadır:

1. Basit bir oturum kaydı oluşturma:
   ```csh
   script oturum.txt
   ```

2. Mevcut bir dosyaya ekleme yaparak kaydetme:
   ```csh
   script -a oturum.txt
   ```

3. Çıktıyı anında gösterme:
   ```csh
   script -f oturum.txt
   ```

4. Sessiz modda oturum kaydetme:
   ```csh
   script -q oturum.txt
   ```

## Tips
- `script` komutunu kullanırken, kaydedilen dosyanın adını anlamlı bir şekilde seçmek, daha sonra bulmanızı kolaylaştırır.
- Oturum kaydını başlatmadan önce, terminaldeki gereksiz çıktıları temizlemek için `clear` komutunu kullanabilirsiniz.
- Kaydedilen dosyayı incelemek için `cat`, `less` veya `more` gibi komutları kullanabilirsiniz.