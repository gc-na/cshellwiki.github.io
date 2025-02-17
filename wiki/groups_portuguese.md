# [Linux] Bash groups uso: Exibe os grupos de um usuário

## Overview
O comando `groups` é utilizado no Bash para exibir os grupos aos quais um usuário pertence. Ele pode ser usado para verificar rapidamente as permissões e a associação de grupos de um usuário específico ou do usuário atual.

## Usage
A sintaxe básica do comando `groups` é a seguinte:

```bash
groups [opções] [argumentos]
```

## Common Options
- `-h`, `--help`: Exibe uma mensagem de ajuda com informações sobre o comando.
- `-v`, `--version`: Mostra a versão do comando `groups`.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `groups`:

1. **Exibir grupos do usuário atual:**
   ```bash
   groups
   ```

2. **Exibir grupos de um usuário específico:**
   ```bash
   groups nome_do_usuario
   ```

3. **Usar com opções de ajuda:**
   ```bash
   groups --help
   ```

4. **Ver a versão do comando:**
   ```bash
   groups --version
   ```

## Tips
- Utilize o comando `groups` sem argumentos para verificar rapidamente os grupos do usuário que está logado.
- Para verificar os grupos de outro usuário, você deve ter permissões adequadas, caso contrário, o comando pode não retornar as informações desejadas.
- Combine o comando `groups` com outros comandos, como `grep`, para filtrar informações específicas sobre grupos.