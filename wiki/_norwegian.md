# [Linux] Bash @ bruk: Utfør kommandoer i bakgrunnen

## Oversikt
Kommandoen `@` brukes i Bash for å kjøre kommandoer i bakgrunnen, noe som lar deg fortsette å bruke terminalen mens prosessen kjører. Dette er nyttig for langvarige oppgaver som du ikke ønsker å vente på.

## Bruk
Grunnleggende syntaks for kommandoen er som følger:

```bash
@ [alternativer] [argumenter]
```

## Vanlige alternativer
- `&`: Kjører kommandoen i bakgrunnen.
- `jobs`: Viser en liste over bakgrunnsjobber.
- `fg`: Bring en bakgrunnsjobb til forgrunnen.
- `bg`: Fortsetter en stoppet jobb i bakgrunnen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `@` i Bash:

1. Kjøre en skriptfil i bakgrunnen:
   ```bash
   ./mitt_skript.sh &
   ```

2. Kjøre en langvarig prosess, som en server, i bakgrunnen:
   ```bash
   python -m http.server &
   ```

3. Sjekke status på bakgrunnsjobber:
   ```bash
   jobs
   ```

4. Bring en bakgrunnsjobb til forgrunnen:
   ```bash
   fg %1
   ```

5. Fortsette en stoppet jobb i bakgrunnen:
   ```bash
   bg %1
   ```

## Tips
- Bruk `jobs` for å holde oversikt over bakgrunnsjobber.
- Husk at du kan bruke `nohup` sammen med `&` for å sikre at jobben fortsetter å kjøre selv om du logger ut.
- Vær oppmerksom på ressursbruken til bakgrunnsjobber, spesielt på servere.