# [Linux] Bash du bruken: viser diskbruk

## Oversikt
`du` (disk usage) er en kommando i Bash som brukes til å estimere og vise mengden diskplass som brukes av filer og kataloger. Den gir en oversikt over hvor mye plass som er opptatt på filsystemet, noe som er nyttig for systemadministrasjon og vedlikehold.

## Bruk
Grunnleggende syntaks for `du`-kommandoen er:

```bash
du [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h`: Viser størrelser i "human-readable" format (f.eks. KB, MB).
- `-s`: Viser total diskbruk for hver angitt katalog i stedet for detaljerte oppføringer.
- `-a`: Viser diskbruk for både filer og kataloger.
- `-c`: Gir en total oppsummering av diskbruken for alle angitte filer og kataloger.
- `--max-depth=N`: Begrens dybden av katalogstrukturen som skal vises til N nivåer.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `du`:

1. **Vis diskbruk for gjeldende katalog:**
   ```bash
   du
   ```

2. **Vis diskbruk i "human-readable" format:**
   ```bash
   du -h
   ```

3. **Vis total diskbruk for en spesifikk katalog:**
   ```bash
   du -sh /sti/til/katalog
   ```

4. **Vis diskbruk for alle filer og kataloger i en katalog:**
   ```bash
   du -ah /sti/til/katalog
   ```

5. **Vis diskbruk med oppsummering:**
   ```bash
   du -ch /sti/til/katalog/*
   ```

6. **Vis diskbruk med begrenset dybde:**
   ```bash
   du --max-depth=1 -h /sti/til/katalog
   ```

## Tips
- Bruk `-h` for å gjøre resultatene lettere å lese, spesielt når du arbeider med store datamengder.
- Kombiner `du` med `sort` for å sortere katalogene etter størrelse:
  ```bash
  du -h /sti/til/katalog | sort -hr
  ```
- Vær oppmerksom på at `du` kan ta tid å kjøre i store filsystemer, så vær tålmodig når du analyserer diskbruk.