# [Linux] Bash id használat: Felhasználói azonosító és csoportinformációk megjelenítése

## Overview
Az `id` parancs a felhasználói azonosító (UID) és a csoportazonosítók (GID) megjelenítésére szolgál a Unix-alapú rendszerekben. Ez a parancs hasznos információkat nyújt a felhasználói fiókról, beleértve a felhasználó csoportjait is.

## Usage
A parancs alapvető szintaxisa a következő:

```bash
id [options] [arguments]
```

## Common Options
- `-u`: Csak a felhasználói azonosítót (UID) jeleníti meg.
- `-g`: Csak a fő csoportazonosítót (GID) jeleníti meg.
- `-G`: Az összes csoportazonosítót (GID) megjeleníti, amelyhez a felhasználó tartozik.
- `-n`: Az azonosítók helyett a nevek megjelenítése.

## Common Examples
1. **Alapvető felhasználói információk megjelenítése:**
   ```bash
   id
   ```

2. **Csak a felhasználói azonosító megjelenítése:**
   ```bash
   id -u
   ```

3. **Csak a fő csoportazonosító megjelenítése:**
   ```bash
   id -g
   ```

4. **Az összes csoportazonosító megjelenítése:**
   ```bash
   id -G
   ```

5. **Felhasználói név és azonosító megjelenítése:**
   ```bash
   id -n
   ```

## Tips
- Használja az `id` parancsot a felhasználói jogosultságok gyors ellenőrzésére.
- A `-n` opcióval kombinálva könnyen megjelenítheti a csoportneveket az azonosítók helyett, ami érthetőbbé teszi az információkat.
- Ha több felhasználó azonosítóját szeretné megtekinteni, adja meg a felhasználó nevét az `id` parancs után, például: `id username`.