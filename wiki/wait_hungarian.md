# [Linux] Bash wait használat: Folyamatok várakoztatása

## Áttekintés
A `wait` parancs a Bash környezetben arra szolgál, hogy megvárja egy vagy több háttérfolyamat befejeződését. Ez hasznos lehet, ha szeretnénk biztosítani, hogy egy adott folyamat csak akkor induljon el, amikor a korábbi háttérfolyamatok már befejeződtek.

## Használat
A `wait` parancs alapvető szintaxisa a következő:

```bash
wait [opciók] [argumentumok]
```

## Gyakori opciók
- `-n`: Várakozik az első befejeződő háttérfolyamatra.
- `PID`: Megadott folyamatazonosítóra várakozik. Ha nem adunk meg PID-t, akkor az összes háttérfolyamatra várakozik.

## Gyakori példák

1. **Várakozás az összes háttérfolyamatra:**
   ```bash
   sleep 5 &
   sleep 3 &
   wait
   echo "Minden háttérfolyamat befejeződött."
   ```

2. **Várakozás egy konkrét háttérfolyamatra:**
   ```bash
   sleep 5 &
   PID=$!
   echo "Várok a PID: $PID folyamatra."
   wait $PID
   echo "A folyamat befejeződött."
   ```

3. **Várakozás az első befejeződő háttérfolyamatra:**
   ```bash
   sleep 5 &
   sleep 3 &
   wait -n
   echo "Az első háttérfolyamat befejeződött."
   ```

## Tippek
- Használj `wait`-et a szkriptekben, hogy biztosítsd a folyamatok helyes sorrendjét.
- Ellenőrizd a háttérfolyamatok PID-jét, hogy pontosan tudd, melyik folyamatra vársz.
- A `wait` parancs használata segíthet elkerülni a versenyhelyzeteket, amikor több folyamatot futtatsz párhuzamosan.