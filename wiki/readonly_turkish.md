# [Linux] Bash readonly Kullanımı: Değiştirilemeyen değişkenler oluşturma

## Genel Bakış
`readonly` komutu, bir değişkenin değerini değiştirilmez hale getirir. Bu, bir değişkenin tanımlandıktan sonra başka bir değer almasını engelleyerek, programlar veya betikler içinde sabit değerler oluşturmanıza yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
readonly [options] [arguments]
```

## Yaygın Seçenekler
- `-p`: Mevcut readonly değişkenlerini ve değerlerini listelemek için kullanılır.

## Yaygın Örnekler

### 1. Basit readonly Değişken Tanımlama
```bash
readonly MY_VAR="Sabit Değer"
```
Bu komut, `MY_VAR` değişkenini "Sabit Değer" olarak tanımlar ve daha sonra bu değerin değiştirilmesini engeller.

### 2. readonly Değişkenin Değerini Değiştirmeye Çalışmak
```bash
readonly MY_VAR="Sabit Değer"
MY_VAR="Yeni Değer"  # Bu satır hata verecektir.
```
`MY_VAR` değişkeni readonly olarak tanımlandığı için, burada yapılan değişiklik bir hata oluşturur.

### 3. Mevcut readonly Değişkenlerini Listeleme
```bash
readonly -p
```
Bu komut, mevcut tüm readonly değişkenlerini ve değerlerini listeler.

## İpuçları
- readonly değişkenleri, betiklerinizde sabit değerler kullanmak istediğinizde oldukça yararlıdır.
- Değişkenleri readonly olarak tanımladıktan sonra, bu değişkenlerin değerlerini değiştirmeye çalıştığınızda hata alacağınızı unutmayın.
- Betiklerinizi daha okunabilir hale getirmek için, önemli sabitleri readonly olarak tanımlamak iyi bir uygulamadır.