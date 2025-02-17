# [Linux] Bash umask brug: Angiver standard tilladelser for nye filer og mapper

## Oversigt
`umask`-kommandoen bruges til at angive standard tilladelser for nye filer og mapper, der oprettes i et Unix-lignende operativsystem. Den bestemmer, hvilke tilladelser der skal fjernes fra de standardtilladelser, der normalt tildeles af systemet.

## Brug
Den grundlæggende syntaks for `umask`-kommandoen er som følger:

```bash
umask [indstillinger] [argumenter]
```

## Almindelige indstillinger
- `-S`: Viser umask-værdien i symbolsk form.
- `-p`: Viser den aktuelle umask-værdi i et format, der kan bruges til at indstille umask igen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `umask` kan bruges:

1. **Vis den nuværende umask-værdi:**
   ```bash
   umask
   ```

2. **Indstil umask til 027:**
   Dette vil fjerne skrive- og udførelsestilladelser for gruppe og andre.
   ```bash
   umask 027
   ```

3. **Vis umask i symbolsk form:**
   ```bash
   umask -S
   ```

4. **Indstil umask til 007:**
   Dette vil fjerne alle tilladelser for andre.
   ```bash
   umask 007
   ```

## Tips
- Det er en god praksis at kontrollere din umask-værdi, før du opretter nye filer, for at sikre, at de har de ønskede tilladelser.
- Overvej at sætte umask-værdien i din shell-konfigurationsfil (f.eks. `.bashrc`), så den anvendes automatisk ved hver opstart af terminalen.
- Vær opmærksom på, at umask-værdien kun påvirker nye filer og mapper, ikke eksisterende.