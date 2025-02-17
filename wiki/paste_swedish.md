# [Linux] Bash paste användning: Sammanfoga filer rad för rad

## Översikt
Kommandot `paste` används för att sammanfoga filer rad för rad. Det tar flera filer som indata och kombinerar dem så att varje rad från varje fil placeras bredvid varandra, vilket skapar en ny utdatafil.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
paste [alternativ] [argument]
```

## Vanliga alternativ
- `-d` : Anger avgränsare mellan sammanfogade rader. Standardavgränsare är tab.
- `-s` : Sammanfogar raderna i varje fil sekventiellt istället för rad för rad.
- `-z` : Behandlar null-terminerade strängar istället för nya rader.

## Vanliga exempel

### Exempel 1: Sammanfoga två filer rad för rad
Anta att vi har två filer, `fil1.txt` och `fil2.txt`:

```bash
paste fil1.txt fil2.txt
```

Detta kommando kommer att sammanfoga innehållet i `fil1.txt` och `fil2.txt` rad för rad.

### Exempel 2: Använda en specifik avgränsare
Om du vill använda ett kommatecken som avgränsare istället för en tab:

```bash
paste -d ',' fil1.txt fil2.txt
```

Detta kommer att sammanfoga raderna med ett kommatecken mellan dem.

### Exempel 3: Sammanfoga filer sekventiellt
För att sammanfoga raderna i en fil sekventiellt:

```bash
paste -s fil1.txt
```

Detta kommer att sammanfoga alla rader i `fil1.txt` till en enda rad.

### Exempel 4: Sammanfoga filer med null-terminerade strängar
Om du har filer med null-terminerade strängar:

```bash
paste -z fil1.txt fil2.txt
```

Detta kommer att hantera filerna korrekt med null-terminering.

## Tips
- Använd `-d` för att anpassa avgränsare när du behöver ett specifikt format.
- Tänk på att `paste` inte ändrar de ursprungliga filerna; det skapar bara en ny utdata.
- Kombinera `paste` med andra kommandon som `sort` eller `uniq` för mer avancerad datahantering.