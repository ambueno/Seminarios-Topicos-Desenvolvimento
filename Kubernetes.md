<h1 align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com/?lines=Kubernetes;:)&center=true&size=35">
  </a>
</h1>

# Introdução
## O que é? 
Kubernetes (K8s) é um sistema open-source para automatizar a implantação (deployment),
o dimensionamento (scaling) e o gerenciamento de aplicativos em containers. De modo mais detalhado, é uma plataforma portátil,
extensível e de código aberto para gerenciar cargas de trabalho e serviços em contêineres, que facilita tanto a configuração 
declarativa quanto a automação.

## Como funciona? 
Se baseia no agrupamento de containers que compõem uma aplicação em unidades lógicas para 
facilitar o gerenciamento e a descoberta dos serviços.

## Contextualização histórica
- #### Era da implantação tradicional: 
No início, as organizações executavam aplicações em servidores físicos. Não havia como definir limites de recursos para aplicações em um mesmo servidor físico,
e isso causava problemas de alocação de recursos. Por exemplo, se várias aplicações fossem executadas em um mesmo servidor físico, poderia haver situações em
que uma aplicação ocupasse a maior parte dos recursos e, como resultado, o desempenho das outras aplicações seria inferior. Uma solução para isso seria executar
cada aplicação em um servidor físico diferente. Mas isso não escalava, pois os recursos eram subutilizados, e se tornava custoso para as organizações manter
muitos servidores físicos.

- #### Era da implantação virtualizada: 
Como solução, a virtualização foi introduzida. Esse modelo permite que você execute várias máquinas virtuais (VMs) em uma única CPU de um servidor físico. A virtualização permite que as aplicações sejam isoladas entre as VMs, e ainda fornece um nível de segurança, pois as informações de uma aplicação não podem ser acessadas livremente por outras aplicações. A virtualização permite melhor utilização de recursos em um servidor físico, e permite melhor escalabilidade porque uma aplicação pode ser adicionada ou atualizada facilmente, reduz os custos de hardware e muito mais. Com a virtualização, você pode apresentar um conjunto de recursos físicos como um cluster de máquinas virtuais descartáveis. Cada VM é uma máquina completa que executa todos os componentes, incluindo seu próprio sistema operacional, além do hardware virtualizado.

- #### Era da implantação em contêineres: 
Contêineres são semelhantes às VMs, mas têm propriedades de isolamento flexibilizados para compartilhar o sistema operacional (SO) entre as aplicações. Portanto, os contêineres são considerados leves. Semelhante a uma VM, um contêiner tem seu próprio sistema de arquivos, compartilhamento de CPU, memória, espaço de processo e muito mais. Como eles estão separados da infraestrutura subjacente, eles são portáveis entre nuvens e distribuições de sistema operacional.

## Recursos principais:

