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

