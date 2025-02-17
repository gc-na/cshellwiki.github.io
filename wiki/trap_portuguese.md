# [Linux] Bash trap uso: Captura de sinais e execução de comandos

## Overview
O comando `trap` no Bash é utilizado para capturar sinais e eventos, permitindo que você execute comandos específicos quando esses sinais são recebidos. Isso é útil para gerenciar a finalização de scripts, limpar recursos ou lidar com interrupções.

## Usage
A sintaxe básica do comando `trap` é a seguinte:

```bash
trap [comando] [sinal]
```

Onde `[comando]` é o comando que você deseja executar e `[sinal]` é o sinal que você deseja capturar.

## Common Options
Aqui estão algumas opções comuns que você pode usar com o comando `trap`:

- `SIGINT`: Captura a interrupção gerada pelo Ctrl+C.
- `SIGTERM`: Captura o sinal de término, que é enviado para solicitar a finalização de um processo.
- `EXIT`: Executa um comando quando o script termina, independentemente do motivo.

## Common Examples

### Exemplo 1: Capturando SIGINT
Este exemplo mostra como capturar a interrupção do Ctrl+C e executar um comando de limpeza.

```bash
trap 'echo "Script interrompido"; exit' SIGINT
while true; do
    echo "Executando..."
    sleep 1
done
```

### Exemplo 2: Limpeza ao sair
Neste exemplo, um comando de limpeza é executado quando o script termina.

```bash
trap 'echo "Limpando recursos..."; rm -f temp.txt' EXIT
touch temp.txt
echo "Fazendo algo com temp.txt"
```

### Exemplo 3: Capturando SIGTERM
Aqui, o script captura o sinal de término e executa um comando antes de sair.

```bash
trap 'echo "Recebido SIGTERM, saindo..."; exit' SIGTERM
while true; do
    echo "Aguardando sinal de término..."
    sleep 2
done
```

## Tips
- Sempre use `trap` para garantir que seus scripts limpem recursos, especialmente ao lidar com arquivos temporários.
- Teste seu script com diferentes sinais para garantir que o comportamento desejado ocorra em todas as situações.
- Lembre-se de que o `trap` pode ser usado para capturar múltiplos sinais, basta separá-los com espaços.

Utilizando o comando `trap`, você pode tornar seus scripts mais robustos e responsivos a eventos inesperados.