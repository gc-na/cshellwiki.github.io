# [Linux] Bash rmdir Uso: Remove diretórios vazios

## Overview
O comando `rmdir` é utilizado para remover diretórios vazios no sistema de arquivos. Se o diretório contiver arquivos ou outros diretórios, o comando falhará e não realizará a remoção.

## Usage
A sintaxe básica do comando `rmdir` é a seguinte:

```bash
rmdir [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `rmdir`:

- `--ignore-fail-on-non-empty`: Ignora erros se o diretório não estiver vazio.
- `--verbose`: Exibe uma mensagem para cada diretório removido.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `rmdir`:

1. **Remover um diretório vazio:**
   ```bash
   rmdir meu_diretorio
   ```

2. **Remover vários diretórios vazios de uma só vez:**
   ```bash
   rmdir dir1 dir2 dir3
   ```

3. **Usar a opção verbose para ver o que está sendo removido:**
   ```bash
   rmdir --verbose meu_diretorio
   ```

4. **Ignorar erros ao tentar remover um diretório não vazio:**
   ```bash
   rmdir --ignore-fail-on-non-empty meu_diretorio
   ```

## Tips
- Sempre verifique se o diretório está realmente vazio antes de usar o `rmdir`, para evitar erros.
- Use a opção `--verbose` se você quiser confirmar quais diretórios foram removidos.
- Para remover diretórios que contêm arquivos ou subdiretórios, considere usar o comando `rm -r` em vez de `rmdir`.