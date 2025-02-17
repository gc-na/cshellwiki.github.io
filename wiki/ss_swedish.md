# [Linux] Bash ss användning: Visa nätverksanslutningar

## Översikt
Kommandot `ss` används för att visa socket-statistik och nätverksanslutningar på Linux-system. Det är ett kraftfullt verktyg för att övervaka och felsöka nätverksproblem genom att ge detaljerad information om aktiva anslutningar och deras tillstånd.

## Användning
Den grundläggande syntaxen för kommandot `ss` är:

```
ss [alternativ] [argument]
```

## Vanliga alternativ
- `-t`: Visa TCP-anslutningar.
- `-u`: Visa UDP-anslutningar.
- `-l`: Visa endast lyssnande sockets.
- `-p`: Visa processinformation kopplad till sockets.
- `-n`: Visa numeriska adresser istället för att försöka lösa domännamn.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `ss`:

### Visa alla aktiva anslutningar
```bash
ss
```

### Visa endast TCP-anslutningar
```bash
ss -t
```

### Visa endast UDP-anslutningar
```bash
ss -u
```

### Visa lyssnande sockets
```bash
ss -l
```

### Visa detaljerad information inklusive processer
```bash
ss -t -p
```

### Visa numeriska adresser
```bash
ss -n
```

## Tips
- Använd `ss -t -l` för att snabbt se vilka TCP-portar som lyssnar på inkommande anslutningar.
- Kombinera alternativ för att få mer specifik information, till exempel `ss -t -u -n` för att visa både TCP och UDP utan domännamn.
- För att få en översikt över nätverksanvändning kan du använda `ss -s` för att se sammanfattning av anslutningar.