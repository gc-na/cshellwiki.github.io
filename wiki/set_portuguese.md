# [Linux] Bash set uso: Configurar opções do shell

## Overview
O comando `set` no Bash é utilizado para definir ou exibir variáveis de ambiente e opções do shell. Ele permite que os usuários ajustem o comportamento do shell, ativando ou desativando funcionalidades específicas.

## Usage
A sintaxe básica do comando `set` é a seguinte:

```bash
set [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `set`:

- `-e`: Faz com que o shell saia imediatamente se um comando retornar um status de erro.
- `-u`: Trata variáveis não definidas como um erro e sai do shell.
- `-x`: Exibe os comandos e seus argumentos à medida que são executados, útil para depuração.
- `-o`: Permite definir opções do shell, como `-o noclobber` para evitar sobrescrever arquivos.

## Common Examples

1. **Ativar a saída em caso de erro:**
   ```bash
   set -e
   ```

2. **Tratar variáveis não definidas como erro:**
   ```bash
   set -u
   ```

3. **Exibir comandos durante a execução:**
   ```bash
   set -x
   ```

4. **Combinar opções:**
   ```bash
   set -eu
   ```

5. **Definir uma opção do shell:**
   ```bash
   set -o noclobber
   ```

## Tips
- Use `set -e` em scripts para evitar que erros passem despercebidos.
- Combine opções como `-eu` para aumentar a robustez do seu script.
- Utilize `set -x` durante a depuração para entender melhor o fluxo do seu script.
- Lembre-se de que as opções definidas com `set` permanecem ativas até que sejam alteradas ou o shell seja encerrado.