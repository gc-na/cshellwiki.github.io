# [Linux] Bash kubectl použití: Správa Kubernetes klastrů

## Přehled
Příkaz `kubectl` je nástroj příkazového řádku pro interakci s Kubernetes klastrami. Umožňuje uživatelům spravovat a orchestraci aplikací běžících v kontejnerech, provádět nasazení, sledovat stav a provádět různé operace na zdrojích Kubernetes.

## Použití
Základní syntaxe příkazu `kubectl` je následující:

```bash
kubectl [možnosti] [argumenty]
```

## Běžné možnosti
- `get`: Získá seznam zdrojů (např. podů, služeb).
- `describe`: Zobrazí podrobnosti o konkrétním zdroji.
- `apply`: Aplikuje změny na zdroje podle specifikace v souboru.
- `delete`: Odstraní specifikované zdroje.
- `logs`: Zobrazí protokoly z podu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `kubectl`:

### Získání seznamu podů
```bash
kubectl get pods
```

### Získání podrobností o konkrétním podu
```bash
kubectl describe pod <název-podu>
```

### Aplikace změn ze souboru
```bash
kubectl apply -f <cesta-k-souboru>.yaml
```

### Odstranění podu
```bash
kubectl delete pod <název-podu>
```

### Zobrazení protokolů z podu
```bash
kubectl logs <název-podu>
```

## Tipy
- Vždy používejte `kubectl get` pro rychlé ověření stavu vašich zdrojů.
- Při práci s YAML soubory se ujistěte, že dodržujete správné odsazení, aby nedošlo k chybám při aplikaci.
- Používejte aliasy pro časté příkazy, aby se zjednodušila práce v příkazovém řádku. Například: `alias k=kubectl`.
- Nezapomeňte pravidelně kontrolovat verzi `kubectl` pomocí `kubectl version`, abyste zajistili kompatibilitu s vaším Kubernetes klastrem.