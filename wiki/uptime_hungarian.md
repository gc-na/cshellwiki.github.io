# [Linux] Bash uptime használat: A rendszer működési idejének megjelenítése

## Overview
Az `uptime` parancs megmutatja, hogy a rendszer mennyi ideje fut, valamint a rendszer terhelését az utolsó 1, 5 és 15 percben. Ez hasznos információkat szolgáltat a rendszeradminisztrátorok számára a rendszer teljesítményének és stabilitásának felméréséhez.

## Usage
A parancs alapvető szintaxisa a következő:

```
uptime [opciók]
```

## Common Options
- `-p` : Az uptime időtartamát egy barátságos formátumban jeleníti meg.
- `-s` : Megjeleníti a rendszer indításának időpontját.
  
## Common Examples
1. Az alap `uptime` parancs futtatása:
   ```bash
   uptime
   ```

2. Az uptime időtartamának barátságos formátumban történő megjelenítése:
   ```bash
   uptime -p
   ```

3. A rendszer indításának időpontjának megjelenítése:
   ```bash
   uptime -s
   ```

## Tips
- Használja az `uptime` parancsot rendszeresen, hogy nyomon követhesse a rendszer teljesítményét.
- Kombinálja az `uptime` parancsot más parancsokkal, mint például a `top`, hogy részletesebb képet kapjon a rendszer terheléséről.
- Figyelje a terhelési átlagokat, hogy időben észlelje a potenciális problémákat a rendszer teljesítményében.