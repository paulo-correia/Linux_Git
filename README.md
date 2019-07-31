# Git

![](https://github.com/paulo-correia/Linux_Git/blob/master/Git-logo.svg.png)

Git é um sistema de controle de versões distribuído e um sistema de gestão de código fonte, com ênfase na velocidade. O Git foi inicialmente projetado e desenvolvido por Linus Torvalds para o desenvolvimento do kernel Linux, mas foi adotado por muitos outros projetos.

## Instalação

Toda a instalação é feita em **root**

### Debian

 Instalar os pacotes git e git-doc com o comando:

`apt-get install git git-doc`

### CentOS

Instalar o pacote git com o comando:

`yum -y install git`

## Configuração

`git config --system color.ui true`

Global (como usuário comum) numa pasta que o usuário possa gravar (Ex: home/usuário)

```
git config --global user.name "Nome"
git config --global user.email "e-mail@mail.com"
```

## Testes

Criação de repositório (como usuário comum)

 ```
mkdir nome.git
cd nome.git
git init
```

Verificação da inicialização (como usuário comum)

 ```
git status

Resposta:
On branch master
Initial commit
nothing to commit (create/copy files and use "git add" to track)
```

Verificação (como usuário comum)

 ```
dentro da pasta nome.git:

echo "Projeto de testes" > LEIAME
git add .
git status

Resposta:
On branch master
Initial commit
Changes to be committed:
 (use "git rm --cached <file>..." to unstage)
        new file:   LEIAME

git commit -m "adicionar o arquivo LEIAME do projeto"
```

Acesso por SSH

 ```
git clone usuario@servidor:~/nome.git

Resposta:
Cloning into 'nome'...
usuario@servidor password: 
remote: Counting objects: 3, done. 
remote: Total 3 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (3/3), done.
```