- **Empacotamento (Bin packing) automático:** organiza automaticamente os contêineres com base em seus requisitos de recursos e outras restrições,
sem sacrificar a disponibilidade. Combinando cargas de trabalho críticas e de melhor esforço para
aumentar a utilização e economizar ainda mais recursos. 
- **Gerenciamento de configurações e Secret:** o Kubernetes permite armazenar e gerenciar informações confidenciais, como senhas, tokens OAuth e chaves SSH. 
Você pode implantar e atualizar segredos e configuração de aplicativos sem reconstruir suas imagens de contêiner e
sem expor segredos em sua configuração de pilha.
- **Projetado para extensibilidade:** possibilita adicionar recursos ao seu cluster Kubernetes sem alterar o código-fonte anterior.
- **Orquestração de armazenamento:** monta automaticamente o sistema de armazenamento de sua escolha, seja de armazenamento local,
um provedor de nuvem pública, como AWS ou GCP, ou um sistema de armazenamento de rede, como NFS, iSCSI, Ceph, Cinder.
- **Descoberta de serviços e balanceamento de carga:** não há necessidade de modificar seu aplicativo para usar um mecanismo de descoberta de serviço desconhecido.
O Kubernetes fornece aos pods seus próprios endereços IP e um único nome DNS para um conjunto de pods e pode balancear a carga (load-balance) entre eles.
- **Autocura:** reinicia os contêineres que falham, substitui e reagenda contêineres quando os nós morrem,
elimina contêineres que não respondem à verificação de integridade definida pelo usuário e
não os anuncia aos clientes até que estejam prontos para serem utilizados.
- **Dimensionamento (scaling) horizontal:** dimensionamento da sua aplicação com um comando, com uma interface do usuário ou automaticamente com base no uso da CPU.
- **IPv4/IPv6 dual-stack:** alocação de endereços IPv4 e IPv6 para pods e serviços
- **Execução em lote:** além dos serviços, o Kubernetes pode gerenciar suas cargas de trabalho de lote e CI, substituindo contêineres que falham, se desejado.
- **Rollouts e rollbacks automatizados:** o Kubernetes lança progressivamente alterações em sua aplicação ou em sua configuração, enquanto monitora a integridade da aplicação para garantir que ele não mate todas as suas instâncias ao mesmo tempo. Se algo der errado, o Kubernetes reverterá a alteração para você.

## Conceitos fundamentais:
- **Cluster:** um conjunto de servidores de processamento, chamados nós, que executam aplicações containerizadas. Todo cluster possui ao menos um servidor de processamento (worker node);
- **Contêiner:** uma imagem executável leve e portável que contém software e todas as suas dependências;
- **Control Plane:** camada de orquestração de contêineres que expõe a API e as interfaces para definir, implantar e gerenciar o ciclo de vida dos contêineres;
- **Deployment:** um objeto de API que gerencia uma aplicação replicada, geralmente executando pods sem estado local;
- **Imagem:** instância armazenada de um contêiner que contém o conjunto de softwares necessários para rodar uma aplicação;
- **Kubectl:** ferramenta de linha de comando para se comunicar com a camada de gerenciamento de um cluster Kubernetes usando a API do Kubernetes;
- **Master:** sinônimo de nós que hospedam o plano de controle;
- **Node:** um Node ou Nó é uma máquina de trabalho no Kubernetes;
- **Pod:** o menor e mais simples objeto Kubernetes. Um Pod representa um conjunto de contêineres em execução no seu cluster.


## Instalação & Configuração

#### **1. Instalação de nó único:** Este tipo de instalação é adequado para quem deseja visualizar o Kubernetes ou é adequado para práticas, testes e fins de desenvolvimento. Existem muitas distribuições de Kubernetes de nó único no mercado, mas apresento as mais populares.

 - **Minikube**: é uma distribuição Kubernetes de nó único que é lançada oficialmente pela comunidade Kubernetes. A versão mais recente do Kubernetes pode ser executada com o minikube. Juntamente com a instalação do Kubernetes, alguns complementos do Kubernetes podem ser executados facilmente. Com o minikube, o Kubernetes pode ser implantado em sistemas VM, Container ou bare-metal. Vários ambientes de execução de contêiner (Docker, Containerd, CRI-O) também são suportados. Mais informações em https://minikube.sigs.k8s.io

  - **Kind**: é uma distribuição para executar o cluster Kubernetes dentro de contêineres do Docker em seu sistema local. kind significa “Kubernetes in Docker” Esta distribuição é adequada para testes, desenvolvimento local e sistemas de CI. kind é distribuído oficialmente pela comunidade Kubernetes. Mais informações em https://kind.sigs.k8s.io

  - **k3s**: é outra distribuição útil lançada pela Rancher. Ele foi desenvolvido inicialmente para IoT e computação de borda, mas pode ser usado para qualquer outra finalidade. Você pode executar um Kubernetes de nó único ou um cluster com alguns comandos. Mais informações em https://k3s.io

  - **k3d**: é um auxiliar para executar k3s no Docker. Ele lança um cluster Kubernetes em sua máquina local como “tipo”. k3d é lançado pela Rancher. Mais informações em https://github.com/rancher/k3d

  - **microk8s**: é outra opção de instalação. Não apenas um Kubernetes de nó único, mas um cluster também pode ser implantado usando microk8s. Esta distribuição do Kubernetes é lançada pela Canonical - a empresa que lança o Ubuntu - e está disponível no gerenciador de pacotes rápido. O Kubernetes pode ser implantado com alguns comandos. Juntamente com o Kubernetes, está disponível uma lista de vários complementos que podem ser implantados facilmente. Mais informações em https://microk8s.io

