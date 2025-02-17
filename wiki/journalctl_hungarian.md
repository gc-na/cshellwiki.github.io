# [Linux] Bash journalctl használata: Rendszernapló megtekintése

## Áttekintés
A `journalctl` parancs a systemd naplózási rendszer része, amely lehetővé teszi a rendszer naplóbejegyzéseinek megtekintését. Ezzel a paranccsal hozzáférhetünk a rendszer eseményeihez, hibáihoz és egyéb fontos információkhoz, amelyek segíthetnek a hibakeresésben és a rendszer állapotának ellenőrzésében.

## Használat
A `journalctl` parancs alapvető szintaxisa a következő:

```bash
journalctl [opciók] [argumentumok]
```

## Gyakori opciók
- `-b` vagy `--boot`: Csak az aktuális rendszerindítási eseményeit mutatja.
- `-f` vagy `--follow`: Folyamatosan figyeli a naplóbejegyzéseket, hasonlóan a `tail -f` parancshoz.
- `-u <szolgáltatás>`: Csak a megadott szolgáltatás naplóbejegyzéseit jeleníti meg.
- `--since <idő>`: Csak az adott időpont óta keletkezett bejegyzéseket mutatja.
- `--until <idő>`: Csak az adott időpontig keletkezett bejegyzéseket mutatja.

## Gyakori példák
1. Az összes naplóbejegyzés megtekintése:
   ```bash
   journalctl
   ```

2. Csak az aktuális rendszerindítási események megjelenítése:
   ```bash
   journalctl -b
   ```

3. Egy szolgáltatás naplóbejegyzéseinek megtekintése (pl. `ssh`):
   ```bash
   journalctl -u ssh
   ```

4. A naplóbejegyzések folyamatos figyelése:
   ```bash
   journalctl -f
   ```

5. Naplóbejegyzések megjelenítése egy adott időszakra:
   ```bash
   journalctl --since "2023-10-01" --until "2023-10-10"
   ```

## Tippek
- Használja a `-p` opciót a naplóbejegyzések szint szerinti szűrésére (pl. `-p err` csak a hibákat mutatja).
- A naplóbejegyzések szűrésére és rendezésére használhatja a `grep` parancsot.
- A `--no-pager` opcióval megakadályozhatja, hogy a kimenet oldalonként jelenjen meg, így az összes bejegyzés egyszerre látható.