# [Linux] Bash netcat användning: Verktyg för nätverkskommunikation

## Översikt
Netcat, ofta kallad "schweizisk armékniv" för nätverksprotokoll, är ett kraftfullt verktyg för att läsa och skriva data över nätverksanslutningar. Det kan användas för att skapa TCP- eller UDP-anslutningar, vilket gör det användbart för felsökning och nätverksanalys.

## Användning
Den grundläggande syntaxen för netcat är:

```
netcat [alternativ] [argument]
```

## Vanliga alternativ
- `-l`: Lyssna på en port för inkommande anslutningar.
- `-p`: Ange portnumret som ska användas.
- `-u`: Använd UDP istället för TCP.
- `-v`: Aktivera verbose-läge för mer detaljerad utdata.
- `-w`: Ange timeout i sekunder för anslutningen.

## Vanliga exempel
### Skapa en enkel TCP-server
För att starta en server som lyssnar på port 1234:
```bash
netcat -l -p 1234
```

### Ansluta till en server
För att ansluta till en server på port 1234:
```bash
netcat [server-ip] 1234
```

### Skicka en fil
För att skicka en fil till en annan dator:
1. På mottagarsidan, lyssna på en port:
   ```bash
   netcat -l -p 1234 > mottagen_fil.txt
   ```
2. På avsändarsidan, skicka filen:
   ```bash
   netcat [mottagar-ip] 1234 < fil_att_skicka.txt
   ```

### Skanna öppna portar
För att skanna efter öppna portar på en server:
```bash
netcat -zv [server-ip] 1-1000
```

## Tips
- Använd `-v` för att få mer information om anslutningar och överföringar.
- Var försiktig med att använda netcat på offentliga nätverk, eftersom det kan exponera känslig information.
- Kombinera netcat med andra kommandon för att skapa kraftfulla skript för nätverksanalys och felsökning.