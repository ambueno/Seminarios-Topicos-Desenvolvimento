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

- #### Empacotamento (Bin packing) automático:
Organiza automaticamente os contêineres com base em seus requisitos de recursos e outras restrições,
sem sacrificar a disponibilidade. Combinando cargas de trabalho críticas e de melhor esforço para
aumentar a utilização e economizar ainda mais recursos. 

- #### Gerenciamento de configurações e Secret:
O Kubernetes permite armazenar e gerenciar informações confidenciais, como senhas, tokens OAuth e chaves SSH. 
Você pode implantar e atualizar segredos e configuração de aplicativos sem reconstruir suas imagens de contêiner e
sem expor segredos em sua configuração de pilha.

- #### Projetado para extensibilidade:
Possibilita adicionar recursos ao seu cluster Kubernetes sem alterar o código-fonte anterior.

- #### Orquestração de armazenamento:
Monta automaticamente o sistema de armazenamento de sua escolha, seja de armazenamento local,
um provedor de nuvem pública, como AWS ou GCP, ou um sistema de armazenamento de rede, como NFS, iSCSI, Ceph, Cinder.

- #### Descoberta de serviços e balanceamento de carga:
Não há necessidade de modificar seu aplicativo para usar um mecanismo de descoberta de serviço desconhecido.
O Kubernetes fornece aos pods seus próprios endereços IP e um único nome DNS para um conjunto de pods e pode balancear a carga (load-balance) entre eles.

- #### Autocura:
Reinicia os contêineres que falham, substitui e reagenda contêineres quando os nós morrem,
elimina contêineres que não respondem à verificação de integridade definida pelo usuário e
não os anuncia aos clientes até que estejam prontos para serem utilizados.

- #### Dimensionamento (scaling) horizontal:
Dimensionamento da sua aplicação com um comando, com uma interface do usuário ou automaticamente com base no uso da CPU.

- #### IPv4/IPv6 dual-stack:
Alocação de endereços IPv4 e IPv6 para pods e serviços

- #### Execução em lote:
Além dos serviços, o Kubernetes pode gerenciar suas cargas de trabalho de lote e CI, substituindo contêineres que falham, se desejado.

- #### Rollouts e rollbacks automatizados:
O Kubernetes lança progressivamente alterações em sua aplicação ou em sua configuração, enquanto monitora a integridade da aplicação
para garantir que ele não mate todas as suas instâncias ao mesmo tempo. 
Se algo der errado, o Kubernetes reverterá a alteração para você. Aproveite um ecossistema crescente de soluções de implantação.


## Instalação & Configuração

#### **1. Instalação de nó único:** Este tipo de instalação é adequado para quem deseja visualizar o Kubernetes ou é adequado para práticas, testes e fins de desenvolvimento. Existem muitas distribuições de Kubernetes de nó único no mercado, mas apresento as mais populares.

 - **Minikube**: é uma distribuição Kubernetes de nó único que é lançada oficialmente pela comunidade Kubernetes. A versão mais recente do Kubernetes pode ser executada com o minikube. Juntamente com a instalação do Kubernetes, alguns complementos do Kubernetes podem ser executados facilmente. Com o minikube, o Kubernetes pode ser implantado em sistemas VM, Container ou bare-metal. Vários ambientes de execução de contêiner (Docker, Containerd, CRI-O) também são suportados.

Mais informações em https://minikube.sigs.k8s.io

  - **Kind**: é uma distribuição para executar o cluster Kubernetes dentro de contêineres do Docker em seu sistema local. kind significa “Kubernetes in Docker” Esta distribuição é adequada para testes, desenvolvimento local e sistemas de CI. kind é distribuído oficialmente pela comunidade Kubernetes.

Mais informações em https://kind.sigs.k8s.io

  - **k3s**: é outra distribuição útil lançada pela Rancher. Ele foi desenvolvido inicialmente para IoT e computação de borda, mas pode ser usado para qualquer outra finalidade. Você pode executar um Kubernetes de nó único ou um cluster com alguns comandos.

Mais informações em https://k3s.io

  - **k3d**: é um auxiliar para executar k3s no Docker. Ele lança um cluster Kubernetes em sua máquina local como “tipo”. k3d é lançado pela Rancher.

