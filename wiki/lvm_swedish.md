# [Linux] Bash lvm användning: Hantera logiska volymer

## Översikt
LVM (Logical Volume Manager) är ett verktyg för att hantera partitioner på Linux-system. Det gör det möjligt att skapa, ändra storlek på och ta bort logiska volymer, vilket ger mer flexibilitet än traditionell partitionering.

## Användning
Den grundläggande syntaxen för lvm-kommandot är:

```bash
lvm [alternativ] [argument]
```

## Vanliga alternativ
- `create`: Skapa en ny logisk volym.
- `remove`: Ta bort en logisk volym.
- `extend`: Utöka storleken på en logisk volym.
- `reduce`: Minska storleken på en logisk volym.
- `lvdisplay`: Visa information om logiska volymer.

## Vanliga exempel
### Skapa en logisk volym
För att skapa en ny logisk volym kan du använda följande kommando:

```bash
lvm lvcreate -n min_volym -L 10G min_vg
```
Detta skapar en logisk volym med namnet "min_volym" och storleken 10 GB i volymgruppen "min_vg".

### Ta bort en logisk volym
För att ta bort en logisk volym, använd:

```bash
lvm lvremove /dev/min_vg/min_volym
```
Detta tar bort logiska volymen "min_volym" från volymgruppen "min_vg".

### Utöka en logisk volym
För att utöka en logisk volym, kör:

```bash
lvm lvextend -L +5G /dev/min_vg/min_volym
```
Detta ökar storleken på "min_volym" med 5 GB.

### Minska en logisk volym
För att minska storleken på en logisk volym, använd:

```bash
lvm lvreduce -L -5G /dev/min_vg/min_volym
```
Detta minskar storleken på "min_volym" med 5 GB. Observera att du bör avmontera volymen innan du minskar den.

## Tips
- Se alltid till att säkerhetskopiera viktiga data innan du gör ändringar med LVM.
- Använd `lvdisplay` för att kontrollera status och egenskaper hos dina logiska volymer.
- Var försiktig när du minskar storleken på en logisk volym; se till att det inte finns några data som riskerar att förloras.