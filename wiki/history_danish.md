# [Linux] Bash history brug: Viser tidligere kommandoer

## Oversigt
Kommandoen `history` i Bash viser en liste over de tidligere udførte kommandoer i den aktuelle shell-session. Dette kan være nyttigt til at genfinde og genbruge kommandoer uden at skulle skrive dem igen.

## Brug
Den grundlæggende syntaks for `history`-kommandoen er:

```bash
history [options] [arguments]
```

## Almindelige muligheder
- `-c`: Rydder historikken.
- `-d offset`: Sletter den angivne kommando fra historikken.
- `-a`: Tilføjer den aktuelle session til historikfilen.
- `-r`: Læser historikken fra historikfilen.
- `n`: Viser de sidste n kommandoer.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `history`:

1. **Vis alle tidligere kommandoer:**
   ```bash
   history
   ```

2. **Vis de seneste 10 kommandoer:**
   ```bash
   history 10
   ```

3. **Slet en specifik kommando fra historikken:**
   ```bash
   history -d 5
   ```

4. **Ryd historikken:**
   ```bash
   history -c
   ```

5. **Gem den aktuelle historik til filen:**
   ```bash
   history -a
   ```

## Tips
- Brug `!n` for at køre kommandoen med nummer n fra historikken.
- Du kan søge i historikken ved at trykke `Ctrl + r` og begynde at skrive en del af kommandoen.
- Overvej at tilpasse din historik ved at ændre indstillingerne i din `.bashrc`-fil for at gemme flere kommandoer eller ændre formatet.