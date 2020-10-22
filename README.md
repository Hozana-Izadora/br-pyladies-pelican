Site Pyladies Brasil
====================
[![Build Status](https://app.codeship.com/projects/bca2dab0-d874-0134-15a2-326e4d300ce2/status?branch=master)](https://app.codeship.com/projects/bca2dab0-d874-0134-15a2-326e4d300ce2/status?branch=master)

Contribuindo
------------

Para contribuir com o projeto veja o guia de [Contribuição](https://github.com/pyladies-brazil/br-pyladies-pelican/blob/master/CONTRIBUTING.md). Lá você encontrará instruções detalhadas de como fazer a sua contribuição.

Instalando e Rodando
--------------------
* [Requisitos Mínimos](#requisitos)
* [Instalação no Linux](#linux)
  - [Usando ambiente virtual](#linux-venv)
  - [Usando docker-compose](#linux-docker)
* [Instalação Windows](#windows)
  - [Usando o docker-compose](#windows-docker)

Requisitos Mínimos
-----
* Python 3.6
* [pip](https://pip.pypa.io/en/stable/)

Instalação no Linux
====================

Usando ambiente virtual
------------
Para rodar o site localmente, você precisa de um ambiente virtual.
Nós usamos o [virtualenv](https://virtualenv.pypa.io/en/stable/), mas se você tem experiência com outros, como o pyenv, não tem problema.
Para verificar a instalação do `virtualenv`, digite

```console
$ virtualenv --version
```
- Se a saida for uma numeração, como `16.1.0`, isso significa que
está instalado. Caso contrario, para instalar o virtualenv basta fazer:

```console
$ pip install virtualenv
```
- O mesmo procedimento pode ser feito para o git. Verifique se já está instalado,
com o comando:
``` console
$ git --version
```

- Se a saída for algo como `git version 2.17.1`, significa que o git já está
instalado. Caso contrário, para instalar o git basta fazer:
``` console
$ sudo apt install git  # para ubuntu
```

> **Observação**: Esse comando funciona apenas em sistemas operacionais que utilizam o
`apt` gerenciador de pacotes. Caso não seja o seu caso, [verifique como instalar](https://git-scm.com/download/linux) o git no seu sistema.

- Assumindo que seu git e virtualenv já estão configurados, faça o clone do repositório

``` console
$ git clone https://github.com/pyladies-brazil/br-pyladies-pelican.git
```
- Após conclusão do clone, acesse o diretório recém-criado

``` console
$ cd br-pyladies-pelican
```
- Rode o comando para criação de ambiente virtual e instalação das dependências

``` console
$ virtualenv .venv 			# cria ambiente virtual
$ source .venv/bin/activate		# ativa o ambiente
$ pip install -r requirements.txt	# instala as dependências
```

- Rode o projeto

``` console
$ make up
```

Abra o browser em [localhost:8000](http://localhost:8000) para ver o conteúdo gerado.

**Observação**: Se sua porta 8000 já estiver em uso, você pode especificar uma porta diferente ao
usar o parâmetro `PORT`. Por exemplo:

```console
$ make up PORT=8001
```

E então acessar [localhost:8001](http://localhost:8001). Atenção! Algumas [portas são reservadas](https://pt.wikipedia.org/wiki/Lista_de_portas_dos_protocolos_TCP_e_UDP).

Para desativar o ambiente virtual

```console
$ deactivate
```
Para mais informações a respeito do `Makefile` e suas opções, digite

```console
$ make help
```

Usando docker-compose
----------------------

Instale [o docker no seu computador](https://docs.docker.com/install/) em seguida execute os passos abaixo:

``` console
$ git clone git@github.com:pyladies-brazil/br-pyladies-pelican.git
$ cd br-pyladies-pelican
$ docker-compose up
```

Agora basta acessar o navegador em [localhost:8000](http://localhost:8000) para ver o conteúdo gerado.

Instalação no Windows
===============

Usando o docker-compose
--------------------------
- [Opcional] Instale o [Visual Studio Code](https://code.visualstudio.com/) para fazer códigos legais;
- [Opcional mas fortemente indicado] Instale o [Git para Windows](https://desktop.github.com/) para um shell mais legal também;
- Python 3.8 está disponível na loja do Windows e você deve instalar também. Só procurar e clicar em obter que está tudo certo;
- Abra o Windows Powershell como administrador e faça a instalação do [chocolatey](https://chocolatey.org/install). Com ele poderemos instalar o comando make que será utilizado junto ao Docker;
- Com o comando *choco* sendo reconhecido no Windows, [instale o make](https://chocolatey.org/packages/make) com `choco install make`;
- Por último, faça a instalação do [Docker](https://docs.docker.com/docker-for-windows/install/), certifique-se que os requisitos mínimos estão sendo cumpridos. Para o Windows 10 Home, é recomendado que atualize o sistema antes da instalação (Configurações → Atualização e Segurança → Windows Update)
    - Atente-se se o WSL2 está rodando na sua máquina. Se ainda for o WSL, [atualize](https://docs.microsoft.com/pt-br/windows/wsl/wsl2-kernel).
- Faça fork do [repositório](https://github.com/pyladies-brazil/br-pyladies-pelican);
- Reinicie o computador para garantir que todas as mudanças foram efetuadas e salvas;
- Agora você tem duas formas de rodar o projeto seguindo o:
    - Comando `make up`
    - Comando `docker-compose up`
- Utilizando o terminal:
    ``` console
    $ git clone git@github.com:pyladies-brazil/br-pyladies-pelican.git
    $ cd br-pyladies-pelican
    $ docker-compose up
    ```
    ou

    ``` console
    $ git clone git@github.com:pyladies-brazil/br-pyladies-pelican.git
    $ cd br-pyladies-pelican
    $ make up
    ```

Links Úteis
-----------

* [Criar um grupo PyLadies](https://brazilpyladies.gitbooks.io/handbook/content/)
* [Documentação git](https://git-scm.com/doc)
* [Documentação Pelican](http://docs.getpelican.com/en/3.6.3/)
* [pyenv](https://github.com/yyuu/pyenv)
* [virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/)

Esse repositório é mantido com :heart: pelo @pyladies-brazil/tech-team
