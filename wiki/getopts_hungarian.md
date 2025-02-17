# [Linux] Bash getopts használata: Parancssori opciók kezelése

## Áttekintés
A `getopts` parancs a Bash shellben lehetővé teszi a parancssori opciók és argumentumok kezelését. Segítségével egyszerűen olvashatunk be és dolgozhatunk fel opciókat a shell szkriptekben, így a felhasználói interakciók zökkenőmentesebbé válnak.

## Használat
A `getopts` parancs alapvető szintaxisa a következő:

```bash
getopts [opciók] [változó] [argumentumok]
```

## Gyakori opciók
- `a`: Egyedi opció, amelyet a felhasználó megadhat.
- `b`: Egy másik opció, amelyhez argumentum is tartozhat.
- `c`: Egy opció, amely nem igényel argumentumot.

## Gyakori példák

1. **Egyszerű opciók kezelése**
   ```bash
   #!/bin/bash
   while getopts "ab:c:" opt; do
       case $opt in
           a)
               echo "A opció aktiválva."
               ;;
           b)
               echo "B opció értéke: $OPTARG"
               ;;
           c)
               echo "C opció aktiválva, argumentum: $OPTARG"
               ;;
           *)
               echo "Érvénytelen opció."
               ;;
       esac
   done
   ```

2. **Több opció egyidejű használata**
   ```bash
   #!/bin/bash
   while getopts "abc:" opt; do
       case $opt in
           a)
               echo "A opció aktiválva."
               ;;
           b)
               echo "B opció aktiválva."
               ;;
           c)
               echo "C opció értéke: $OPTARG"
               ;;
           *)
               echo "Érvénytelen opció."
               ;;
       esac
   done
   ```

3. **Alapértelmezett érték beállítása**
   ```bash
   #!/bin/bash
   option_a=false
   while getopts "a" opt; do
       case $opt in
           a)
               option_a=true
               ;;
           *)
               ;;
       esac
   done

   if $option_a; then
       echo "A opció aktiválva."
   else
       echo "A opció nem aktiválva."
   fi
   ```

## Tippek
- Mindig használj `case` szerkezetet a `getopts` kimenetének kezelésére, hogy könnyen bővíthesd a parancsokat.
- Használj `OPTARG` változót az argumentumok elérésére, ha az opciókhoz argumentumok is tartoznak.
- Érdemes a `getopts` parancsot a szkript elején használni, hogy a felhasználó könnyen láthassa, milyen opciók érhetők el.