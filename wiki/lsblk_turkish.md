# [Linux] Bash lsblk Kullanımı: Disk ve Bölüm Bilgilerini Gösterir

## Overview
`lsblk` komutu, sistemdeki blok aygıtlarını ve bunların bölümlerini listelemek için kullanılır. Bu komut, disklerin ve bölümlerin hiyerarşik yapısını görsel olarak sunar, böylece kullanıcılar sistemdeki depolama aygıtlarını kolayca anlayabilir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
lsblk [options] [arguments]
```

## Common Options
- `-a`, `--all`: Tüm aygıtları gösterir, boş olanlar da dahil.
- `-f`, `--fs`: Dosya sistemi bilgilerini gösterir.
- `-l`, `--list`: Listeleme formatını düz bir liste olarak gösterir.
- `-o`, `--output`: Gösterilecek sütunları belirler.
- `-p`, `--paths`: Aygıt yollarını tam olarak gösterir.

## Common Examples
Aşağıda `lsblk` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Temel Listeleme
Sadece diskleri ve bölümleri listelemek için:
```bash
lsblk
```

### 2. Dosya Sistemi Bilgileri ile Listeleme
Disklerin dosya sistemi bilgilerini görmek için:
```bash
lsblk -f
```

### 3. Düz Liste Formatında Gösterim
Düz bir liste formatında aygıtları görmek için:
```bash
lsblk -l
```

### 4. Belirli Sütunları Gösterme
Sadece belirli bilgileri göstermek için:
```bash
lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
```

### 5. Tüm Aygıtları Gösterme
Boş aygıtlar dahil tüm aygıtları listelemek için:
```bash
lsblk -a
```

## Tips
- `lsblk` komutunu `sudo` ile kullanarak daha fazla bilgi elde edebilirsiniz.
- Aygıtların hangi dosya sistemine sahip olduğunu görmek için `-f` seçeneğini kullanmayı unutmayın.
- Çıktıyı daha okunabilir hale getirmek için `column` komutunu kullanabilirsiniz:
  ```bash
  lsblk | column -t
  ```