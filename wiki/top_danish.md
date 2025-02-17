# [Linux] Bash top brug: Visning af systemets processer i realtid

## Oversigt
`top`-kommandoen bruges til at vise en dynamisk liste over aktive processer på et Unix-lignende system. Den giver brugeren mulighed for at overvåge systemets ressourcer, såsom CPU- og hukommelsesforbrug, i realtid.

## Brug
Den grundlæggende syntaks for `top`-kommandoen er:

```bash
top [options] [arguments]
```

## Almindelige muligheder
- `-d <sekunder>`: Angiver opdateringsintervallet i sekunder.
- `-n <antal>`: Angiver antallet af opdateringer, før `top` afsluttes.
- `-u <bruger>`: Viser kun processer, der tilhører den angivne bruger.
- `-p <pid>`: Overvåg kun den angivne proces ID.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `top`:

1. **Start `top` med standardindstillinger**:
   ```bash
   top
   ```

2. **Ændre opdateringsintervallet til 2 sekunder**:
   ```bash
   top -d 2
   ```

3. **Vis kun processer for en bestemt bruger**:
   ```bash
   top -u username
   ```

4. **Vis kun en specifik proces ved hjælp af dens PID**:
   ```bash
   top -p 1234
   ```

5. **Kør `top` i et begrænset antal opdateringer**:
   ```bash
   top -n 5
   ```

## Tips
- For at afslutte `top`, tryk på `q`.
- Du kan sortere processerne ved at trykke på `M` for at sortere efter hukommelsesforbrug eller `P` for at sortere efter CPU-forbrug.
- Brug `h` for at få hjælp til de tilgængelige tastaturgenveje, mens `top` kører.
- Overvej at bruge `htop`, som er en mere brugervenlig version af `top`, hvis det er tilgængeligt på dit system.