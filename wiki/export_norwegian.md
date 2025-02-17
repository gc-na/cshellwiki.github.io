# [Linux] Bash export bruk: Setter miljøvariabler

## Oversikt
`export`-kommandoen i Bash brukes til å sette miljøvariabler, som gjør dem tilgjengelige for alle underprosesser som kjøres fra den nåværende shell-økten. Dette er nyttig for å dele konfigurasjonsinnstillinger og andre verdier mellom skript og programmer.

## Bruk
Grunnleggende syntaks for `export`-kommandoen er som følger:

```bash
export [alternativer] [argumenter]
```

## Vanlige alternativer
- `-n`: Fjerner eksporten av en variabel.
- `-p`: Viser alle eksporterte variabler.
- `VARIABEL=VERDI`: Setter en ny variabel og eksporterer den.

## Vanlige eksempler

1. **Eksportere en ny variabel:**
   ```bash
   export MY_VAR="Hei, verden!"
   ```

2. **Sjekke eksporterte variabler:**
   ```bash
   export -p
   ```

3. **Fjerne eksport av en variabel:**
   ```bash
   export -n MY_VAR
   ```

4. **Eksportere en variabel og kjøre et program:**
   ```bash
   export PATH="$PATH:/ny/sti"
   my_program
   ```

## Tips
- Husk at variabler som settes med `export` bare varer så lenge den nåværende shell-økten er aktiv. For å gjøre dem permanente, kan du legge dem til i filen `~/.bashrc` eller `~/.bash_profile`.
- Bruk alltid anførselstegn rundt verdier som inneholder mellomrom for å unngå feil.
- Sjekk alltid hvilke variabler som er eksportert med `export -p` for å unngå konflikter.