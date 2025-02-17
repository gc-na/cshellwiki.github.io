# [Linux] Bash vipw Uso: Editar arquivos de senhas de forma segura

## Overview
O comando `vipw` é utilizado para editar de forma segura o arquivo de senhas do sistema, geralmente localizado em `/etc/passwd` e `/etc/shadow`. Ele garante que o arquivo não seja corrompido durante a edição, bloqueando o acesso a outros processos enquanto o arquivo está sendo modificado.

## Usage
A sintaxe básica do comando `vipw` é a seguinte:

```bash
vipw [opções]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `vipw`:

- `-s`: Edita o arquivo de senhas seguro (`/etc/shadow`) em vez do arquivo de senhas padrão.
- `-h`: Mostra a ajuda sobre o uso do comando.

## Common Examples

### Editar o arquivo de senhas padrão
Para editar o arquivo de senhas padrão, você pode simplesmente executar:

```bash
vipw
```

### Editar o arquivo de senhas seguro
Se você precisar editar o arquivo de senhas seguro, use a opção `-s`:

```bash
vipw -s
```

### Exibir ajuda
Para ver as opções disponíveis e como usar o comando, você pode executar:

```bash
vipw -h
```

## Tips
- Sempre use `vipw` em vez de um editor de texto comum para editar arquivos de senhas, pois ele previne a corrupção do arquivo.
- Faça backup dos arquivos de senhas antes de realizar alterações significativas, para evitar perda de dados.
- Utilize um editor de texto que você esteja confortável, pois `vipw` abrirá o editor padrão configurado no sistema.