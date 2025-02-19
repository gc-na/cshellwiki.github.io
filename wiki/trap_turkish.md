# [Linux] C Shell (csh) trap Kullanımı: Sinyal yakalama

## Overview
`trap` komutu, C Shell (csh) ortamında belirli sinyalleri yakalamak ve bu sinyallere yanıt vermek için kullanılır. Bu, bir betiğin belirli durumlarda (örneğin, bir sinyal alındığında) nasıl davranacağını kontrol etmenizi sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
trap [options] [arguments]
```

## Common Options
- `0`: Betik sona erdiğinde çalışacak komutları belirtir.
- `1`: Sinyal 1 (SIGHUP) alındığında çalışacak komutları belirtir.
- `2`: Sinyal 2 (SIGINT) alındığında çalışacak komutları belirtir.
- `3`: Sinyal 3 (SIGQUIT) alındığında çalışacak komutları belirtir.
- `EXIT`: Betik sona erdiğinde çalışacak komutları belirtir.

## Common Examples
Aşağıda `trap` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Sinyal 2 (SIGINT) için bir komut ayarlama
```csh
trap 'echo "SIGINT sinyali alındı!"' 2
```
Bu komut, kullanıcı Ctrl+C tuşlarına bastığında "SIGINT sinyali alındı!" mesajını yazdırır.

### Örnek 2: Betik sona erdiğinde bir temizlik işlemi yapma
```csh
trap 'rm -f /tmp/tempfile; echo "Geçici dosya silindi."' EXIT
```
Bu komut, betik sona erdiğinde `/tmp/tempfile` dosyasını siler ve "Geçici dosya silindi." mesajını gösterir.

### Örnek 3: Sinyal 1 (SIGHUP) için bir işlem ayarlama
```csh
trap 'echo "SIGHUP sinyali alındı, yeniden başlatılıyor..."' 1
```
Bu komut, SIGHUP sinyali alındığında bir mesaj gösterir.

## Tips
- `trap` komutunu kullanarak betiklerinizin daha güvenilir ve kullanıcı dostu olmasını sağlayabilirsiniz.
- Sinyal yakalamak için `trap` komutunu betiğinizin en başında tanımlamak iyi bir uygulamadır.
- Birden fazla sinyal için aynı komutu ayarlamak isterseniz, sinyal numaralarını boşlukla ayırarak yazabilirsiniz.