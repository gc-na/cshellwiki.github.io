# [Linux] Bash sftp brug: Overførsel af filer sikkert

## Oversigt
`sftp` (SSH File Transfer Protocol) er et netværksprotokol, der bruges til at overføre filer mellem en lokal og en fjern computer over en sikker forbindelse. Det er en del af SSH (Secure Shell) og giver en sikker måde at overføre filer på.

## Brug
Den grundlæggende syntaks for `sftp`-kommandoen er som følger:

```bash
sftp [options] [user@]host
```

## Almindelige muligheder
- `-b batchfile`: Angiver en batchfil, der indeholder en liste over kommandoer, der skal udføres.
- `-C`: Aktiverer komprimering for at reducere mængden af data, der overføres.
- `-i identity_file`: Angiver en specifik privat nøglefil til autentificering.
- `-P port`: Angiver en alternativ port til SSH-forbindelsen.
- `-v`: Aktiverer detaljeret output for fejlfinding.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `sftp`:

1. **Opret forbindelse til en fjernserver:**
   ```bash
   sftp user@hostname
   ```

2. **Overfør en fil fra den lokale maskine til fjernserveren:**
   ```bash
   sftp user@hostname
   put localfile.txt
   ```

3. **Overfør en fil fra fjernserveren til den lokale maskine:**
   ```bash
   sftp user@hostname
   get remotefile.txt
   ```

4. **Liste filer i den aktuelle fjernmappe:**
   ```bash
   sftp user@hostname
   ls
   ```

5. **Brug af batchfil til at overføre flere filer:**
   ```bash
   sftp -b batchfile.txt user@hostname
   ```

## Tips
- Brug `-v`-muligheden for at få mere information om forbindelsen, hvis du oplever problemer.
- Overvej at bruge en SSH-nøgle til autentificering for at forbedre sikkerheden og undgå at skulle indtaste adgangskoden hver gang.
- Hold din SFTP-klient opdateret for at sikre, at du har de nyeste sikkerhedsopdateringer og funktioner.