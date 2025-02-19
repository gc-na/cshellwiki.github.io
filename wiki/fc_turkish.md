# [Linux] C Shell (csh) fc Kullanımı: Komut geçmişini düzenleme ve çalıştırma

## Genel Bakış
`fc` komutu, C Shell (csh) ortamında komut geçmişini düzenlemek ve çalıştırmak için kullanılır. Kullanıcıların daha önce çalıştırdıkları komutları kolayca bulmalarını, düzenlemelerini ve yeniden çalıştırmalarını sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
fc [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Geçmişteki komutları listelemek için kullanılır.
- `-s`: Belirtilen komutu doğrudan çalıştırır, düzenleme yapmadan.
- `-n`: Komut numaralarını listelemeden gösterir.

## Yaygın Örnekler
Aşağıda `fc` komutunun bazı pratik örnekleri verilmiştir:

1. **Son komutu düzenleme:**
   ```csh
   fc
   ```
   Bu komut, en son çalıştırılan komutu varsayılan metin düzenleyici ile açar.

2. **Belirli bir komutu listeleme:**
   ```csh
   fc -l
   ```
   Bu komut, geçmişteki tüm komutları listeleyecektir.

3. **Son 5 komutu listeleme:**
   ```csh
   fc -l -5
   ```
   Bu komut, en son 5 çalıştırılan komutu listeleyecektir.

4. **Belirli bir komutu düzenleme:**
   ```csh
   fc 10
   ```
   Bu komut, geçmişteki 10. komutu düzenlemek için açar.

5. **Belirli bir komutu çalıştırma:**
   ```csh
   fc -s 10
   ```
   Bu komut, geçmişteki 10. komutu düzenlemeden doğrudan çalıştırır.

## İpuçları
- `fc` komutunu kullanmadan önce, düzenlemek istediğiniz komutun numarasını öğrenmek için `fc -l` komutunu çalıştırın.
- Komut geçmişini düzenlerken dikkatli olun; yanlış bir düzenleme, istenmeyen sonuçlara yol açabilir.
- `fc` komutunu sık sık kullanarak, komut geçmişinizi daha verimli bir şekilde yönetebilirsiniz.