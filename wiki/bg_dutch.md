# [Linux] C Shell (csh) bg gebruik: Voortzetten van een op de achtergrond uitgevoerd proces

## Overzicht
De `bg`-opdracht in C Shell (csh) wordt gebruikt om een gestopte taak of proces opnieuw op de achtergrond te starten. Dit is handig wanneer je een proces wilt laten draaien zonder dat het de controle over de terminal overneemt.

## Gebruik
De basis syntaxis van de `bg`-opdracht is als volgt:

```csh
bg [opties] [argumenten]
```

## Veelvoorkomende opties
- `job_spec`: Dit is de specificatie van de taak die je wilt hervatten. Dit kan een jobnummer of een proces-ID zijn.
- `&`: Hiermee kun je een opdracht in de achtergrond starten, maar dit is niet specifiek voor `bg`.

## Veelvoorkomende voorbeelden

1. **Een gestopte taak hervatten**:
   Stel dat je een taak hebt gestopt met `Ctrl+Z`, je kunt deze hervatten met:
   ```csh
   bg
   ```

2. **Een specifieke taak hervatten**:
   Als je meerdere taken hebt en je wilt een specifieke taak hervatten, gebruik je het jobnummer:
   ```csh
   bg %1
   ```

3. **Een taak in de achtergrond starten**:
   Je kunt ook een nieuwe taak in de achtergrond starten met:
   ```csh
   myscript.sh &
   ```

## Tips
- Gebruik `jobs` om een lijst van je huidige taken te bekijken. Dit helpt je bij het identificeren van de jobnummers die je met `bg` kunt gebruiken.
- Vergeet niet dat processen die in de achtergrond draaien, mogelijk output naar de terminal sturen. Dit kan verwarrend zijn, dus overweeg om de output naar een bestand te leiden.
- Als je een taak wilt stoppen, gebruik dan `fg` om deze naar de voorgrond te brengen en vervolgens `Ctrl+Z` om het te stoppen.