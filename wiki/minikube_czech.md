# [Linux] Bash minikube použití: Správa lokálních Kubernetes klastrů

## Přehled
Minikube je nástroj, který umožňuje snadno spouštět a spravovat lokální Kubernetes klastr. Je ideální pro vývoj a testování aplikací v prostředí Kubernetes bez potřeby přístupu k externímu cloudu.

## Použití
Základní syntaxe příkazu minikube je následující:

```
minikube [možnosti] [argumenty]
```

## Běžné možnosti
- `start`: Spustí nový Minikube klastr.
- `stop`: Zastaví běžící Minikube klastr.
- `delete`: Odstraní Minikube klastr.
- `status`: Zobrazí stav Minikube klastru.
- `kubectl`: Spustí kubectl příkazy v kontextu Minikube.

## Běžné příklady
1. **Spuštění nového klastru:**
   ```bash
   minikube start
   ```

2. **Zastavení běžícího klastru:**
   ```bash
   minikube stop
   ```

3. **Odstranění klastru:**
   ```bash
   minikube delete
   ```

4. **Zobrazení stavu klastru:**
   ```bash
   minikube status
   ```

5. **Spuštění kubectl příkazu:**
   ```bash
   minikube kubectl -- get pods -A
   ```

## Tipy
- Ujistěte se, že máte nainstalovány všechny potřebné závislosti, jako je VirtualBox nebo Docker, pro správnou funkčnost Minikube.
- Pravidelně aktualizujte Minikube na nejnovější verzi, abyste měli přístup k nejnovějším funkcím a opravám.
- Používejte příkaz `minikube dashboard` pro otevření webového rozhraní, které vám umožní vizuálně spravovat vaše Kubernetes zdroje.