# Kubernetes

https://www.canva.com/design/DAFQQ4KyDIU/cmNiuZYSkgtmCzstqRP7oQ/edit?utm_content=DAFQQ4KyDIU&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

## O que é? 
Kubernetes (K8s) é um sistema open-source para automatizar a implantação (deployment),
 o dimensionamento (scaling) e o gerenciamento de aplicativos em containers.

## Como funciona? 
Se baseia no agrupamento de containers que compõem uma aplicação em unidades lógicas para 
facilitar o gerenciamento e a descoberta dos serviços.

## Recursos principais:

- #### Empacotamento (Bin packing) automático:
Organiza automaticamente os contêineres com base em seus requisitos de recursos e outras restrições,
sem sacrificar a disponibilidade. Combinando cargas de trabalho críticas e de melhor esforço para
aumentar a utilização e economizar ainda mais recursos. 

- #### Orquestração de armazenamento:
Monta automaticamente o sistema de armazenamento de sua escolha, seja de armazenamento local,
um provedor de nuvem pública, como AWS ou GCP, ou um sistema de armazenamento de rede, como NFS, iSCSI, Ceph, Cinder.

- #### Projetado para extensibilidade:
Possibilita adicionar recursos ao seu cluster Kubernetes sem alterar o código-fonte anterior.

- #### Autocura:
Reinicia os contêineres que falham, substitui e reagenda contêineres quando os nós morrem,
elimina contêineres que não respondem à verificação de integridade definida pelo usuário e
não os anuncia aos clientes até que estejam prontos para serem utilizados.

- #### Descoberta de serviços e balanceamento de carga:
Não há necessidade de modificar seu aplicativo para usar um mecanismo de descoberta de serviço desconhecido.
O Kubernetes fornece aos pods seus próprios endereços IP e um único nome DNS para um conjunto de pods e pode balancear a carga (load-balance) entre eles.

- #### IPv4/IPv6 dual-stack:
Alocação de endereços IPv4 e IPv6 para pods e serviços

- #### Dimensionamento (scaling) horizontal:
Dimensionamento da sua aplicação com um comando, com uma interface do usuário ou automaticamente com base no uso da CPU.

- #### Execução em lote:
Além dos serviços, o Kubernetes pode gerenciar suas cargas de trabalho de lote e CI, substituindo contêineres que falham, se desejado.

- #### Rollouts e rollbacks automatizados:
O Kubernetes lança progressivamente alterações em sua aplicação ou em sua configuração, enquanto monitora a integridade da aplicação
para garantir que ele não mate todas as suas instâncias ao mesmo tempo. 
Se algo der errado, o Kubernetes reverterá a alteração para você. Aproveite um ecossistema crescente de soluções de implantação.

## Introdução

https://kubernetes.io/docs/tutorials/kubernetes-basics/

https://blog.brainboard.co/kubernetes-explained#-problem-automation-and-speed


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

