# [Linux] Bash traceroute6 Uso: Rastrear o caminho de pacotes IPv6

## Overview
O comando `traceroute6` é utilizado para rastrear o caminho que os pacotes IPv6 percorrem até um destino específico. Ele fornece informações sobre cada salto (hop) que o pacote faz, permitindo que os usuários identifiquem possíveis problemas de conectividade na rede.

## Usage
A sintaxe básica do comando `traceroute6` é a seguinte:

```bash
traceroute6 [opções] [destino]
```

## Common Options
Aqui estão algumas opções comuns do `traceroute6`:

- `-m <n>`: Define o número máximo de saltos (hops) que o comando deve seguir.
- `-p <n>`: Especifica a porta de destino a ser usada.
- `-w <n>`: Define o tempo de espera em segundos para cada resposta.
- `-q <n>`: Define o número de consultas por salto.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `traceroute6`:

1. Rastrear o caminho para um endereço IPv6 específico:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Definir o número máximo de saltos para 15:
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. Especificar uma porta de destino, por exemplo, a porta 80:
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

4. Aumentar o tempo de espera para 3 segundos:
   ```bash
   traceroute6 -w 3 2001:db8::1
   ```

5. Realizar múltiplas consultas por salto, por exemplo, 5 consultas:
   ```bash
   traceroute6 -q 5 2001:db8::1
   ```

## Tips
- Sempre verifique se o endereço IPv6 de destino está correto para evitar resultados inesperados.
- Use a opção `-m` para limitar o número de saltos, especialmente em redes grandes, para evitar longas esperas.
- Combine várias opções para obter resultados mais precisos e relevantes para suas necessidades de diagnóstico de rede.