#### **2. Instalação manual do cluster:** Esse tipo de instalação é usado para implantar um cluster mínimo viável. Algumas partes da instalação devem ser feitas manualmente. É a maneira preferida de implantar o cluster Kubernetes pela primeira vez.

  - **Kubeadm**: é uma ferramenta que é usada para implantar um cluster por mãos humanas. Ele é usado para inicializar componentes do Kubernetes, não para provisionar máquinas. Antes de inicializar o cluster, algumas ações devem ser feitas manualmente. Mais informações em https://kubernetes.io/docs/reference/setup-tools/kubeadm

#### **3. Instalação automática do cluster:** Esse tipo de instalação é feito usando ferramentas de automação, scripts ou instaladores distribuídos pelo provedor. É uma maneira preferencial para aqueles que desejam implantar clusters Kubernetes de nível de produção em um ambiente local ou desejam gerenciar o ciclo de vida do cluster manualmente.

 - **Kubespray**: é uma coleção de playbooks Ansible que são usados para implantar clusters de nível de produção em bare-metal e na nuvem. Juntamente com a instalação, as operações do segundo dia podem ser realizadas com o kubespray. Este instalador é mantido oficialmente pela comunidade Kubernetes. Uma dúzia de complementos estão disponíveis no kubespray e podem ser implantados facilmente junto com o Kubernetes. kubespray é uma das opções de instalação mais adequadas. Mais informações em https://github.com/kubernetes-sigs/kubespray

  - **Kops**: não apenas gerenciará o ciclo de vida do cluster, mas também fornecerá a infraestrutura de nuvem necessária. A implantação na AWS é suportada oficialmente, a implantação em outros provedores de nuvem está disponível, mas em estado alfa e beta. Mais informações em https://kops.sigs.k8s.io

  - **RKE**: é um Kubernetes distribuído do Rancher que pode implantar clusters Kubernetes de nível de produção sobre contêineres do Docker. O gerenciamento de clusters do Kubernetes é feito facilmente com o RKE. Se você deseja usar a plataforma Rancher, deve selecionar esta distribuição. Mais informações em https://github.com/rancher/rke

  - **Charmed Kubernetes**: é a maneira canônica de implantar clusters Kubernetes com Juju. É adequado para executar o Kubernetes em ambientes multinuvem e bare-metal. Se você procura uma distribuição qualificada do Kubernetes que possa ser implantada no OpenStack, este instalador é para você. Mais informações em https://ubuntu.com/kubernetes

  - **KubeSphere**: não é apenas uma distribuição Kubernetes, é também uma plataforma para criar uma solução em nuvem baseada em Kubernetes. Um grande número de ferramentas, complementos etc. podem ser implantados usando o KubeSphere junto com o Kubernetes. Essa plataforma também pode ser implantada no cluster Kubernetes existente. Mais informações em https://kubesphere.io

  - **Kubermatic**: é uma plataforma Kubernetes assim como o Rancher. Você pode implantar e gerenciar clusters do Kubernetes em nuvens e no local. A conexão entre o cluster mestre/semente e os clusters downstream é tratada pelo OpenVPN. Mais informações em https://github.com/kubermatic/kubermatic

  - **KubeOne**: é uma ferramenta para provisionar a infraestrutura necessária e implantar o Kubernetes em alguns provedores. Ele pode ser facilmente integrado ao Terraform e Kubermatic. Mais informações em https://github.com/kubermatic/kubeone

