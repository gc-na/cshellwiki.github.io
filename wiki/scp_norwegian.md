# [Linux] Bash scp Bruk: Kopier filer sikkert mellom datamaskiner

## Oversikt
`scp` (Secure Copy Protocol) er et Bash-kommando som brukes til å kopiere filer og kataloger mellom datamaskiner over et nettverk. Det bruker SSH (Secure Shell) for å sikre dataoverføringen, noe som gjør det til et trygt alternativ for filoverføring.

## Bruk
Den grunnleggende syntaksen for `scp`-kommandoen er som følger:

```bash
scp [alternativer] [kilde] [mål]
```

## Vanlige alternativer
- `-r`: Kopierer kataloger rekursivt.
- `-P`: Angir portnummeret for SSH-tilkoblingen.
- `-i`: Spesifiserer en privat nøkkel for autentisering.
- `-v`: Aktiverer verbose-modus for mer detaljert utdata.
- `-C`: Aktiverer komprimering for å redusere overføringstiden.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `scp` kan brukes:

1. **Kopiere en fil fra lokal til ekstern server:**
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. **Kopiere en fil fra ekstern server til lokal maskin:**
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. **Kopiere en hel katalog fra lokal til ekstern server:**
   ```bash
   scp -r /path/to/local/directory/ user@remote_host:/path/to/remote/directory/
   ```

4. **Kopiere en fil til en spesifikk port:**
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

## Tips
- Sørg for at SSH-tjenesten kjører på den eksterne serveren før du prøver å bruke `scp`.
- Bruk `-v` alternativet for å feilsøke problemer med tilkoblingen.
- For store filer, vurder å bruke `-C` for å aktivere komprimering, noe som kan redusere overføringstiden.
- Husk å sjekke fil- og katalogrettigheter på både lokal og ekstern maskin for å unngå tilgangsproblemer.