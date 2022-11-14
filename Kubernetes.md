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

- #### Instalação do Kubernetes para desenvolvimento:
É usado para um único nó ou para uma configuração rápida do Kubernetes. Para fins de desenvolvimento, colocamos tudo em um único nó. Por isso é limitado a um nó.

-> Minikube: É uma implementação leve do Kubernetes que cria um cluster Kubernetes em um único host com um conjunto de pequenos recursos para executar uma pequena implantação do Kubernetes. Ele é destinado a cenários de teste do Kubernetes (criação de pods, serviços, gerenciamento de armazenamento, regras de entrada de rede, etc), mas no ambiente local para o desenvolvedor ou administrador testar. Ele não se destina ao uso em produção, pois executa uma máquina virtual, instala o Docker e, em seguida, implanta os contêineres essenciais do Kubernetes. O Minikube é um Kubernetes local, com foco em facilitar o aprendizado e o desenvolvimento do Kubernetes. Tudo o que você precisa é de um contêiner Docker (ou similarmente compatível) ou um ambiente de máquina virtual, e o Kubernetes está a um único comando: minikube start.

-> Docker: Kubernetes com Docker Desktop é para um único nó. Está disponível para Windows, Mac e Linux, sendo utilizado localmente em nossos sistemas. Fazemos isso como um sandbox de desenvolvedor. É conveniente e fácil de instalar e é usado principalmente para fins de teste.


- #### Instalação não gerenciada do Kubernetes (baseada no instalador):
Na instalação não gerenciada do Kubernetes, tudo precisa ser gerenciado pelo desenvolvedor, o que significa que todos os nós, independente de seu tipo,
são gerenciados pelo desenvolvedor. Ele não é gerenciado por um fornecedor de nuvem, portanto, conhecido como não gerenciado ou baseado em instalador.

 -> Kubeadm: É uma ferramenta criada para fornecer kubeadm init e kubeadm join como “caminhos rápidos” de práticas recomendadas para a criação de clusters
Kubernetes. Ele executa as ações necessárias para obter um cluster mínimo viável em funcionamento. Por design, ele se preocupa apenas com a inicialização,
não com o provisionamento de máquinas. Podemos usar o kubeadm para criar um ambiente Kubernetes de nível de produção.

 -> Kops: O Kubernetes Operations, ou Kops, é um projeto de código aberto usado para configurar clusters do Kubernetes com facilidade e rapidez. É considerada
a maneira “kubectl” de criar clusters. Kops permite a implantação de clusters Kubernetes altamente disponíveis na AWS.

 -> Kubespray: Os clusters do Kubernetes podem ser criados usando várias ferramentas de automação. Kubespray é uma combinação de Kubernetes e Ansible.
Isso significa que podemos instalar o Kubernetes usando o Ansible. Também podemos implantar clusters usando serviços de computação em nuvem kubespray, como
EC2 (AWS). O Kubespray oferece flexibilidade de implantação. Ele permite que você implante um cluster rapidamente e personalize todos os aspectos da implementação.


- #### Tudo do zero (Kubernetes The Hard Way):
É otimizado para aprendizado, o que significa seguir o longo caminho para garantir que você entenda cada tarefa necessária para inicializar um cluster Kubernetes. 
Sendo indicado para àqueles que planejam dar suporte a um cluster Kubernetes de produção e querem entender como tudo se encaixa, ou seja, não se trata um comando totalmente automatizado para abrir um cluster Kubernetes.



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