Mais informações em https://github.com/rancher/k3d

  - **microk8s**: é outra opção de instalação. Não apenas um Kubernetes de nó único, mas um cluster também pode ser implantado usando microk8s. Esta distribuição do Kubernetes é lançada pela Canonical - a empresa que lança o Ubuntu - e está disponível no gerenciador de pacotes rápido. O Kubernetes pode ser implantado com alguns comandos. Juntamente com o Kubernetes, está disponível uma lista de vários complementos que podem ser implantados facilmente.

Mais informações em https://microk8s.io

#### **2. Instalação manual do cluster:** Esse tipo de instalação é usado para implantar um cluster mínimo viável. Algumas partes da instalação devem ser feitas manualmente. É a maneira preferida de implantar o cluster Kubernetes pela primeira vez.

  - **Kubeadm**: é uma ferramenta que é usada para implantar um cluster por mãos humanas. Ele é usado para inicializar componentes do Kubernetes, não para provisionar máquinas. Antes de inicializar o cluster, algumas ações devem ser feitas manualmente.

Mais informações em https://kubernetes.io/docs/reference/setup-tools/kubeadm

#### **3. Instalação automática do cluster:** Esse tipo de instalação é feito usando ferramentas de automação, scripts ou instaladores distribuídos pelo provedor. É uma maneira preferencial para aqueles que desejam implantar clusters Kubernetes de nível de produção em um ambiente local ou desejam gerenciar o ciclo de vida do cluster manualmente.

 - **Kubespray**: é uma coleção de playbooks Ansible que são usados para implantar clusters de nível de produção em bare-metal e na nuvem. Juntamente com a instalação, as operações do segundo dia podem ser realizadas com o kubespray. Este instalador é mantido oficialmente pela comunidade Kubernetes. Uma dúzia de complementos estão disponíveis no kubespray e podem ser implantados facilmente junto com o Kubernetes. kubespray é uma das opções de instalação mais adequadas.

Mais informações em https://github.com/kubernetes-sigs/kubespray

  - **Kops**: não apenas gerenciará o ciclo de vida do cluster, mas também fornecerá a infraestrutura de nuvem necessária. A implantação na AWS é suportada oficialmente, a implantação em outros provedores de nuvem está disponível, mas em estado alfa e beta.

Mais informações em https://kops.sigs.k8s.io

  - **RKE**: é um Kubernetes distribuído do Rancher que pode implantar clusters Kubernetes de nível de produção sobre contêineres do Docker. O gerenciamento de clusters do Kubernetes é feito facilmente com o RKE. Se você deseja usar a plataforma Rancher, deve selecionar esta distribuição.

Mais informações em https://github.com/rancher/rke

  - **Charmed Kubernetes**: é a maneira canônica de implantar clusters Kubernetes com Juju. É adequado para executar o Kubernetes em ambientes multinuvem e bare-metal. Se você procura uma distribuição qualificada do Kubernetes que possa ser implantada no OpenStack, este instalador é para você.

Mais informações em https://ubuntu.com/kubernetes

  - **KubeSphere**: não é apenas uma distribuição Kubernetes, é também uma plataforma para criar uma solução em nuvem baseada em Kubernetes. Um grande número de ferramentas, complementos etc. podem ser implantados usando o KubeSphere junto com o Kubernetes. Essa plataforma também pode ser implantada no cluster Kubernetes existente.

Mais informações em https://kubesphere.io

  - **Kubermatic**: é uma plataforma Kubernetes assim como o Rancher. Você pode implantar e gerenciar clusters do Kubernetes em nuvens e no local. A conexão entre o cluster mestre/semente e os clusters downstream é tratada pelo OpenVPN.

Mais informações em https://github.com/kubermatic/kubermatic

  - **KubeOne**: é uma ferramenta para provisionar a infraestrutura necessária e implantar o Kubernetes em alguns provedores. Ele pode ser facilmente integrado ao Terraform e Kubermatic.

Mais informações em https://github.com/kubermatic/kubeone

