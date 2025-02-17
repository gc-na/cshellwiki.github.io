# [Linux] Bash dpkg Brug: Håndtering af Debian-pakker

## Oversigt
`dpkg` er et lavniveau værktøj til håndtering af Debian-pakker. Det bruges til at installere, fjerne og administrere pakker på Debian-baserede systemer som Ubuntu.

## Brug
Den grundlæggende syntaks for `dpkg`-kommandoen er:

```bash
dpkg [muligheder] [argumenter]
```

## Almindelige muligheder
- `-i`, `--install`: Installerer en pakke.
- `-r`, `--remove`: Fjerner en installeret pakke.
- `-l`, `--list`: Viser en liste over installerede pakker.
- `-s`, `--status`: Viser status for en specifik pakke.
- `-P`, `--purge`: Fjerner en pakke og dens konfigurationsfiler.

## Almindelige eksempler
- **Installere en pakke:**
  ```bash
  sudo dpkg -i pakke-navn.deb
  ```

- **Fjerne en pakke:**
  ```bash
  sudo dpkg -r pakke-navn
  ```

- **Liste installerede pakker:**
  ```bash
  dpkg -l
  ```

- **Tjekke status for en pakke:**
  ```bash
  dpkg -s pakke-navn
  ```

- **Fjerne en pakke og dens konfigurationsfiler:**
  ```bash
  sudo dpkg -P pakke-navn
  ```

## Tips
- Brug `dpkg` sammen med `apt-get` for at løse afhængigheder, da `dpkg` ikke automatisk håndterer dem.
- Sørg for at have de nødvendige rettigheder (brug `sudo`), når du installerer eller fjerner pakker.
- Tjek altid status for en pakke efter installation eller fjernelse for at sikre, at operationen blev udført korrekt.