#### **4. Clusters gerenciados:** O ciclo de vida dos clusters é gerenciado pelos provedores. Nesse tipo de instalação, um cluster de nível de produção pode ser implantado com ações mínimas do usuário. Os provedores são responsáveis por gerenciar todo o cluster, bem como a infraestrutura subjacente. Devido à facilidade de instalação e gerenciamento, este método é sugerido a qualquer pessoa. Outro benefício de usar o Kubernetes gerenciado é o acesso aos recursos da nuvem. Alguns provedores gerenciados do Kubernetes fornecem um conjunto de recursos úteis que podem não estar disponíveis em soluções locais ou bare-metal.

  - **Magnum**: é uma solução OpenStack para instalar Kubernetes gerenciados e outras ferramentas de orquestração no ecossistema OpenStack. Com o Magnum, os clientes da nuvem podem executar clusters do Kubernetes facilmente. Esse método também pode ser categorizado em Métodos de instalação automatizada de cluster. Decidi apresentá-lo aqui porque ele também suporta os incríveis recursos de nuvem. Além disso, os provedores de nuvem baseados em OpenStack podem fornecer esse método para seus clientes instalarem clusters Kubernetes gerenciados. Mais informações em https://docs.openstack.org/magnum/latest

  - **EKS**: significa Elastic Kubernetes Service é a solução da Amazon para fornecer cluster Kubernetes gerenciado. O EKS pode ser facilmente integrado a outros serviços da Amazon. Uma ferramenta de linha de comando, eksctl, é usada para executar um cluster Kubernetes de produção em alguns minutos. Mais informações em https://aws.amazon.com/eks

  - **GKE**: é uma versão do Kubernetes do Google Cloud, assim como o AWS EKS. O GKE oferece um modo de operação especial chamado Autopilot, que reduz os custos de gerenciamento e otimiza os clusters para produção. Mais informações em https://cloud.google.com/kubernetes-engine

  - **AKS**: é gerenciado pelo Microsoft Azure e pode ser implantado facilmente. Essa solução gerenciada do Kubernetes é boa para usuários do Azure porque pode se integrar a outras ferramentas do Azure disponíveis no ecossistema do Azure. Mais informações em https://azure.microsoft.com/en-us/services/kubernetes-service

#### **5. Kubernetes - The Hard Way:** O método da maneira mais difícil é usado para instalar o Kubernetes do zero. Sugiro este tipo de instalação para todos que desejam aprender todos os componentes do Kubernetes para entender profundamente o Kubernetes. Se você quiser saber o processo de implantação de um cluster e o que acontece entre os componentes do cluster, instale o Kubernetes com esse método pelo menos uma vez.

  - **Kelsey Hightower:** explica como implantar o Kubernetes do zero no Google Cloud Platform. Mais informações em https://github.com/kelseyhightower/kubernetes-the-hard-way

  - **Mumshad Mannambeth:** bifurca o método do Kelsey Hightower e o alterou para implantar em máquinas locais usando o Vagrant, porém não é atualizada para o Kubernetes mais recente. Mais informações em https://github.com/mmumshad/kubernetes-the-hard-way

### **Instalação minikube**
#### 0. Pré-requisitos:
- 2 CPUs ou mais
- 2 GB de memória livre
- 20 GB de espaço livre em disco
- Conexão de internet
- Gerenciador de contêiner ou máquina virtual, como: Docker, Hyperkit, Hyper-V, KVM, Parallels, Podman, VirtualBox ou VMware Fusion/Workstation

