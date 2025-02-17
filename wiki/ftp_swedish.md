# [Linux] Bash ftp användning: Överför filer med FTP-protokollet

## Översikt
Kommandot `ftp` används för att överföra filer mellan datorer över ett nätverk med hjälp av File Transfer Protocol (FTP). Det möjliggör både nedladdning och uppladdning av filer till och från en FTP-server.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
ftp [alternativ] [värd]
```

Där `[värd]` är adressen till FTP-servern du vill ansluta till.

## Vanliga alternativ
- `-i`: Inaktiverar interaktiv läge, vilket gör att överföringar inte stoppas för att be om bekräftelse.
- `-n`: Förhindrar automatisk inloggning till FTP-servern.
- `-v`: Aktiverar detaljerad utdata, vilket ger mer information om vad som händer under överföringen.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `ftp`-kommandot:

### Ansluta till en FTP-server
```bash
ftp ftp.example.com
```

### Ladda ner en fil
```bash
get filnamn.txt
```

### Ladda upp en fil
```bash
put filnamn.txt
```

### Lista filer i den aktuella katalogen
```bash
ls
```

### Byta katalog på servern
```bash
cd /mapp/namn
```

## Tips
- Använd `-i` alternativet för att undvika bekräftelsefrågor vid överföring av flera filer.
- Kom ihåg att använda `bye` eller `quit` för att avsluta FTP-sessionen korrekt.
- Kontrollera alltid filrättigheter och ägarskap efter uppladdning för att säkerställa att filerna är tillgängliga som avsett.