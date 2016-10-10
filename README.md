# Tutorial Caelum 

## Configurações necessárias

### docker

#### Mac

Instalar a última versão estável do docker for Mac [https://www.docker.com/products/docker#/mac]. Não instalar o docker toolbox. Se você já tem o toolbox instalado na sua máquina e não quer/pode remover/atualizar o toolbox prefira realizar o tutorial utilizando uma vm com uma distribuição linux de sua preferência.

Esta instalação não remove suas imagens/containers atuais caso você já execute o docker na sua maquina de outra forma.

É importante que seja instalada a versão stable. Caso você já utilize a versão beta, por favor, desinstale e instale a stable. Neste caso pode haver perda de containers e imagens, logo faça um backup se necessário.

#### Windows

Instalar a última versão estável do docker for Windows [https://www.docker.com/products/docker#/windows]. Não instalar o docker toolbox. Se você já tem o toolbox instalado na sua máquina e não quer/pode remover/atualizar o toolbox prefira realizar o tutorial utilizando uma vm com uma distribuição linux de sua preferência.

É importante que seja instalada a versão stable. Caso você já utilize a versão beta, por favor, desinstale e instale a stable. Neste caso pode haver perda de containers e imagens, logo faça um backup se necessário.

#### Linux

Existem repositório de pacotes para a instalação do docker mantidos pela Docker Inc para a maioria das distribuições.

A instalação é simples, pois geralmente está relacionada com a configuração de um repositório novo e a instalação dos pacots necessários. Os detalhes para cada distribuição podem ser encontrados em [https://docs.docker.com/engine/installation/linux/]

Se você já tem o docker instalado conforme o procedimento mencionado acima, por favor atualize a versão para a versão 1.11 ou superior.

Se você já tem o docker instalado e não quer/pode atualizar a versão utilize uma VM com sua distribuição Linux favorita.

### Imagens que serão utilizadas

Visando evitar perder tempo fazendo downloads de imagens será necessário que algumas imagens sejam baixadas para a máquina que será utilizada durante o tutorial.

Você deve realizar isso depois que finalizar sua instalação do docker conforme o procedimento descrito no tópico anterior.

Para obter as imagens você deve executar os seguintes comandos num terminal:

```
docker pull busybox
```
```
docker pull ubuntu
```
```
docker pull ubuntu:trusty
```
```
docker pull fedora
```
```
docker pull alpine
```
```
docker pull openjdk
```
```
docker pull openjdk:alpine
```
```
docker pull openjdk:jre
```
```
docker pull openjdk:jre-alpine
```
```
docker pull maven
```
```
docker pull nginx
```
```
docker pull nginx:alpine
```
```
docker pull mysql
```
```
docker pull postgres
```
```
docker pull php
```
```
docker pull php:apache
```
```
docker pull php:alpine
```
```
docker pull php:5
```
```
docker pull php:5-alpine
```
```
docker pull php:5-apache
```
```
docker pull ruby
```
```
docker pull python
```


### Vagrant

#### Instalação

A instalação do Vagrant deve ser realizada de acordo com o link [https://www.vagrantup.com/downloads.html] e selecione a plataforma desejada.

#### CoreOS box

No nosso tutorial iremos utilizar o vagrant para disponibilizarmos uma VM com CoreOS. Na pasta `coreos` temos um Vagrantfile modificado do repositório oficial [https://github.com/coreos/coreos-vagrant] apenas para utilizarmos a versão stable da distribuição.

Para inicializar a VM entra na pasta `coreos` e digite:

```
vagrant up
```

Você verá que o vagrant executa algumas tarefas para provisionar a máquina, uma delas é lhe informar que existe uma atualização do box. Para atualizá-lo voce deve deve executar:

```
vagrant box update
```

Para acessar a máquina criada basta executar:
```
vagrant ssh
```

Se você não ver no prompt a seguinte informação:
```
$ vagrant ssh
CoreOS stable (1122.2.0)
```

Execute os seguintes comandos:
```
vagrant destroy
```
```
vagrant up
```
