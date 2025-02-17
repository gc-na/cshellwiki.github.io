# [Linux] Bash pr: Formatere tekstfiler for utskrift

## Oversikt
`pr`-kommandoen brukes til å formatere tekstfiler for utskrift. Den kan organisere innholdet i filer slik at det blir lettere å lese, spesielt når man skriver ut flere sider.

## Bruk
Den grunnleggende syntaksen for `pr`-kommandoen er som følger:

```bash
pr [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h`: Angi en tilpasset overskrift for utskriften.
- `-l`: Angi antall linjer per side.
- `-t`: Skriv ut uten overskrifter og fotnoter.
- `-s`: Angi et spesifikt mellomrom mellom kolonnene.
- `-w`: Angi bredden på utskriftsområdet.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `pr`-kommandoen:

1. **Formatere en fil for utskrift med standardinnstillinger:**
   ```bash
   pr fil.txt
   ```

2. **Angi en tilpasset overskrift:**
   ```bash
   pr -h "Min tilpassede overskrift" fil.txt
   ```

3. **Endre antall linjer per side til 50:**
   ```bash
   pr -l 50 fil.txt
   ```

4. **Skrive ut uten overskrifter og fotnoter:**
   ```bash
   pr -t fil.txt
   ```

5. **Formatere flere filer side om side:**
   ```bash
   pr fil1.txt fil2.txt
   ```

## Tips
- Når du bruker `pr`, kan det være nyttig å kombinere det med `less` eller `more` for å se på utskriften i terminalen før du skriver ut.
- Eksperimenter med forskjellige alternativer for å finne den beste formateringen for dine behov.
- Husk at `pr` er spesielt nyttig når du arbeider med lange tekstfiler som trenger å bli delt opp i håndterbare seksjoner for utskrift.