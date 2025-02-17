# [Linux] Bash socat brug: Et værktøj til at oprette forbindelser mellem to strømme

## Oversigt
`socat` (SOcket CAT) er et kraftfuldt værktøj, der bruges til at etablere forbindelser mellem to strømme, såsom netværksforbindelser, filer eller enheder. Det fungerer som en proxy, der kan videresende data mellem forskellige input- og outputkilder.

## Brug
Den grundlæggende syntaks for `socat`-kommandoen er:

```bash
socat [options] [arguments]
```

## Almindelige muligheder
- `-d`: Aktiverer debug-udskrift, hvilket kan være nyttigt til fejlfinding.
- `-v`: Viser detaljerede oplysninger om data, der sendes og modtages.
- `TCP:<host>:<port>`: Opretter en TCP-forbindelse til den angivne vært og port.
- `UDP:<host>:<port>`: Opretter en UDP-forbindelse til den angivne vært og port.
- `FILE:<filename>`: Bruger en fil som input eller output.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `socat` kan bruges:

1. **Opret en TCP-forbindelse til en server:**
   ```bash
   socat -v - TCP:example.com:80
   ```

2. **Lyt på en port og videresend data til en anden server:**
   ```bash
   socat TCP-LISTEN:1234,fork TCP:example.com:80
   ```

3. **Opret en forbindelse til en lokal fil og send dens indhold til en TCP-server:**
   ```bash
   socat FILE:/path/to/file.txt,ro TCP:example.com:80
   ```

4. **Brug socat til at videresende UDP-pakker:**
   ```bash
   socat UDP-LISTEN:1234,fork UDP:example.com:5678
   ```

## Tips
- Brug `-d -v` mulighederne sammen for at få en detaljeret fejlfinding, når du arbejder med netværksforbindelser.
- Vær opmærksom på sikkerheden, når du lytter på porte; sørg for, at du kun tillader forbindelser fra betroede kilder.
- Test altid dine `socat`-kommandoer i et sikkert miljø, før du implementerer dem i produktion.