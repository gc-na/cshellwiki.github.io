# [Linux] Bash sftp användning: Överför filer säkert

## Översikt
`sftp` (Secure File Transfer Protocol) är ett nätverksprotokoll som används för att överföra filer mellan datorer på ett säkert sätt. Det fungerar över SSH (Secure Shell) och ger en säker kanal för filöverföring, vilket gör det till ett populärt val för att hantera filer på fjärrservrar.

## Användning
Den grundläggande syntaxen för `sftp`-kommandot är:

```bash
sftp [alternativ] [användare@värd]
```

## Vanliga alternativ
- `-P port`: Ange en specifik port för anslutning.
- `-i fil`: Ange en specifik nyckelfil för autentisering.
- `-o alternativ`: Ange specifika SSH-alternativ.
- `-v`: Aktivera detaljerad (verbose) utdata för felsökning.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `sftp`:

### Ansluta till en fjärrserver
För att ansluta till en fjärrserver med användarnamn `user` och värd `example.com`:

```bash
sftp user@example.com
```

### Ladda upp en fil
För att ladda upp en fil som heter `localfile.txt` till den aktuella mappen på fjärrservern:

```bash
put localfile.txt
```

### Ladda ner en fil
För att ladda ner en fil som heter `remotefile.txt` från fjärrservern till den lokala datorn:

```bash
get remotefile.txt
```

### Lista filer i en katalog
För att lista filer i den aktuella katalogen på fjärrservern:

```bash
ls
```

### Byta katalog
För att byta till en annan katalog på fjärrservern:

```bash
cd /path/to/remote/directory
```

## Tips
- Använd `-P` alternativet om din fjärrserver använder en annan port än standardporten 22.
- För att öka säkerheten, använd nyckelbaserad autentisering istället för lösenord.
- Kontrollera alltid filrättigheter efter överföring för att säkerställa att de är korrekta.