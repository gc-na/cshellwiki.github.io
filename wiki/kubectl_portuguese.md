# [Linux] Bash kubectl Uso: Gerenciar clusters Kubernetes

## Overview
O comando `kubectl` é a ferramenta de linha de comando para interagir com clusters Kubernetes. Ele permite que os usuários executem comandos para implantar aplicações, inspecionar e gerenciar recursos, além de visualizar logs e executar outras operações de gerenciamento.

## Usage
A sintaxe básica do comando `kubectl` é a seguinte:

```bash
kubectl [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `kubectl`:

- `get`: Recupera informações sobre recursos.
- `apply`: Aplica alterações a recursos a partir de um arquivo de configuração.
- `delete`: Remove recursos do cluster.
- `describe`: Fornece detalhes sobre um recurso específico.
- `logs`: Exibe logs de um pod específico.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `kubectl`:

### Listar todos os pods em um namespace
```bash
kubectl get pods -n meu-namespace
```

### Aplicar uma configuração a partir de um arquivo YAML
```bash
kubectl apply -f minha-configuracao.yaml
```

### Deletar um pod específico
```bash
kubectl delete pod meu-pod
```

### Descrever um serviço
```bash
kubectl describe service meu-servico
```

### Visualizar logs de um pod
```bash
kubectl logs meu-pod
```

## Tips
- Sempre verifique o namespace atual com `kubectl config view --minify | grep namespace` para garantir que você está operando no contexto correto.
- Utilize `kubectl get all` para obter uma visão geral de todos os recursos em um namespace.
- Para facilitar o uso, considere criar aliases no seu shell para comandos `kubectl` mais comuns.