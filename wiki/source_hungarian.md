# [Linux] Bash source használata: Shell szkriptek futtatása

## Áttekintés
A `source` parancs a Bash shell-ben lehetővé teszi egy szkript vagy parancsfájl futtatását a jelenlegi shell környezetében. Ez azt jelenti, hogy a szkriptben definiált változók és funkciók elérhetők maradnak a parancs végrehajtása után is.

## Használat
A `source` parancs alapvető szintaxisa a következő:

```bash
source [opciók] [argumentumok]
```

Alternatív megoldásként a `.` (pont) karaktert is használhatjuk a `source` helyett.

## Gyakori opciók
- Nincs külön opció a `source` parancshoz, de a szkriptekben használt parancsoknak lehetnek saját opcióik.

## Gyakori példák
1. **Szkript futtatása:**
   Egy szkript futtatása a jelenlegi shell környezetében:
   ```bash
   source myscript.sh
   ```

2. **Változók beállítása:**
   Egy szkript futtatása, amely változókat definiál:
   ```bash
   source setenv.sh
   echo $MY_VARIABLE
   ```

3. **Funkciók definiálása:**
   Funkciók betöltése egy szkriptből:
   ```bash
   source functions.sh
   my_function
   ```

4. **Alternatív szintaxis:**
   A `.` karakter használata a `source` helyett:
   ```bash
   . myscript.sh
   ```

## Tippek
- Használj `source`-t, amikor szeretnéd, hogy a szkript által definiált változók és funkciók a shell session-ben elérhetők maradjanak.
- Ellenőrizd a szkriptek szintaxisát és hibáit a futtatás előtt, hogy elkerüld a váratlan viselkedést.
- Használj relatív vagy abszolút elérési utakat a szkriptek hívásakor, hogy biztosítsd a helyes fájlok betöltését.