#### 1. Instalação:
- **Linux:**
Para instalar a última versão estável do minikube no x86-64 Linux usando o download binário:

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```
- **Windows:**
Para instalar a última versão estável do minikube no Windows x86-64 usando o download do executável:

```bash
$oldPath = [Environment]::GetEnvironmentVariable('Path', [EnvironmentVariableTarget]::Machine)
if ($oldPath.Split(';') -inotcontains 'C:\minikube'){ `
  [Environment]::SetEnvironmentVariable('Path', $('{0};C:\minikube' -f $oldPath), [EnvironmentVariableTarget]::Machine) `
}
```

Adicione o binário minikube.exe ao seu PATH:

```bash
New-Item -Path 'c:\' -Name 'minikube' -ItemType Directory -Force
Invoke-WebRequest -OutFile 'c:\minikube\minikube.exe' -Uri 'https://github.com/kubernetes/minikube/releases/latest/download/minikube-windows-amd64.exe' -UseBasicParsing
```

- **macOS:**
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64
sudo install minikube-darwin-amd64 /usr/local/bin/minikube
```

#### 2. Inicie seu cluster:
```bash
minikube start
```

#### 3. Interaja com seu cluster:
**3.1. Instalação do Kubectl:**
- **Linux:**

Baixe a versão mais recente com o comando:
```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
```
Instale o Kubectl:
```bash
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

- **Windows:**

Baixe a versão mais recente com o comando:
```bash
curl.exe -LO "https://dl.k8s.io/release/v1.25.0/bin/windows/amd64/kubectl.exe"
```
Adicione a pasta binária kubectl às suas variáveis de ambiente.

- **macOS:**

Baixe a versão mais recente com o comando:
```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl"
```
Torne executável o binário kubectl:
```bash
chmod +x ./kubectl
```
Mova o binário kubectl para um local de arquivo no PATH:
```bash
sudo mv ./kubectl /usr/local/bin/kubectl
sudo chown root: /usr/local/bin/kubectl
```

**3.2. Explore comandos do kubectl:**

Execute o comando a seguir para visualizar os pods no seu cluster:
```bash
kubectl get po -A
```

**3.3. Interface gráfica:**

Execute o comando a seguir para acessar a interface gráfica:
```bash
minikube dashboard
```

#### 3. Gerencie seu cluster:
- Pausar: 
```bash
minikube pause
```
- Continuar: 
```bash
minikube unpause
```
- Parar: 
```bash
minikube stop
```
- Mudar o limite de memória padrão:
```bash
minikube config set memory 9001
```
- Catálogo de serviços do Kubernetes:
```bash
minikube addons list
```
- Criar um segundo cluster executando uma versão mais antiga do Kubernetes:
```bash
minikube start -p aged --kubernetes-version=v1.16.1
```
- Excluir todos os clusters do minikube:
```bash
minikube delete --all
```

## Getting Started

```javascript
import Component from 'my-project'

