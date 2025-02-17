# [Linux] Bash wait gebruik: Wacht op achtergrondprocessen

## Overzicht
De `wait` opdracht in Bash wordt gebruikt om te wachten op de voltooiing van achtergrondprocessen. Het is handig wanneer je wilt dat een script of een reeks opdrachten pas verder gaat nadat bepaalde processen zijn afgerond.

## Gebruik
De basis syntaxis van de `wait` opdracht is als volgt:

```bash
wait [options] [arguments]
```

## Veelvoorkomende opties
- `-n`: Wacht op de voltooiing van de eerstvolgende achtergrondtaak.
- `PID`: Geef een specifieke proces-ID op om op te wachten.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Wachten op alle achtergrondprocessen
```bash
sleep 5 &
sleep 10 &
wait
echo "Alle achtergrondprocessen zijn voltooid."
```
In dit voorbeeld worden twee `sleep` opdrachten op de achtergrond uitgevoerd. Het script wacht totdat beide zijn voltooid voordat het verder gaat.

### Voorbeeld 2: Wachten op een specifieke achtergrondtaak
```bash
sleep 5 &
PID=$!
echo "Wacht op proces met PID $PID"
wait $PID
echo "Proces $PID is voltooid."
```
Hier wordt de PID van de achtergrond `sleep` taak opgeslagen en het script wacht specifiek op die taak.

### Voorbeeld 3: Wachten op de eerstvolgende achtergrondtaak
```bash
sleep 3 &
sleep 5 &
wait -n
echo "Eerste achtergrondtaak is voltooid."
```
In dit geval wacht het script op de eerstvolgende achtergrondtaak die is voltooid, ongeacht welke dat is.

## Tips
- Gebruik `wait` aan het einde van een script om ervoor te zorgen dat alle achtergrondprocessen zijn afgerond voordat het script eindigt.
- Houd rekening met de PID's van processen als je met meerdere achtergrondprocessen werkt, zodat je gerichter kunt wachten.
- Combineer `wait` met andere commando's in een script om de controle over de uitvoering van taken te verbeteren.