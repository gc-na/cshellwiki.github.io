# [Linux] Bash basename brug: Hent filnavn fra en sti

## Oversigt
`basename`-kommandoen bruges til at hente filnavnet fra en given sti. Den fjerner eventuelle foranstillede stier og efterlader kun selve filnavnet, hvilket gør det nyttigt i scripts og kommandolinjeoperationer.

## Brug
Den grundlæggende syntaks for `basename`-kommandoen er:

```bash
basename [options] [arguments]
```

## Almindelige muligheder
- `-a`: Behandl alle argumenter som en liste og returner filnavnene for hver.
- `-s`: Angiv en suffix, der skal fjernes fra filnavnet.
- `--help`: Vis hjælp og afslut.
- `--version`: Vis versionsinformation.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `basename` kan bruges:

1. Hent filnavnet fra en sti:
   ```bash
   basename /path/to/file.txt
   ```
   Output: `file.txt`

2. Hent filnavnet uden suffix:
   ```bash
   basename /path/to/file.txt .txt
   ```
   Output: `file`

3. Behandl flere stier:
   ```bash
   basename -a /path/to/file1.txt /path/to/file2.txt
   ```
   Output:
   ```
   file1.txt
   file2.txt
   ```

4. Hent filnavnet fra en sti med en anden suffix:
   ```bash
   basename /path/to/file.log .log
   ```
   Output: `file`

## Tips
- Brug `basename` i scripts til at isolere filnavne fra stier, hvilket kan være nyttigt ved filbehandling.
- Kombiner `basename` med andre kommandoer som `find` for at få en liste over filnavne fra en mappe.
- Vær opmærksom på, at `basename` kun returnerer det sidste segment af stien, så hvis du har brug for hele stien, skal du bruge andre metoder.