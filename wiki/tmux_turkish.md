# [Linux] Bash tmux Kullanımı: Terminal oturumlarını yönetme aracı

## Genel Bakış
tmux, bir terminal çoklayıcısıdır. Kullanıcıların birden fazla terminal oturumu oluşturmasına, yönetmesine ve bunlar arasında geçiş yapmasına olanak tanır. Bu sayede, kullanıcılar aynı anda birden fazla işlemi takip edebilir ve çalışabilir.

## Kullanım
tmux komutunun temel sözdizimi aşağıdaki gibidir:

```bash
tmux [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `new`: Yeni bir tmux oturumu oluşturur.
- `attach`: Var olan bir tmux oturumuna bağlanır.
- `list-sessions`: Mevcut tmux oturumlarını listeler.
- `kill-session`: Belirtilen tmux oturumunu sonlandırır.
- `detach`: Aktif tmux oturumundan ayrılır.

## Yaygın Örnekler
Aşağıda tmux kullanımına dair bazı pratik örnekler bulunmaktadır:

### Yeni Oturum Oluşturma
Yeni bir tmux oturumu başlatmak için:

```bash
tmux new -s oturum_adı
```

### Var Olan Oturuma Bağlanma
Mevcut bir oturuma bağlanmak için:

```bash
tmux attach -t oturum_adı
```

### Oturumları Listeleme
Tüm mevcut tmux oturumlarını görmek için:

```bash
tmux list-sessions
```

### Oturumu Sonlandırma
Belirli bir oturumu kapatmak için:

```bash
tmux kill-session -t oturum_adı
```

### Oturumdan Ayrılma
Aktif oturumdan ayrılmak için:

```bash
tmux detach
```

## İpuçları
- tmux oturumlarınızı adlandırarak daha düzenli bir çalışma ortamı oluşturabilirsiniz.
- Kısa yolları öğrenmek, tmux kullanımını hızlandırır. Örneğin, `Ctrl + b` tuş kombinasyonu ile tmux komutlarına erişebilirsiniz.
- Oturumları arka planda çalıştırarak, terminali kapatmadan işlemlerinizi sürdürebilirsiniz.