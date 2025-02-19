# [Linux] C Shell (csh) export Kullanımı: Ortam Değişkenlerini Ayarlama

## Overview
`export` komutu, C Shell (csh) ortamında değişkenleri tanımlamak ve bu değişkenleri alt süreçlere iletmek için kullanılır. Bu sayede, tanımlanan değişkenler, shell oturumunun dışında da erişilebilir hale gelir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
export [options] [arguments]
```

## Common Options
- `-n`: Değişkenin dışa aktarımını iptal eder.
- `-p`: Dışa aktarılan tüm değişkenleri listeler.

## Common Examples

### Örnek 1: Basit Değişken Tanımlama
```csh
set MY_VAR="Merhaba Dünya"
export MY_VAR
```
Bu örnekte, `MY_VAR` adlı bir değişken tanımlanır ve dışa aktarılır.

### Örnek 2: Dışa Aktarılan Değişkeni Kullanma
```csh
set MY_VAR="Merhaba"
export MY_VAR
csh -c 'echo $MY_VAR'
```
Bu komut, yeni bir C Shell oturumu başlatır ve dışa aktarılan `MY_VAR` değişkenini kullanarak "Merhaba" yazdırır.

### Örnek 3: Dışa Aktarılan Değişkenleri Listeleme
```csh
export -p
```
Bu komut, dışa aktarılan tüm değişkenleri listeler.

## Tips
- Değişkenlerinizi dışa aktarırken, isimlendirme kurallarına dikkat edin; özel karakterler kullanmaktan kaçının.
- Dışa aktarılan değişkenlerinizi kontrol etmek için `export -p` komutunu kullanarak mevcut değişkenlerinizi gözden geçirin.
- Ortam değişkenlerinizi düzenli olarak güncelleyin ve gereksiz değişkenleri temizleyin.