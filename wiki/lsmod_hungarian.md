# [Linux] Bash lsmod használata: A betöltött modulok listázása

## Áttekintés
Az `lsmod` parancs a Linux operációs rendszerben a betöltött kernel modulok listázására szolgál. Ez a parancs segít megérteni, hogy mely modulok aktívak a rendszerben, és hasznos információkat nyújt a rendszer állapotáról.

## Használat
A `lsmod` parancs alapvető szintaxisa a következő:

```bash
lsmod [opciók] [argumentumok]
```

## Gyakori opciók
- **-h, --help**: Megjeleníti a súgót és a parancs használatára vonatkozó információkat.
- **-q, --quiet**: Csökkenti a kimenetet, csak a legfontosabb információkat jeleníti meg.

## Gyakori példák
1. **Betöltött modulok listázása**:
   ```bash
   lsmod
   ```

2. **Súgó megjelenítése**:
   ```bash
   lsmod --help
   ```

3. **Csendes mód használata**:
   ```bash
   lsmod --quiet
   ```

## Tippek
- Használja az `lsmod` parancsot rendszeresen a kernel modulok állapotának ellenőrzésére, különösen hibaelhárítás során.
- Kombinálja az `lsmod` parancsot más parancsokkal, mint például a `grep`, hogy specifikus modulokat keressen:
  ```bash
  lsmod | grep modul_neve
  ```
- Figyelje a modulok közötti függőségeket, amelyek segíthetnek a rendszer stabilitásának megértésében.