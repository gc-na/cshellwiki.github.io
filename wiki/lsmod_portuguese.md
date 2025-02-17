# [Linux] Bash lsmod Uso: Exibir módulos do kernel carregados

## Overview
O comando `lsmod` é utilizado para listar os módulos do kernel que estão atualmente carregados no sistema Linux. Ele fornece informações sobre os módulos, como seu nome, tamanho e dependências, permitindo que os usuários verifiquem quais drivers e funcionalidades estão ativos no momento.

## Usage
A sintaxe básica do comando `lsmod` é a seguinte:

```bash
lsmod [opções] [argumentos]
```

## Common Options
O comando `lsmod` não possui muitas opções, mas aqui estão algumas que podem ser úteis:

- `-h`, `--help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.
- `-v`, `--version`: Mostra a versão do comando `lsmod`.

## Common Examples

1. **Listar todos os módulos carregados:**
   ```bash
   lsmod
   ```

2. **Exibir ajuda sobre o comando:**
   ```bash
   lsmod --help
   ```

3. **Ver a versão do comando:**
   ```bash
   lsmod --version
   ```

## Tips
- Utilize o comando `lsmod` em conjunto com `modinfo` para obter mais detalhes sobre um módulo específico.
- Para verificar se um módulo específico está carregado, você pode usar `grep` junto com `lsmod`. Por exemplo:
  ```bash
  lsmod | grep nome_do_modulo
  ```
- Lembre-se de que a saída do `lsmod` pode ser útil para solucionar problemas de hardware, pois ajuda a identificar se os drivers necessários estão ativos.