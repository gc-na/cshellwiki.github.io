# [Linux] Bash hostnamectl használata: Rendszernév és egyéb információk kezelése

## Áttekintés
A `hostnamectl` parancs a Linux operációs rendszerekben a rendszer nevét és egyéb kapcsolódó információkat kezeli. Ezzel a paranccsal megtekinthetjük és módosíthatjuk a gép nevét, valamint információkat kaphatunk a rendszer állapotáról.

## Használat
A `hostnamectl` parancs alapvető szintaxisa a következő:

```bash
hostnamectl [opciók] [argumentumok]
```

## Gyakori opciók
- `set-hostname`: A rendszer nevét állítja be.
- `status`: Megjeleníti a rendszer aktuális állapotát és információit.
- `set-icon-name`: Az ikon nevét állítja be a rendszerhez.
- `set-chassis`: A rendszer típusát állítja be (pl. asztali, szerver).

## Gyakori példák

### Rendszernév megjelenítése
A rendszer aktuális nevének megtekintéséhez használja a következő parancsot:

```bash
hostnamectl status
```

### Rendszernév beállítása
A rendszer nevét az alábbi módon állíthatja be:

```bash
sudo hostnamectl set-hostname új-nev
```

### Ikon név beállítása
Az ikon nevét a következő parancs segítségével állíthatja be:

```bash
sudo hostnamectl set-icon-name új-ikon-név
```

### Rendszer típusának beállítása
A rendszer típusának beállításához használja az alábbi parancsot:

```bash
sudo hostnamectl set-chassis asztali
```

## Tippek
- Mindig használjon `sudo`-t a `set-hostname` és hasonló parancsoknál, hogy elegendő jogosultsága legyen a módosításokhoz.
- Ellenőrizze a rendszer nevét a módosítások előtt és után a `status` opcióval, hogy megbizonyosodjon a sikeres változtatásról.
- A rendszer név megváltoztatása után érdemes újraindítani a rendszert, hogy a változások érvénybe lépjenek.