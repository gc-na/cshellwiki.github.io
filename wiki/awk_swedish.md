# [Linux] Bash awk användning: Bearbeta text och data

## Översikt
`awk` är ett kraftfullt textbehandlingsverktyg i Bash som används för att analysera och bearbeta data i textfiler. Det är särskilt användbart för att extrahera specifika kolumner, utföra beräkningar och manipulera textbaserad information.

## Användning
Den grundläggande syntaxen för `awk` ser ut så här:

```bash
awk [alternativ] 'mönster {åtgärd}' filnamn
```

## Vanliga alternativ
- `-F`: Anger fältavgränsare (standard är blanksteg).
- `-v`: Tillåter att variabler definieras innan skriptet körs.
- `-f`: Anger en fil som innehåller awk-programmet istället för att skriva det direkt i kommandoraden.

## Vanliga exempel

### Exempel 1: Visa specifika kolumner
För att visa den första och tredje kolumnen i en fil kan du använda:

```bash
awk '{print $1, $3}' fil.txt
```

### Exempel 2: Använda en anpassad fältavgränsare
Om du har en CSV-fil och vill använda kommatecken som avgränsare:

```bash
awk -F, '{print $1, $2}' fil.csv
```

### Exempel 3: Filtrera rader
För att visa rader där värdet i den andra kolumnen är större än 100:

```bash
awk '$2 > 100' fil.txt
```

### Exempel 4: Beräkna summan av en kolumn
För att beräkna summan av värden i den tredje kolumnen:

```bash
awk '{sum += $3} END {print sum}' fil.txt
```

## Tips
- Använd `-F` för att enkelt hantera olika avgränsare.
- Kom ihåg att `awk` är känsligt för blanksteg och format, så se till att din data är konsekvent.
- För mer komplexa skript, överväg att skriva dem i en separat fil och använd `-f` för att köra dem.