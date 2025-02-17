# [Linux] Bash last használat: Felhasználói bejelentkezések megjelenítése

## Áttekintés
A `last` parancs megjeleníti a felhasználók bejelentkezési előzményeit a rendszerben. Hasznos információkat nyújt arról, hogy mikor és ki lépett be a rendszerbe, valamint a bejelentkezések időtartamát.

## Használat
A `last` parancs alapvető szintaxisa a következő:

```bash
last [opciók] [felhasználónév]
```

## Gyakori opciók
- `-a`: Megjeleníti a bejelentkezési helyet (hostname).
- `-n [szám]`: Csak a megadott számú bejelentkezést mutatja.
- `-x`: Megjeleníti a rendszer leállításait és újraindításait is.

## Gyakori példák
1. **Összes bejelentkezés megjelenítése:**

   ```bash
   last
   ```

2. **Csak az utolsó 5 bejelentkezés megjelenítése:**

   ```bash
   last -n 5
   ```

3. **Bejelentkezések megjelenítése egy adott felhasználóra:**

   ```bash
   last username
   ```

4. **Bejelentkezések helyének megjelenítése:**

   ```bash
   last -a
   ```

5. **Bejelentkezések és rendszer leállítások megjelenítése:**

   ```bash
   last -x
   ```

## Tippek
- Használja a `-n` opciót, ha csak a legfrissebb bejelentkezéseket szeretné látni, ez segít a felesleges információk kiszűrésében.
- A `last` parancs kimenete hasznos lehet a rendszer biztonsági auditálásához, mivel nyomon követi a felhasználói tevékenységeket.
- Ellenőrizze rendszeresen a bejelentkezési előzményeket, hogy észlelje a gyanús tevékenységeket.