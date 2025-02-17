# [Linux] Bash vgcreate användning: Skapa en ny volymgrupp

## Översikt
Kommandot `vgcreate` används för att skapa en ny volymgrupp i Linux Logical Volume Manager (LVM). En volymgrupp är en samling av logiska volymer som kan hanteras som en enhet, vilket gör det enklare att hantera lagringsutrymme.

## Användning
Den grundläggande syntaxen för kommandot är:

```
vgcreate [alternativ] [namn på volymgrupp] [fysisk volym...]
```

## Vanliga alternativ
- `-s, --stripes <antal>`: Anger antalet strimmor för volymgruppen.
- `-p, --max-pv <antal>`: Anger det maximala antalet fysiska volymer som kan ingå i volymgruppen.
- `-f, --force`: Tvingar skapandet av volymgruppen även om vissa kontroller misslyckas.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `vgcreate`:

1. Skapa en volymgrupp med namnet `vg01` med en fysisk volym `/dev/sdb1`:
   ```bash
   vgcreate vg01 /dev/sdb1
   ```

2. Skapa en volymgrupp med flera fysiska volymer:
   ```bash
   vgcreate vg02 /dev/sdb1 /dev/sdc1
   ```

3. Skapa en volymgrupp med specifika alternativ:
   ```bash
   vgcreate -s 64M -p 16 vg03 /dev/sdb1
   ```

## Tips
- Kontrollera alltid att de fysiska volymerna är korrekt konfigurerade innan du skapar en volymgrupp.
- Använd `vgdisplay` för att verifiera att volymgruppen har skapats korrekt.
- Tänk på att namnge volymgrupper på ett meningsfullt sätt för att underlätta hanteringen av lagringsresurser.