function App() {
  return <Component />
}
```


## Ferramentas similares
- **Docker Swarm:** 
  - **Vantagens:** é simples de instalar, especialmente para aqueles que estão entrando no mundo da orquestração de contêineres. É leve e fácil de usar. Além disso, fornece balanceamento de carga automatizado nos contêineres do Docker, enquanto outras ferramentas de orquestração de contêineres exigem esforços manuais. Funciona com o Docker CLI, portanto, não há necessidade de executar ou instalar todo o novo CLI. Além disso, funciona perfeitamente com as ferramentas existentes do Docker, como o Docker Compose. Por fim, não requer mudanças de configuração se o seu sistema já estiver rodando dentro do Docker.
  - **Desvantagens:** é leve e vinculado à API do Docker, o que limita sua funcionalidade, em comparação com o Kubernetes. Da mesma forma, os recursos de automação não são tão robustos quanto os oferecidos pelo Kubernetes.
- **Nomad:**
  - **Vantagens:** é fácil de instalar e operar porque se concentra apenas no gerenciamento de cluster. Em geral, é uma plataforma mais simples que o Kubernetes. Ele também suporta vários tipos de cargas de trabalho.
  - **Desvantagens:** oferece funcionalidade limitada, o que requer a instalação de ferramentas de terceiros para resolver tarefas que o Kubernetes implementa por padrão.
- **ECS:**
  - **Vantagens:** permite que você opere contêineres sem precisar gerenciar máquinas virtuais diretamente. Além disso, implanta VMs e gerencia contêineres nelas sem intervenção do usuário. O Amazon ECS é protegido por padrão, com todos os contêineres executados em uma nuvem privada virtual com rede isolada e segura. Ademais, é perfeitamente integrado a outros serviços da Amazon que são úteis para cargas de trabalho em contêineres, como Elastic Load Balancing, CloudWatch, CloudFormation e IAM. Como os contêineres são imutáveis, você pode executar muitas cargas de trabalho usando Amazon EC2 Spot Instances (que podem ser encerradas sem aviso prévio) e economizar 90% nos custos de instância sob demanda.
  - **Desvantagens:** os contêineres só podem ser implantados na Amazon. Além disso, o ECS só pode gerenciar contêineres que criou. Além disso, o armazenamento externo é limitado à Amazon, incluindo o Amazon EBS. Sendo um produto da Amazon, não está disponível publicamente para implantação fora da Amazon. Grande parte do código ECS não está disponível publicamente. Apenas algumas das partes do ECS, como o AWS Blox, que é uma estrutura que ajuda os clientes a criar agendadores personalizados, são de código aberto da Amazon.
  
- **Apache Mesos:**
  - **Vantagens:** se você tiver cargas de trabalho existentes, por exemplo (Hadoop, Kafka, Spark, etc), o Mesos facilita muito o uso dessas cargas de trabalho juntas. Muitos aplicativos modernos de processamento de dados (Hadoop, Kafka, Spark) funcionam muito bem no Mesos. Isso é especialmente bom porque todos eles podem ser executados no mesmo pool de recursos, junto com novos aplicativos empacotados em contêiner. O Mesos é um software que tem sido usado em muitos projetos de grande escala (é usado pelo Twitter, Ebay e AirBnB) e pode suportar centenas de milhares de nós.
  - **Desvantagens:** ao trabalhar com pequenos clusters (menos de uma dúzia de nós), o Mesos pode ser uma solução complicada demais, pois é de baixo nível e projetado para grandes clusters e dimensionamento.

## Referências
- Documentação do Kubernetes: https://kubernetes.io/
- Documentação do Minikube: https://minikube.sigs.k8s.io/docs/start/
- Documentação do Kind: https://kind.sigs.k8s.io/
- Documentação do k3s: https://k3s.io/
- Documentação do k3d: https://k3d.io/
- Documentação do Microk8s: https://microk8s.io/
- Documentação do Kubeadm: https://kubernetes.io/docs/reference/setup-tools/kubeadm
- Documentação do Kubespray: https://github.com/kubernetes-sigs/kubespray
- Documentação do Kops: https://kops.sigs.k8s.io
- Documentação do RKE: https://github.com/rancher/rke
- Documentação do Charmed Kubernetes: https://ubuntu.com/kubernetes
- Documentação do KubeSphere: https://kubesphere.io
- Documentação do Kubermatic: https://github.com/kubermatic/kubermatic
- Documentação do KubeOne: https://github.com/kubermatic/kubeone
- Documentação do Magnum: https://docs.openstack.org/magnum/latest
- Documentação do EKS: https://aws.amazon.com/eks
- Documentação do GKE: https://cloud.google.com/kubernetes-engine
- Documentação do AKS: https://azure.microsoft.com/en-us/services/kubernetes-service
- Kelsey Hightower - Kubernetes The Hard Way: https://github.com/kelseyhightower/kubernetes-the-hard-way
- Mumshad Mannambeth - Kubernetes The Hard Way: https://github.com/mmumshad/kubernetes-the-hard-way
- https://www.servertribe.com/kubernetes-alternatives-container-orchestration-tools/
- https://www.youtube.com/watch?v=PH-2FfFD2PU
- https://www.youtube.com/watch?v=VnvRFRk_51k
- https://www.youtube.com/watch?v=aSrqRSk43lY
- https://www.youtube.com/watch?v=cC46cg5FFAM

## Autores
[ambueno](https://www.github.com/ambueno)
