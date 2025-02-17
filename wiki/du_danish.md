# [Linux] Bash du brug: viser diskforbrug

## Oversigt
`du` (disk usage) er et Bash-kommando, der bruges til at vise, hvor meget diskplads en fil eller en mappe optager. Det er nyttigt til at identificere store filer eller mapper, der kan tage unødvendig plads på dit system.

## Brug
Den grundlæggende syntaks for `du`-kommandoen er:

```bash
du [options] [arguments]
```

## Almindelige muligheder
- `-h`: Viser størrelser i et menneskeligt læsbart format (f.eks. KB, MB).
- `-s`: Viser kun den samlede størrelse for hver angivet mappe eller fil.
- `-a`: Inkluderer alle filer i output, ikke kun mapper.
- `-c`: Viser en samlet sum af størrelserne i slutningen af outputtet.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `du`:

1. **Vis diskforbrug for den aktuelle mappe:**
   ```bash
   du
   ```

2. **Vis diskforbrug i menneskeligt læsbart format:**
   ```bash
   du -h
   ```

3. **Vis den samlede størrelse af en specifik mappe:**
   ```bash
   du -sh /sti/til/mappe
   ```

4. **Vis diskforbrug for alle filer og mapper i den aktuelle mappe:**
   ```bash
   du -a
   ```

5. **Vis diskforbrug med en samlet sum:**
   ```bash
   du -ch
   ```

## Tips
- Brug `du -sh *` for hurtigt at se størrelsen på alle filer og mapper i den aktuelle mappe.
- Kombiner `du` med `sort` for at finde de største mapper:
  ```bash
  du -h | sort -hr
  ```
- Vær opmærksom på, at `du` kan tage tid at køre på store filsystemer, så vær tålmodig, når du arbejder med mange filer.