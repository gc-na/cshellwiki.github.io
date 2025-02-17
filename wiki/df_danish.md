# [Linux] Bash df Brug: Vis diskpladsinformation

## Oversigt
`df`-kommandoen bruges til at vise information om diskpladsen på filsystemer. Den giver brugeren indsigt i, hvor meget plads der er tilgængelig, hvor meget der er brugt, og hvilke filsystemer der er monteret.

## Brug
Den grundlæggende syntaks for `df`-kommandoen er som følger:

```
df [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h`: Viser størrelser i et menneskeligt læsbart format (f.eks. KB, MB, GB).
- `-T`: Viser filsystemtypen for hver monteret enhed.
- `-a`: Viser alle filsystemer, inklusive dem med 0 brugt plads.
- `-i`: Viser information om inode-brug i stedet for diskplads.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `df`-kommandoen:

1. **Vis diskplads i menneskeligt læsbart format:**
   ```bash
   df -h
   ```

2. **Vis diskplads med filsystemtype:**
   ```bash
   df -T
   ```

3. **Vis alle filsystemer, inklusive tomme:**
   ```bash
   df -a
   ```

4. **Vis inode-brug:**
   ```bash
   df -i
   ```

## Tips
- Brug `df -h` for hurtigt at få et overblik over diskpladsen i et format, der er nemt at forstå.
- Kombiner `df` med `grep` for at finde specifikke filsystemer, f.eks.:
  ```bash
  df -h | grep /dev/sda1
  ```
- Tjek regelmæssigt diskpladsen for at undgå problemer med pladsmangel, især på servere og systemer med begrænset lager.