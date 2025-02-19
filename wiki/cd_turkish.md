# [Linux] C Shell (csh) cd Kullanımı: Dizinler arasında geçiş yapma

## Overview
`cd` komutu, kullanıcıların dosya sisteminde dizinler arasında geçiş yapmalarını sağlar. Bu komut, "change directory" ifadesinin kısaltmasıdır ve terminalde çalışırken bulunduğunuz dizini değiştirmenize olanak tanır.

## Usage
Temel sözdizimi şu şekildedir:

```csh
cd [options] [arguments]
```

## Common Options
- `-`: Önceki dizine geri döner.
- `~`: Kullanıcının ana dizinine geçiş yapar.
- `..`: Bir üst dizine geçiş yapar.

## Common Examples
Aşağıda `cd` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Ana dizine geçiş:
   ```csh
   cd ~
   ```

2. Bir üst dizine geçiş:
   ```csh
   cd ..
   ```

3. Belirli bir dizine geçiş (örneğin, "Belgeler" dizinine):
   ```csh
   cd Belgeler
   ```

4. Önceki dizine geri dönme:
   ```csh
   cd -
   ```

## Tips
- `cd` komutunu kullanırken, dizin adlarını tam olarak yazmak yerine kısaltmalar kullanabilirsiniz. Örneğin, `cd ~/Belgeler` ile ana dizinin altındaki "Belgeler" dizinine hızlıca geçebilirsiniz.
- Dizin adları büyük/küçük harf duyarlıdır, bu nedenle doğru yazdığınızdan emin olun.
- Dizinler arasında geçiş yaparken, terminaldeki mevcut konumunuzu kontrol etmek için `pwd` (print working directory) komutunu kullanabilirsiniz.