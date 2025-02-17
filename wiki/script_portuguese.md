# [Linux] Bash script uso: Gravar sessões de terminal

## Overview
O comando `script` é utilizado para gravar uma sessão de terminal em um arquivo. Isso permite que você capture tudo o que foi exibido na tela, incluindo entradas de comando e saídas, facilitando a documentação e a análise posterior.

## Usage
A sintaxe básica do comando `script` é a seguinte:

```bash
script [opções] [arquivo]
```

## Common Options
- `-a`: Anexa a saída ao arquivo existente, em vez de sobrescrevê-lo.
- `-c <comando>`: Executa um comando específico e grava a saída no arquivo.
- `-f`: Força a gravação em tempo real, exibindo a saída imediatamente.
- `-q`: Executa o comando em modo silencioso, sem exibir mensagens de início e término.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `script`:

### Exemplo 1: Gravar uma sessão padrão
```bash
script sessao.txt
```
Este comando inicia uma nova sessão de terminal e grava tudo em `sessao.txt`. Para encerrar a gravação, basta digitar `exit`.

### Exemplo 2: Anexar a um arquivo existente
```bash
script -a sessao_anexa.txt
```
Com este comando, você pode anexar novas entradas e saídas a `sessao_anexa.txt` sem perder o conteúdo anterior.

### Exemplo 3: Gravar a saída de um comando específico
```bash
script -c "ls -l" lista.txt
```
Este comando executa `ls -l` e grava a saída diretamente em `lista.txt`.

### Exemplo 4: Gravação em tempo real
```bash
script -f sessao_tempo_real.txt
```
Usando a opção `-f`, você grava a sessão em `sessao_tempo_real.txt` e vê as saídas imediatamente.

### Exemplo 5: Modo silencioso
```bash
script -q sessao_silenciosa.txt
```
Este comando grava a sessão em `sessao_silenciosa.txt` sem exibir mensagens de início e término.

## Tips
- Sempre verifique o conteúdo do arquivo gravado após a sessão para garantir que tudo foi registrado corretamente.
- Utilize a opção `-a` se você precisar gravar várias sessões em um único arquivo, evitando a perda de dados.
- Considere usar `script` em conjunto com outros comandos para documentar processos complexos ou tutoriais.