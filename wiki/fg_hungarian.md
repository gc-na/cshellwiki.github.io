# [Linux] Bash fg használata: A háttérben futó folyamatok előtérbe hozása

## Áttekintés
A `fg` parancs a Bash környezetben lehetővé teszi a háttérben futó folyamatok előtérbe hozását. Ez hasznos, amikor egy folyamatot háttérbe helyeztünk, és szeretnénk újra aktívan irányítani.

## Használat
A `fg` parancs alapvető szintaxisa a következő:

```bash
fg [options] [job_spec]
```

## Gyakori opciók
- `job_spec`: Megadhatjuk a folyamat azonosítóját vagy számát, amelyet előtérbe szeretnénk hozni. Ha nem adunk meg semmit, az utolsó háttérben futó folyamatot hozza előtérbe.

## Gyakori példák

1. Az utolsó háttérben futó folyamat előtérbe hozása:
   ```bash
   fg
   ```

2. Egy konkrét háttérfolyamat előtérbe hozása, például ha a folyamat azonosítója 1:
   ```bash
   fg %1
   ```

3. Ha több háttérfolyamatunk van, és az azonosítójuk 2, akkor azt így hozhatjuk előtérbe:
   ```bash
   fg %2
   ```

## Tippek
- Használja a `jobs` parancsot, hogy megtekintse a háttérben futó folyamatokat és azok azonosítóit, mielőtt a `fg` parancsot használná.
- Ha egy folyamatot előtérbe hozott, és szeretné megszakítani, használja a `Ctrl + C` billentyűkombinációt.
- A `fg` parancs használata előtt győződjön meg róla, hogy a folyamat valóban háttérben fut, különben hibaüzenetet kaphat.