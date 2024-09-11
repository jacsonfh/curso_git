# Git

## Instalar o Git
```bash
sudo dnf install git
```

## Configurar o git
```bash
git config --global user.name "Seu Nome"
git config --global user.email "Seu e-Mail"
git config --global core.editor vim
```

#### Visualizar Config
```bash
git config user.name
```

#### Listar tudo.
```bash
git config --list
```

#### Configurar um projeto.
```bash
mkdir git-course
cd git course
git init # Para inicializar o diretório, e vai criar o diretório .git
```

#### Verficar o status dos seus arquivos da branch
```bash
git status
```

#### Adicionar um arquivo.
#### Clonar ou criar uma nova 
```bash
git clone [https://link-com-o-nome-do-repositório](https://link-com-o-nome-do-repositorio)
```

#### Criar uma branch  é necessário haver um commit antes.
```bash
git add .
git commit -m "Inicialização do projeto"
git branch `<nome-da-branch>`
```

#### Muda para branch criada.
```bash
git checkout `<nome-da-branch>`
```

#### Enviar Arquivo.
```bash
git push -u `<local-remoto>` `<nome-da-branch>`
```

#### Ver as branches:
```bash
git branch #ou 
git branch --list
```

#### Excluir uma branch:
```bash
git branch -d `<nome-da-branch>`
git checkout `<nome-da-branch>`
```

### Alguns comandos de git
* Este é um estudo de comandos para usar no repositório github.
```bash
git status #Para ver o status do branch no stage que é local. 
git add 
```

#### Para adicionar arquivos no breach localmente.
```bash
git commit -m "Descrição do Commit"
git log #Mostra minhas entradas na branch. 
git log --decorate #log com mais informacoes.
git log --author=Jacson #Lista todas as entradas do autor Jacson.
git shortlog
git shortlog -sn
git log --graph
git show 71ef465e9c1d8069855efa0... #Dentro do git log tem uma hash e pla hash é possível ver o que foadicionado.
git diff --name-only #Mostra somente o nome do arquivo que foi modificado.
git diff #mostra as diferencas antes de commit e para dar uma ultima lida e ver o que você fez.
git checkout nome_arquivo.py #Fazendo isso o git vai retornar o arquivo para antes da edição. Quanto você quer trocar de um repositorio para o outro você da um git checkout
```
#### Alternar entre repositórios.
Se está em um repositorio e quer cirar uma ramificação a partir desse repositorio você também usa ele.
Deve-se manter sempre dois repositorios apenas (main, develop)
Sempre que começar um projeto novo vc entra no develop e cria um branch novo a partir dele.
```bash
git checkout develop
git checkout -b nova_branch
git checkout -b <nome_do_novo_repositorio>
git reset HEAD readme_git.py #Fazer o git tirar a última entrada do commit.
git commit -am #Adicionando todos os modif. mais a minha msg.
git reset --soft #Volta o Commit para o Stage.
git reset --mixed #Volta o Commit para o stage, e volta os arquivos para antes do stage
git reset --hard #apaga o ultimo commit e volta os aquivos para antes de ele existir.
git reset --soft 001523c82fe2d3fea4480b44eec8f4d270e30a3b #Você deve voltar para um comit anterior.
```
#### Trabalhando com repositório remoto.
```bash
git init #Se logar no github.
```
* Adicione a sua chave publica ssh nas configurações de segurança do gitHub.
```bash
git remote add origin git@github.com:jacsonfh/developer.git #conecte a sua pasta ao repositorio desejado.

git remote -v #Mostra se está conectado ao repositório.

git push -u origin master #ver o que houve.

git clone ls nomeclone #Clonar repositório es colha uma nova pasta.

git switch master #Por exemplo para mudar para branch master.
É interessante ter uma pasta para cada branch.

git remote add origin git@github.com:jacsonfh/developer.git -m dev #Adicionar branch especifica.

>Fork - Cria uma cópia de um projeto para você alterar e depois devolver.
>Breanch - Possibilita manter uma versão master e diversas outras assim.

git checkout -b nome_novo_breach #Criando um breanch -b cria um novo, sem ele muda para o branch em questão.

git branch #Mostra os branchs que tem e qual você está.

git branch -D nome_branch_apagar #para apagar um branch especifico.
Merge e Rebase = para juntar branch com as modificações.
branch merge junta todas as modificações.
branch rebase joga as modificações fora do master para o frente da fila do master.

git init # Comando para inicializar o repositório.

git push --set-upstream origin testing # Levar a saida para o branch chamado testing.

git merge testing # Dentro do master leva tudo para o master.

git log --graph # mostra o gráfico da branch.

```
#### Criar o arquivo .gitignore
```bash
git stash #para guardar alguma modificacao para aplicar depois WIP - work in progress.
git stash list #mostra todas as minhas modif. guardadas. clear para limpar os statist. git stash apply para aplicar alguma alteracao.

git config --global alias.s status #Criar alias no git.

git tag -a 1.0.0 -m aspas Todos os comandos do Curso.aspas #cria a tag da versão.

git push origin master --tags

git revert b56224d7814f594d9149f3f983ad751dee5331fe #para reverter um commit, mas deixa no meu codigo.

git tag -d 1.0.0 e depois git push origin :1.0.0 tags ou branch para apagar.

git switch master #Por exemplo para mudar para branch master. (não se usa) Se usa git checkout master git checkout -b nome_novo_breach #Criando um breanch -b cria um novo, sem ele muda para o branch em questão. incorreto ele muda para o novo branch git checkout -b branch_novo (mude para o branch_novo a partir do branch que eu estou)
```

## Mini Resumo
```bash
git pull

git fetch

git prune

git add .

git commit -am "Mensagem"

git push
```
