# [Linux] Bash ps Brug: Vise procesinformation

## Oversigt
`ps`-kommandoen bruges til at vise information om aktive processer på systemet. Den giver brugerne mulighed for at se, hvilke processer der kører, deres status og ressourcer, de bruger.

## Brug
Den grundlæggende syntaks for `ps`-kommandoen er:

```bash
ps [options] [arguments]
```

## Almindelige muligheder
- `-e` eller `-A`: Viser alle processer.
- `-f`: Viser fuld format, inklusive forældreprocesser.
- `-u [bruger]`: Viser processer for en specifik bruger.
- `-aux`: Viser alle processer med detaljeret information.
- `--sort`: Sorterer output baseret på en specifik kolonne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `ps` kan bruges:

1. **Vis alle processer:**
   ```bash
   ps -e
   ```

2. **Vis processer med fuld format:**
   ```bash
   ps -f
   ```

3. **Vis processer for en specifik bruger:**
   ```bash
   ps -u username
   ```

4. **Vis alle processer med detaljeret information:**
   ```bash
   ps aux
   ```

5. **Sortér processer efter hukommelsesforbrug:**
   ```bash
   ps aux --sort=-%mem
   ```

## Tips
- Brug `man ps` for at få adgang til den fulde manual og lære om flere muligheder.
- Kombiner `ps` med `grep` for at filtrere output. For eksempel, for at finde en bestemt proces:
  ```bash
  ps aux | grep process_name
  ```
- Overvej at bruge `top` eller `htop` for en mere interaktiv visning af processer.