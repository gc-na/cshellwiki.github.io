# [Linux] Bash tee Uso: Redireciona a saída para arquivos e para a tela

## Overview
O comando `tee` no Bash é utilizado para ler da entrada padrão e gravar tanto na saída padrão (geralmente a tela) quanto em um ou mais arquivos. Isso permite que você visualize a saída de um comando enquanto também a salva em um arquivo.

## Usage
A sintaxe básica do comando `tee` é a seguinte:

```bash
tee [opções] [arquivos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `tee`:

- `-a`, `--append`: Anexa a saída ao final do arquivo em vez de sobrescrevê-lo.
- `-i`, `--ignore-interrupts`: Ignora sinais de interrupção.
- `-p`, `--output-error`: Controla como os erros de saída são tratados.

## Common Examples

### Exemplo 1: Redirecionar a saída de um comando para um arquivo
```bash
echo "Olá, mundo!" | tee arquivo.txt
```
Esse comando grava "Olá, mundo!" no arquivo `arquivo.txt` e também exibe a mensagem na tela.

### Exemplo 2: Anexar a saída a um arquivo existente
```bash
echo "Outra linha" | tee -a arquivo.txt
```
Aqui, "Outra linha" é adicionada ao final de `arquivo.txt`, mantendo o conteúdo anterior.

### Exemplo 3: Usar com múltiplos arquivos
```bash
echo "Salvando em múltiplos arquivos" | tee arquivo1.txt arquivo2.txt
```
Esse comando grava a saída em `arquivo1.txt` e `arquivo2.txt`, além de exibi-la na tela.

### Exemplo 4: Ignorar interrupções
```bash
cat arquivo.txt | tee -i arquivo_copia.txt
```
Neste exemplo, o comando `cat` lê `arquivo.txt` e `tee` grava a saída em `arquivo_copia.txt`, ignorando interrupções.

## Tips
- Utilize a opção `-a` se precisar adicionar informações a um arquivo existente sem perder os dados anteriores.
- Combine `tee` com outros comandos usando pipes para capturar saídas intermediárias.
- Lembre-se de que `tee` pode ser útil em scripts para registrar logs enquanto ainda exibe informações ao usuário.