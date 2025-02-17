# [Linux] Bash exec uso equivalente: Executar comandos substituindo o shell atual

## Overview
O comando `exec` no Bash é utilizado para substituir o processo do shell atual por um novo comando. Isso significa que, ao usar `exec`, o shell atual não retornará após a execução do comando especificado, pois ele é substituído pelo novo processo.

## Usage
A sintaxe básica do comando `exec` é a seguinte:

```bash
exec [opções] [comando]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `exec`:

- `-a nome`: Permite especificar um nome diferente para o comando executado.
- `-l`: Inicia o novo comando como um shell de login.
- `-c`: Ignora o ambiente atual e inicia o comando com um ambiente limpo.

## Common Examples

### Substituir o shell atual por um novo comando
```bash
exec ls -l
```
Neste exemplo, o comando `ls -l` será executado e o shell atual será substituído por ele. Após a execução, não haverá retorno ao shell.

### Executar um script com exec
```bash
exec ./meu_script.sh
```
Aqui, o script `meu_script.sh` será executado, substituindo o shell atual.

### Usar exec com um nome diferente
```bash
exec -a novo_nome /bin/bash
```
Esse comando inicia uma nova instância do Bash com o nome `novo_nome`.

### Limpar o ambiente antes de executar um comando
```bash
exec -c /usr/bin/env
```
Este exemplo executa o comando `env` em um ambiente limpo, sem variáveis de ambiente do shell atual.

## Tips
- Use `exec` quando você não precisar mais do shell atual e quiser economizar recursos do sistema.
- Lembre-se de que após a execução de um comando com `exec`, você não retornará ao shell anterior.
- Teste comandos em um terminal separado antes de usar `exec` para evitar perder o acesso ao shell.