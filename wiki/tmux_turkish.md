# [Linux] C Shell (csh) tmux Kullanımı: Terminal oturumlarını yönetme aracı

## Genel Bakış
tmux, bir terminal çoklayıcısıdır. Kullanıcıların birden fazla terminal oturumunu tek bir pencerede yönetmelerine olanak tanır. Bu, özellikle uzaktan bağlantılarda veya birden fazla görev üzerinde çalışırken oldukça faydalıdır.

## Kullanım
tmux komutunun temel sözdizimi aşağıdaki gibidir:

```bash
tmux [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `new`: Yeni bir tmux oturumu başlatır.
- `attach`: Var olan bir tmux oturumuna bağlanır.
- `list-sessions`: Mevcut tmux oturumlarını listeler.
- `kill-session`: Belirtilen tmux oturumunu kapatır.

## Yaygın Örnekler
Aşağıda tmux kullanımına dair bazı pratik örnekler bulunmaktadır:

### Yeni Bir Oturum Başlatma
Yeni bir tmux oturumu başlatmak için:

```bash
tmux new -s oturum_adı
```

### Var Olan Bir Oturuma Bağlanma
Daha önce oluşturulmuş bir oturuma bağlanmak için:

```bash
tmux attach -t oturum_adı
```

### Oturumları Listeleme
Mevcut tmux oturumlarını görmek için:

```bash
tmux list-sessions
```

### Oturumu Kapatma
Belirli bir oturumu kapatmak için:

```bash
tmux kill-session -t oturum_adı
```

## İpuçları
- tmux oturumlarınızı düzenli tutmak için anlamlı isimler verin.
- Oturumlar arasında geçiş yaparken `Ctrl+b` ardından `n` veya `p` tuşlarına basarak bir sonraki veya bir önceki oturuma geçebilirsiniz.
- tmux yapılandırma dosyası (`~/.tmux.conf`) oluşturarak kişisel ayarlarınızı kaydedebilirsiniz. Bu dosya, tmux başlatıldığında otomatik olarak yüklenir.