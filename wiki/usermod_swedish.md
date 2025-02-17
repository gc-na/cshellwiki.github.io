# [Linux] Bash usermod användning: Hantera användarkonton

## Översikt
`usermod` är ett kommandon i Linux som används för att ändra inställningar för befintliga användarkonton. Med detta kommando kan du justera olika aspekter av användarkontot, såsom gruppmedlemskap, användarnamn och hemkatalog.

## Användning
Den grundläggande syntaxen för `usermod` är:

```bash
usermod [alternativ] [argument]
```

## Vanliga alternativ
- `-aG`: Lägger till användaren till en eller flera grupper utan att ta bort dem från andra grupper.
- `-d`: Ändrar användarens hemkatalog.
- `-l`: Ändrar användarnamnet.
- `-s`: Ändrar användarens standard skal (shell).
- `-u`: Ändrar användarens ID (UID).

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `usermod`:

### Lägga till en användare till en grupp
För att lägga till användaren `john` till gruppen `sudo` kan du använda följande kommando:

```bash
sudo usermod -aG sudo john
```

### Ändra hemkatalog
Om du vill ändra hemkatalogen för användaren `john` till `/home/john_new`, kör du:

```bash
sudo usermod -d /home/john_new john
```

### Ändra användarnamn
För att ändra användarnamnet från `john` till `johnny`, använd:

```bash
sudo usermod -l johnny john
```

### Ändra standard skal
För att ändra användarens skal till `/bin/bash`, använd:

```bash
sudo usermod -s /bin/bash john
```

## Tips
- Använd alltid `sudo` för att köra `usermod` om du inte är inloggad som root-användare.
- Kontrollera alltid att du har en säkerhetskopia av användardata innan du gör ändringar.
- Använd `id [användarnamn]` för att verifiera användarens grupper och ID efter att du har gjort ändringar.