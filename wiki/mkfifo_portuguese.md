# [Linux] Bash mkfifo Uso: Criar um FIFO (First In, First Out)

## Overview
O comando `mkfifo` é utilizado para criar um arquivo FIFO (First In, First Out) no sistema de arquivos. Um FIFO é um tipo especial de arquivo que permite a comunicação entre processos, onde os dados escritos em um FIFO são lidos na ordem em que foram escritos.

## Usage
A sintaxe básica do comando `mkfifo` é a seguinte:

```bash
mkfifo [opções] [argumentos]
```

## Common Options
- `-m, --mode=MODE`: Define as permissões do arquivo FIFO a ser criado. O modo deve ser especificado em formato octal.
- `--help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.
- `--version`: Mostra a versão do comando `mkfifo`.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `mkfifo`:

### Criar um FIFO simples
```bash
mkfifo meu_fifo
```
Este comando cria um arquivo FIFO chamado `meu_fifo` no diretório atual.

### Criar um FIFO com permissões específicas
```bash
mkfifo -m 644 meu_fifo
```
Neste exemplo, o FIFO `meu_fifo` é criado com permissões de leitura e escrita para o proprietário e leitura para o grupo e outros.

### Usar um FIFO para comunicação entre processos
1. Em um terminal, execute:
   ```bash
   cat > meu_fifo
   ```
   Isso aguardará a entrada de dados.
   
2. Em outro terminal, execute:
   ```bash
   echo "Olá, FIFO!" > meu_fifo
   ```
   O primeiro terminal exibirá "Olá, FIFO!" assim que o comando acima for executado.

## Tips
- Sempre verifique as permissões do FIFO após a criação, especialmente se você estiver permitindo que outros usuários acessem o arquivo.
- Use `rm meu_fifo` para remover um FIFO quando não for mais necessário, assim como faria com um arquivo comum.
- Lembre-se de que o FIFO bloqueia a leitura até que haja dados disponíveis, então tenha cuidado ao projetar a lógica de comunicação entre processos.