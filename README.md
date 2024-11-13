# Kubernetes Deployment Producers gRPC

Este repositório contém arquivos de configuração YAML para o deployment e configuração dos serviços de um sistema distribuído de produtores de recursos usando gRPC em Go, que simula o fornecimento e consumo de itens como grãos, água, farinha e pão. Os manifestos incluem definições de `Deployment` e `Service` para cada microserviço, organizados para fácil aplicação e gerenciamento no cluster Kubernetes.

## Estrutura dos Arquivos

- **deployments.yaml**: Contém todos os `Deployments` dos microserviços, incluindo o número de réplicas e as imagens Docker correspondentes.
- **services.yaml**: Contém todos os `Services` dos microserviços, permitindo a comunicação entre eles dentro do cluster.

## Pré-requisitos

- Cluster Kubernetes ativo (local ou em nuvem).
    Você pode utilizar o projeto [kubebox](https://github.com/thiagogmta/kubebox) para implantar um cluster localmente.

## Aplicação dos Manifestos

1. Clone este repositório:

    ```bash
    git clone https://github.com/thiagogmta/k8s-deployment-producers-grpc.git
    cd k8s-deployment-manifests
    ```

2. Aplique o arquivo de Deployments:

    ```bash
    kubectl apply -f deployments.yaml
    ```

3. Aplique o arquivo de Services:

    ```bash
    kubectl apply -f services.yaml
    ```

4. Verifique se todos os Pods estão em execução:

    ```bash
    kubectl get pods
    ```

5. Verifique se os Services foram criados:

    ```bash
    kubectl get services
    ```