# [Linux] Bash w bruksområde: viser innloggede brukere og systemaktivitet

## Oversikt
`w`-kommandoen viser informasjon om innloggede brukere og deres aktivitet på systemet. Den gir en oversikt over hvilke brukere som er pålogget, hva de gjør, og hvor lenge de har vært aktive.

## Bruk
Den grunnleggende syntaksen for `w`-kommandoen er:

```bash
w [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h`: Skru av overskriften i utdataene.
- `-s`: Vis en kortere versjon av utdataene.
- `-u`: Vis brukernavn i stedet for bruker-ID.

## Vanlige eksempler

1. **Vis alle innloggede brukere:**
   ```bash
   w
   ```

2. **Vis innloggede brukere uten overskrift:**
   ```bash
   w -h
   ```

3. **Vis en kortere versjon av utdataene:**
   ```bash
   w -s
   ```

4. **Vis informasjon om en spesifikk bruker:**
   ```bash
   w username
   ```

## Tips
- Bruk `w` regelmessig for å overvåke systemaktivitet og innloggede brukere.
- Kombiner `w` med andre kommandoer som `grep` for å filtrere utdataene basert på spesifikke brukernavn.
- Vær oppmerksom på at `w` kan vise sensitive data, så bruk den med forsiktighet på delte systemer.