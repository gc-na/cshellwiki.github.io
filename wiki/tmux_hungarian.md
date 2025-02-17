# [Linux] Bash tmux használata: Több terminál egyidejű kezelése

## Áttekintés
A `tmux` egy terminál multiplexer, amely lehetővé teszi, hogy több terminálablakot kezeljünk egyetlen ablakban. Használatával könnyedén válthatunk az ablakok között, és megőrizhetjük a munkameneteket, még akkor is, ha a terminál bezárul.

## Használat
A `tmux` parancs alapvető szintaxisa a következő:

```bash
tmux [opciók] [argumentumok]
```

## Gyakori Opciók
- `new`: Új tmux munkamenet indítása.
- `attach`: Csatlakozás egy meglévő munkamenethez.
- `detach`: Leválasztás a jelenlegi munkamenetről.
- `list-sessions`: A futó tmux munkamenetek listázása.
- `kill-session`: Egy munkamenet bezárása.

## Gyakori Példák
- Új tmux munkamenet indítása:
  ```bash
  tmux new -s mysession
  ```

- Csatlakozás egy meglévő munkamenethez:
  ```bash
  tmux attach -t mysession
  ```

- Munkamenet leválasztása:
  ```bash
  Ctrl + b, d
  ```

- Futó munkamenetek listázása:
  ```bash
  tmux list-sessions
  ```

- Munkamenet bezárása:
  ```bash
  tmux kill-session -t mysession
  ```

## Tippek
- Használj előre definiált billentyűparancsokat a tmux-ban, mint például `Ctrl + b`, majd `c` új ablak létrehozásához.
- A tmux konfigurálásához érdemes létrehozni egy `.tmux.conf` fájlt a home könyvtárban, ahol testreszabhatod a beállításokat.
- Használj panelek létrehozását (`Ctrl + b`, majd `%` vagy `"`), hogy párhuzamosan több feladatot végezhess el.