# [Linux] Bash scp användning: Överför filer säkert mellan datorer

## Översikt
`scp` (Secure Copy Protocol) är ett kommandoradsverktyg som används för att överföra filer och kataloger mellan datorer över ett nätverk. Det använder SSH-protokollet för att säkerställa att överföringen är säker och krypterad.

## Användning
Den grundläggande syntaxen för `scp` är:

```bash
scp [alternativ] [källa] [destination]
```

## Vanliga alternativ
- `-r`: Kopiera kataloger rekursivt.
- `-P`: Ange portnummer för SSH-servern (observera att det är en stor bokstav P).
- `-i`: Ange en specifik identitetsfil (privat nyckel) för autentisering.
- `-v`: Aktivera detaljerad utdata för felsökning.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `scp`:

1. **Överföra en fil från lokal dator till en fjärrdator:**
   ```bash
   scp /lokal/sökväg/till/fil.txt användare@fjärrdator:/fjärr/sökväg/
   ```

2. **Överföra en fil från en fjärrdator till lokal dator:**
   ```bash
   scp användare@fjärrdator:/fjärr/sökväg/fil.txt /lokal/sökväg/
   ```

3. **Överföra en katalog rekursivt:**
   ```bash
   scp -r /lokal/sökväg/till/katalog användare@fjärrdator:/fjärr/sökväg/
   ```

4. **Använda en specifik port:**
   ```bash
   scp -P 2222 /lokal/sökväg/till/fil.txt användare@fjärrdator:/fjärr/sökväg/
   ```

## Tips
- Kontrollera alltid att du har rätt behörigheter på både lokal och fjärrdator innan du försöker överföra filer.
- Använd `-v` för att få mer information om överföringsprocessen, vilket kan vara användbart för felsökning.
- För att öka säkerheten, överväg att använda SSH-nycklar istället för lösenord för autentisering.