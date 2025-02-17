# [Linux] Bash hexdump brug: Vis hexadecimale repræsentationer af filer

## Oversigt
Hexdump-kommandoen bruges til at vise den hexadecimale repræsentation af binære filer. Den kan være nyttig til fejlfinding, analyse af filindhold eller når man ønsker at se data i et mere læsbart format.

## Brug
Den grundlæggende syntaks for hexdump-kommandoen er:

```bash
hexdump [options] [arguments]
```

## Almindelige muligheder
- `-C`: Vis output i en kombination af hex og ASCII.
- `-n <antal>`: Angiv det antal bytes, der skal vises.
- `-v`: Vis alle data, selv hvis der er gentagelser.
- `-e <format>`: Angiv et brugerdefineret format for output.

## Almindelige eksempler

1. **Vis hele filens hexadecimale indhold**:
   ```bash
   hexdump fil.txt
   ```

2. **Vis de første 16 bytes af en fil**:
   ```bash
   hexdump -n 16 fil.txt
   ```

3. **Vis filens indhold i både hex og ASCII**:
   ```bash
   hexdump -C fil.txt
   ```

4. **Brug et brugerdefineret format**:
   ```bash
   hexdump -e '16/1 "%02x " "\n"' fil.txt
   ```

5. **Vis alle data, selv hvis der er gentagelser**:
   ```bash
   hexdump -v fil.txt
   ```

## Tips
- Brug `-C` for at få en bedre forståelse af filens indhold, da det viser både hex og ASCII.
- Vær opmærksom på filens størrelse, da store filer kan producere meget output. Overvej at bruge `-n` for at begrænse outputtet.
- Eksperimenter med `-e` for at tilpasse formatet til dine behov, hvilket kan være nyttigt i scripts.