# [Linux] Bash iotop användning: Övervaka disk I/O-användning

## Översikt
Kommandot `iotop` används för att övervaka disk I/O-användning i realtid. Det visar vilka processer som använder mest diskresurser, vilket är användbart för att identifiera flaskhalsar och optimera systemprestanda.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
iotop [alternativ] [argument]
```

## Vanliga alternativ
- `-o`, `--only`: Visa endast processer som för närvarande gör I/O.
- `-b`, `--batch`: Kör i batch-läge, vilket är användbart för att logga utdata till en fil.
- `-d`, `--delay`: Ange fördröjning i sekunder mellan uppdateringar (standard är 1 sekund).
- `-p`, `--pid`: Visa endast processer med angivet process-ID.

## Vanliga exempel
För att starta `iotop` och se alla processer som gör I/O:

```bash
iotop
```

För att visa endast processer som för närvarande gör I/O:

```bash
iotop -o
```

För att köra `iotop` i batch-läge med en fördröjning på 2 sekunder mellan uppdateringar:

```bash
iotop -b -d 2
```

För att övervaka en specifik process med ett angivet PID (t.ex. PID 1234):

```bash
iotop -p 1234
```

## Tips
- Använd `iotop` med `sudo` för att få fullständig information om alla processer, eftersom vissa processer kan vara begränsade för vanliga användare.
- Kombinera `iotop` med andra verktyg som `htop` för en mer omfattande systemövervakning.
- Om du planerar att logga utdata, överväg att använda `-b` för att underlätta analysen av loggar senare.