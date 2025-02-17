# [Linux] Bash curl användning: Hämta data från webben

## Översikt
`curl` är ett kommandoradsverktyg som används för att överföra data till och från servrar. Det stöder olika protokoll, inklusive HTTP, HTTPS, FTP och många fler. Med `curl` kan du enkelt hämta filer, skicka data och interagera med API:er.

## Användning
Den grundläggande syntaxen för `curl` är:

```bash
curl [alternativ] [argument]
```

## Vanliga alternativ
- `-X`: Anger HTTP-metoden som ska användas (t.ex. GET, POST).
- `-d`: Skickar data med POST-förfrågningar.
- `-H`: Lägger till en HTTP-header.
- `-o`: Sparar svaret i en fil.
- `-I`: Hämtar endast HTTP-huvuden.
- `-L`: Följ omdirigeringar.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `curl`:

### Hämta en webbsida
```bash
curl https://www.example.com
```

### Hämta en fil och spara den lokalt
```bash
curl -o fil.txt https://www.example.com/fil.txt
```

### Skicka en POST-förfrågan med data
```bash
curl -X POST -d "namn=John&ålder=30" https://www.example.com/api
```

### Lägga till en HTTP-header
```bash
curl -H "Authorization: Bearer TOKEN" https://www.example.com/api
```

### Hämta endast HTTP-huvuden
```bash
curl -I https://www.example.com
```

## Tips
- Använd `-L` för att följa omdirigeringar automatiskt.
- Kontrollera alltid svaret från servern för att säkerställa att din begäran lyckades.
- Använd `-v` för att få detaljerad information om vad som händer under överföringen, vilket är användbart för felsökning.