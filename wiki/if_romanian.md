# [Linux] C Shell (csh) if: Evaluare condițională

## Overview
Comanda `if` în C Shell (csh) este utilizată pentru a evalua condiții și a executa comenzi în funcție de rezultatul acestei evaluări. Aceasta permite scripturilor să ia decizii bazate pe condiții specifice.

## Usage
Sintaxa de bază a comenzii `if` este următoarea:

```csh
if (condiție) then
    comenzi
endif
```

## Common Options
- `then`: Indică începutul blocului de comenzi care se va executa dacă condiția este adevărată.
- `endif`: Marchează sfârșitul blocului `if`.
- `else`: Permite specificarea unui bloc alternativ de comenzi care se va executa dacă condiția este falsă.

## Common Examples

### Exemplul 1: Verificarea existenței unui fișier
```csh
if (-e "fisier.txt") then
    echo "Fișierul există."
endif
```

### Exemplul 2: Compararea numerelor
```csh
set numar = 10
if ($numar > 5) then
    echo "Numărul este mai mare decât 5."
endif
```

### Exemplul 3: Utilizarea unui bloc else
```csh
if (-d "folder") then
    echo "Folderul există."
else
    echo "Folderul nu există."
endif
```

### Exemplul 4: Verificarea unui argument de linie de comandă
```csh
if ($#argv == 0) then
    echo "Te rog să introduci un argument."
else
    echo "Argumentul introdus este: $argv[1]"
endif
```

## Tips
- Asigură-te că utilizezi parantezele corecte pentru condiții.
- Folosește blocuri `else` pentru a gestiona cazurile alternative.
- Testează întotdeauna scripturile tale pentru a verifica dacă condițiile sunt evaluate corect.