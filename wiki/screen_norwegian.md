# [Linux] Bash screen bruk: Administrere terminaløkter

## Oversikt
`screen` er et kraftig verktøy som lar brukere opprette og administrere flere terminaløkter i en enkelt vindu. Det er spesielt nyttig for å kjøre langvarige prosesser, da det lar deg koble fra og til økter uten å miste fremdriften.

## Bruk
Grunnleggende syntaks for `screen`-kommandoen er som følger:

```bash
screen [alternativer] [argumenter]
```

## Vanlige alternativer
- `-S <navn>`: Gi økten et spesifikt navn.
- `-d -r`: Koble fra en eksisterende økt og koble til den igjen.
- `-list`: Vis en liste over aktive `screen`-økter.
- `-L`: Aktiver logging av utdata til en fil.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `screen`:

1. Opprett en ny `screen`-økt:
   ```bash
   screen
   ```

2. Opprett en ny `screen`-økt med et spesifikt navn:
   ```bash
   screen -S min_økt
   ```

3. Koble fra en `screen`-økt (trykk `Ctrl + A`, deretter `D`):
   ```bash
   # Ingen spesifikk kommando, bare trykk Ctrl + A, så D
   ```

4. Koble til en eksisterende `screen`-økt:
   ```bash
   screen -r min_økt
   ```

5. Vis en liste over aktive `screen`-økter:
   ```bash
   screen -list
   ```

6. Aktiver logging av utdata:
   ```bash
   screen -L
   ```

## Tips
- Bruk `Ctrl + A` etterfulgt av `?` for å se en liste over hurtigtaster i `screen`.
- Hvis du jobber med flere økter, kan det være nyttig å gi dem meningsfulle navn for enklere identifikasjon.
- Husk å bruke `exit`-kommandoen for å avslutte en `screen`-økt når du er ferdig, slik at du ikke etterlater unødvendige prosesser kjørende.