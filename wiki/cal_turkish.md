# [Linux] Bash cal Kullanımı: Takvim görüntüleme komutu

## Overview
`cal` komutu, belirli bir ay veya yıl için takvim görüntülemek amacıyla kullanılan bir Bash komutudur. Kullanıcılar, bu komut sayesinde tarihleri hızlı bir şekilde görebilirler.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
cal [seçenekler] [argümanlar]
```

## Common Options
- `-m`: Ayın ilk gününü haftanın ilk günü olarak ayarlar (Pazar yerine Pazartesi).
- `-y`: Yıl takvimini görüntüler.
- `-3`: Geçerli ayın yanı sıra bir önceki ve bir sonraki ayı da gösterir.
- `-j`: Yılın gün numaralarını gösterir.
- `-A [n]`: Geçerli aydan sonra gelen `n` ayı gösterir.
- `-B [n]`: Geçerli aydan önceki `n` ayı gösterir.

## Common Examples
Aşağıda `cal` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### Geçerli Ayın Takvimini Görüntüleme
```bash
cal
```

### Belirli Bir Yılın Takvimini Görüntüleme
```bash
cal 2023
```

### Geçerli Ay ile Bir Önceki ve Bir Sonraki Ayı Görüntüleme
```bash
cal -3
```

### Geçerli Ayın Gün Numaralarını Gösterme
```bash
cal -j
```

### Önceki 2 Ayı ve Geçerli Ayı Görüntüleme
```bash
cal -B 2
```

## Tips
- `cal` komutunu sık sık kullanıyorsanız, sık kullandığınız seçenekler için bir alias oluşturabilirsiniz.
- Takvimde belirli tarihlerde önemli günleri işaretlemek için `ncal` komutunu da inceleyebilirsiniz; bu, daha gelişmiş bir takvim görüntüleme aracıdır.
- `man cal` komutunu kullanarak `cal` hakkında daha fazla bilgi edinebilirsiniz.