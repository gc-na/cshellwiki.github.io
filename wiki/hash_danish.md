# [Linux] Bash hash brug: Håndtering af kommandohashes

## Oversigt
Bash-kommandoen `hash` bruges til at administrere og vise den interne cache af kommandohashes. Den hjælper med at optimere udførelsen af kommandoer ved at gemme stierne til de senest brugte eksekverbare filer.

## Brug
Den grundlæggende syntaks for `hash`-kommandoen er:

```bash
hash [options] [arguments]
```

## Almindelige muligheder
- `-r`: Rydder den interne cache af kommandoer.
- `-p`: Angiver en specifik sti til en kommando.
- `-l`: Viser en liste over alle gemte hashes.

## Almindelige eksempler

1. **Visning af gemte hashes:**
   For at se de nuværende gemte kommandoer kan du bruge:
   ```bash
   hash
   ```

2. **Rydde cachen:**
   Hvis du vil rydde den interne cache, kan du gøre det med:
   ```bash
   hash -r
   ```

3. **Tilføje en specifik sti til en kommando:**
   Hvis du har en kommando i en bestemt mappe, kan du tilføje den til cachen:
   ```bash
   hash -p /path/to/command command_name
   ```

4. **Liste alle gemte hashes:**
   For at få en liste over alle gemte kommandoer med deres stier, brug:
   ```bash
   hash -l
   ```

## Tips
- Brug `hash` til at forbedre hastigheden på kommandoudførelse ved at cache ofte brugte kommandoer.
- Husk at rydde cachen, hvis du ændrer placeringen af en eksekverbar fil, så du undgår at køre en forældet version.
- Tjek regelmæssigt de gemte hashes for at sikre, at de stadig er relevante for dit arbejde.