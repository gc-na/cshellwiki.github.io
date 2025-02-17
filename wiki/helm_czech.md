# [Linux] Bash helm použití: Správa Kubernetes aplikací

## Přehled
Příkaz `helm` slouží k správě aplikací v Kubernetes prostředí. Je to nástroj pro správu balíčků, který usnadňuje instalaci, aktualizaci a odstraňování aplikací v Kubernetes pomocí tzv. "chartů".

## Použití
Základní syntaxe příkazu `helm` je následující:

```bash
helm [možnosti] [argumenty]
```

## Běžné možnosti
- `install`: Nainstaluje nový chart.
- `upgrade`: Aktualizuje existující release.
- `uninstall`: Odstraní release.
- `list`: Zobrazí seznam nainstalovaných release.
- `repo`: Spravuje Helm repozitáře.

## Běžné příklady
1. **Instalace nového chartu:**
   ```bash
   helm install my-release stable/mysql
   ```

2. **Aktualizace existujícího release:**
   ```bash
   helm upgrade my-release stable/mysql
   ```

3. **Odstranění release:**
   ```bash
   helm uninstall my-release
   ```

4. **Zobrazení seznamu nainstalovaných release:**
   ```bash
   helm list
   ```

5. **Přidání nového repozitáře:**
   ```bash
   helm repo add stable https://charts.helm.sh/stable
   ```

## Tipy
- Před instalací nového chartu si vždy zkontrolujte dostupné verze pomocí `helm search repo`.
- Používejte `--dry-run` možnost při instalaci nebo aktualizaci, abyste viděli, co se stane, aniž byste provedli skutečné změny.
- Udržujte své Helm repozitáře aktuální pomocí `helm repo update`, abyste měli přístup k nejnovějším chartům.