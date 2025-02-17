# [Linux] Bash sed användning: Textbearbetning med strömmande redigering

## Översikt
`sed` (stream editor) är ett kraftfullt verktyg i Bash som används för att bearbeta och redigera textströmmar. Det kan utföra en mängd olika textmanipulationer, inklusive sökning, ersättning och borttagning av text.

## Användning
Den grundläggande syntaxen för `sed` är:

```bash
sed [alternativ] [argument]
```

## Vanliga alternativ
- `-e`: Anger ett skript för att utföra flera redigeringar.
- `-i`: Gör ändringar direkt i filen (in-place).
- `-n`: Tystar ut standardutmatningen, vilket gör att endast specifika rader skrivs ut.
- `s/pattern/replacement/`: Ersätter mönstret med ersättningen.

## Vanliga exempel
### Ersätta text i en fil
För att ersätta alla förekomster av "hund" med "katt" i en fil:

```bash
sed -i 's/hund/katt/g' fil.txt
```

### Visa specifika rader
För att visa endast rad 2 till 4 i en fil:

```bash
sed -n '2,4p' fil.txt
```

### Ta bort tomma rader
För att ta bort alla tomma rader från en fil:

```bash
sed -i '/^$/d' fil.txt
```

### Ersätta text i en ström
För att ersätta "äpple" med "banan" i en textström:

```bash
echo "Jag gillar äpple" | sed 's/äpple/banan/'
```

## Tips
- Använd `-i.bak` med `-i` för att skapa en säkerhetskopia av filen innan ändringar görs.
- Testa alltid dina `sed`-kommandon utan `-i` först för att se resultatet innan du gör permanenta ändringar.
- Använd `-n` tillsammans med `p` för att få mer kontroll över vad som skrivs ut.