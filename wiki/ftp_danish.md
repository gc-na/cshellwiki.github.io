# [Linux] Bash ftp brug: Overførsel af filer via FTP

## Oversigt
`ftp` (File Transfer Protocol) er en standard netværksprotokol, der bruges til at overføre filer mellem en klient og en server over et TCP-baseret netværk. Denne kommando giver brugerne mulighed for at uploade, downloade og administrere filer på en FTP-server.

## Brug
Den grundlæggende syntaks for `ftp`-kommandoen er som følger:

```bash
ftp [muligheder] [argumenter]
```

## Almindelige muligheder
- `-i`: Slå interaktiv mode fra, så du kan overføre filer uden at blive bedt om bekræftelse.
- `-n`: Forhindrer automatisk login til serveren.
- `-v`: Aktiverer detaljeret output, hvilket kan være nyttigt til fejlfinding.
- `-g`: Tillader brugen af globbing (wildcards) i filnavne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `ftp`-kommandoen:

1. **Opret forbindelse til en FTP-server:**
   ```bash
   ftp ftp.example.com
   ```

2. **Log ind med brugernavn og adgangskode:**
   ```bash
   ftp
   Name (ftp.example.com:brugernavn): dit_brugernavn
   Password: din_adgangskode
   ```

3. **Download en fil fra serveren:**
   ```bash
   get filnavn.txt
   ```

4. **Upload en fil til serveren:**
   ```bash
   put lokal_fil.txt
   ```

5. **Liste filer i den aktuelle mappe på serveren:**
   ```bash
   ls
   ```

## Tips
- Brug `-i` muligheden, når du overfører store filer for at undgå at blive bedt om bekræftelse for hver fil.
- Tjek altid forbindelsen til serveren ved at bruge `ping` før du forsøger at oprette forbindelse med `ftp`.
- For mere sikkerhed, overvej at bruge `sftp` (SSH File Transfer Protocol) i stedet for `ftp`, da det krypterer data under overførslen.