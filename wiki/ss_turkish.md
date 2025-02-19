# [Linux] C Shell (csh) ss Kullanımı: Ağ bağlantılarını görüntüleme

## Overview
`ss` komutu, ağ bağlantılarını, dinleme soketlerini ve diğer ağ istatistiklerini görüntülemek için kullanılan bir araçtır. Bu komut, sistem yöneticileri ve geliştiriciler için ağ durumu hakkında bilgi edinmek amacıyla oldukça faydalıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
ss [options] [arguments]
```

## Common Options
- `-t`: TCP bağlantılarını gösterir.
- `-u`: UDP bağlantılarını gösterir.
- `-l`: Dinleme durumundaki soketleri listeler.
- `-p`: Bağlantıların hangi süreçler tarafından kullanıldığını gösterir.
- `-n`: Adres ve port numaralarını sayısal olarak gösterir.

## Common Examples
Aşağıda `ss` komutunun bazı yaygın kullanımları bulunmaktadır:

1. **Tüm bağlantıları görüntüleme:**
   ```bash
   ss
   ```

2. **Sadece TCP bağlantılarını görüntüleme:**
   ```bash
   ss -t
   ```

3. **Dinleme durumundaki soketleri görüntüleme:**
   ```bash
   ss -l
   ```

4. **UDP bağlantılarını görüntüleme:**
   ```bash
   ss -u
   ```

5. **Bağlantıların süreç bilgisi ile birlikte görüntülenmesi:**
   ```bash
   ss -p
   ```

6. **Sayısal adres ve port numaraları ile görüntüleme:**
   ```bash
   ss -n
   ```

## Tips
- `ss` komutunu kullanırken, belirli bir protokolü hedeflemek için `-t` veya `-u` seçeneklerini kullanmak, daha net sonuçlar almanıza yardımcı olur.
- Ağ sorunlarını teşhis ederken, `-p` seçeneği ile süreç bilgilerini görmek, hangi uygulamaların ağ kaynaklarını kullandığını anlamanızı sağlar.
- `ss` komutunu sık sık kullanıyorsanız, sık kullandığınız seçenekleri bir alias ile kısayol olarak tanımlamak işinizi kolaylaştırabilir.