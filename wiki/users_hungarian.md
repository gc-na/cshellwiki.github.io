# [Linux] Bash felhasználók parancs: Felhasználók listázása

## Áttekintés
A `users` parancs a Linux és Unix rendszerekben a bejelentkezett felhasználók nevét listázza ki. Ez a parancs egyszerű és gyors módot kínál arra, hogy lássuk, kik vannak bejelentkezve a rendszerre.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
users [opciók] [argumentumok]
```

## Gyakori opciók
- `-n`: Csak a felhasználók nevét jeleníti meg, anélkül, hogy a bejelentkezési időt vagy más információt tartalmazna.
- `-r`: Csak a rendszergazda felhasználókat listázza.

## Gyakori példák
1. **Felhasználók listázása**:
   A legegyszerűbb használat, amely megjeleníti az összes bejelentkezett felhasználó nevét.
   ```bash
   users
   ```

2. **Felhasználók listázása rendszergazdai jogokkal**:
   Csak a rendszergazda felhasználók megjelenítése.
   ```bash
   users -r
   ```

3. **Felhasználók listázása név szerint**:
   A felhasználók neveinek megjelenítése, anélkül, hogy más információt tartalmazna.
   ```bash
   users -n
   ```

## Tippek
- Használja a `who` vagy `w` parancsot, ha részletesebb információra van szüksége a bejelentkezett felhasználókról, például a bejelentkezési időről és a használt terminálról.
- A `users` parancs kimenete egy sorban jeleníti meg a felhasználókat, így könnyen átirányíthatja a kimenetet egy fájlba, ha szükséges:
  ```bash
  users > felhasználok.txt
  ```