# [Linux] Bash export uso equivalente: Definindo variáveis de ambiente

## Overview
O comando `export` no Bash é utilizado para definir variáveis de ambiente que podem ser acessadas por processos filhos. Isso é útil para configurar o ambiente de execução de programas e scripts.

## Usage
A sintaxe básica do comando `export` é a seguinte:

```bash
export [opções] [variável[=valor]]
```

## Common Options
- `-n`: Remove a variável do ambiente, ou seja, não a exporta mais.
- `-p`: Exibe todas as variáveis de ambiente exportadas.
- `-f`: Exporta funções em vez de variáveis.

## Common Examples

1. **Exportar uma variável simples:**
   ```bash
   export MY_VAR="Olá, Mundo!"
   ```

2. **Verificar a variável exportada:**
   ```bash
   echo $MY_VAR
   ```

3. **Exportar uma variável e usá-la em um novo shell:**
   ```bash
   export PATH="$PATH:/usr/local/bin"
   ```

4. **Remover uma variável do ambiente:**
   ```bash
   export -n MY_VAR
   ```

5. **Listar todas as variáveis exportadas:**
   ```bash
   export -p
   ```

## Tips
- Sempre que você definir uma variável que precisa ser acessada por scripts ou programas filhos, use `export`.
- Para evitar conflitos de nomes, é uma boa prática prefixar suas variáveis com um identificador único.
- Lembre-se de que as variáveis exportadas só estarão disponíveis para processos filhos iniciados após a exportação.