#### **4. Clusters gerenciados:** O ciclo de vida dos clusters é gerenciado pelos provedores. Nesse tipo de instalação, um cluster de nível de produção pode ser implantado com ações mínimas do usuário. Os provedores são responsáveis por gerenciar todo o cluster, bem como a infraestrutura subjacente. Devido à facilidade de instalação e gerenciamento, este método é sugerido a qualquer pessoa. Outro benefício de usar o Kubernetes gerenciado é o acesso aos recursos da nuvem. Alguns provedores gerenciados do Kubernetes fornecem um conjunto de recursos úteis que podem não estar disponíveis em soluções locais ou bare-metal.

  - **Magnum**: é uma solução OpenStack para instalar Kubernetes gerenciados e outras ferramentas de orquestração no ecossistema OpenStack. Com o Magnum, os clientes da nuvem podem executar clusters do Kubernetes facilmente. Esse método também pode ser categorizado em Métodos de instalação automatizada de cluster. Decidi apresentá-lo aqui porque ele também suporta os incríveis recursos de nuvem. Além disso, os provedores de nuvem baseados em OpenStack podem fornecer esse método para seus clientes instalarem clusters Kubernetes gerenciados.

Mais informações em https://docs.openstack.org/magnum/latest

  - **EKS**: significa Elastic Kubernetes Service é a solução da Amazon para fornecer cluster Kubernetes gerenciado. O EKS pode ser facilmente integrado a outros serviços da Amazon. Uma ferramenta de linha de comando, eksctl, é usada para executar um cluster Kubernetes de produção em alguns minutos.

Mais informações em https://aws.amazon.com/eks

  - **GKE**: é uma versão do Kubernetes do Google Cloud, assim como o AWS EKS. O GKE oferece um modo de operação especial chamado Autopilot, que reduz os custos de gerenciamento e otimiza os clusters para produção.

Mais informações em https://cloud.google.com/kubernetes-engine

  - **AKS**: é gerenciado pelo Microsoft Azure e pode ser implantado facilmente. Essa solução gerenciada do Kubernetes é boa para usuários do Azure porque pode se integrar a outras ferramentas do Azure disponíveis no ecossistema do Azure.

#### **5. Kubernetes - The Hard Way:** O método da maneira mais difícil é usado para instalar o Kubernetes do zero. Sugiro este tipo de instalação para todos que desejam aprender todos os componentes do Kubernetes para entender profundamente o Kubernetes. Se você quiser saber o processo de implantação de um cluster e o que acontece entre os componentes do cluster, instale o Kubernetes com esse método pelo menos uma vez.

  - **Kelsey Hightower** é quem lançou o método da maneira difícil pela primeira vez, até onde eu sei. Ele explica como implantar o Kubernetes do zero no Google Cloud Platform.

Mais informações em https://github.com/kelseyhightower/kubernetes-the-hard-way

  - **Mumshad Mannambeth** bifurca o método explicado anteriormente e mudou isso para implantar em máquinas locais usando o Vagrant. Esta versão da maneira mais difícil não é atualizada para o Kubernetes mais recente.

Mais informações em https://github.com/mmumshad/kubernetes-the-hard-way

Mais informações em https://azure.microsoft.com/en-us/services/kubernetes-service

https://kubernetes.io/docs/tasks/tools/

https://kubernetes.io/docs/setup/production-environment/#production-cluster-setup

https://github.com/kubernetes/kubernetes/blob/master/README.md#to-start-developing-k8s

https://www.freecodecamp.org/news/the-kubernetes-handbook/

https://itnext.io/kubernetes-installation-methods-the-complete-guide-1036c860a2b3

https://instruqt.com/blog/digital-transformations/6-ways-to-run-kubernetes-in-the-cloud/

Install my-project with npm

```bash
  npm install my-project
  cd my-project
```
    
## Run Locally

Clone the project

```bash
  git clone https://link-to-project
```

Go to the project directory

```bash
  cd my-project
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```


## Recursos

- Light/dark mode toggle
- Live previews
- Fullscreen mode
- Cross platform


## Getting Started

```javascript
import Component from 'my-project'

function App() {
  return <Component />
}
```


## Ferramentas similares
## Authors

- [ambueno](https://www.github.com/ambueno)

