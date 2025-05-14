# Containers e Kubernetes

### 📦 **Containers** – O que são?

Um **container** é uma **unidade leve e portátil de software** que **empacota código, dependências, bibliotecas e configurações** em um único pacote executável.\
Isso garante que o software rode **de forma idêntica** em qualquer ambiente, seja local ou em produção.

***

#### ✅ Características dos containers:

* Compartilham o **kernel do sistema operacional**, mas isolam processos.
* São **mais leves que VMs** (máquinas virtuais).
* Iniciam e escalam rapidamente.
* Imagem = modelo do container (ex: `imagem do serviço de pedidos`)
* Container = instância em execução da imagem.

***

#### 🐳 Ferramenta mais comum: **Docker**

* Criação de imagens: `Dockerfile`
* Executar: `docker run`
* Gerenciar: `docker-compose.yml` (multi-contêiner)



### ☸️ **Kubernetes** – O que é?

**Kubernetes** (ou **K8s**) é uma **plataforma de orquestração de containers** criada pela Google.\
Ele automatiza o **deploy, escalonamento, balanceamento de carga, monitoramento e resiliência** de aplicações baseadas em containers.

***

#### 🧠 Conceitos principais:

| Conceito       | Descrição                                                                |
| -------------- | ------------------------------------------------------------------------ |
| **Pod**        | A menor unidade do K8s, geralmente contém 1 container (ou mais).         |
| **Service**    | Um ponto de acesso para os pods — expõe portas e IP fixo.                |
| **Deployment** | Define como criar e atualizar réplicas de pods.                          |
| **ReplicaSet** | Garante que haja sempre X instâncias rodando.                            |
| **Ingress**    | Recurso de entrada com regras para acesso HTTP (ex: roteamento de URLs). |
| **Namespace**  | Isola recursos dentro do cluster (útil por ambiente/projeto).            |
| **Cluster**    | Conjunto de máquinas (nós) gerenciado pelo K8s.                          |

***

#### 🔁 Fluxo simplificado:

1. Você **empacota seu app** em uma imagem Docker.
2. Sobe para um **registry** (ex: Docker Hub, Azure Container Registry).
3. Cria arquivos `.yaml` para definir **pods, services, deployments** etc.
4. Usa o `kubectl apply` para subir ao cluster.
5. Kubernetes **orquestra tudo automaticamente**.
