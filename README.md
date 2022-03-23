# 1 - Introdução ao controle de versões com Git
``` bash 
  git init

```
# 2 - O ciclo básico do Git
#### Verificar arquivos que estão sendo controlados pelo Git
``` bash 
  git ls-files
```

#### Estado atual dos arquivos
``` bash 
  git status

```
#### Adicionar o arquivo para ser monitorado pelo Git/ Adicionar arquivos alterados
``` bash 
  git add index.html
```

#### Gravar alterações no repositório
``` bash 
  git commit -m "Criando o Projeto"
```

#### Configurar usuário Git somente para o repositório atual
``` bash 
  git config user.name "João Paulo"
  git config user.email "joaopaulo@gmail.com"
```

#### Configurar usuário Git para o computador
``` bash 
  git config --global user.name "João Paulo"
  git config --global user.email "joaopaulo@gmail.com"
```
# 3 -  Sincronização dos dados com o repositório
#### Verificar o histórico de commits
``` bash
  git log 
```

#### Mostra além dos commits quais arquivos foram alterados
``` bash
  git whatchanged
```

#### Mostra o que foi alterado
``` bash
  git whatchanged -p
```
#### Mostra os repositórios remotos
``` bash
  git remote
  git remote add origin https://github.com/jp17paulo/curso-git.git
```
#### Enviando para o repositório remoto
``` bash
  git push origin master
```
#### Clonando um repositório
``` bash
  git clone https://github.com/jp17paulo/curso-git.git
```
# 4 - Organização do trabalho com branches

#### Criando branch
``` bash
   git branch design
```

#### Enviando para o repositório remoto
``` bash
   git push -u origin design
```

#### Mostra branchs locais
``` bash
  git branch
```

#### Mostra branchs remotas
``` bash
  git branch -r
```

#### Cria uma branch local já trackeada com a branch remota
``` bash
  git branch -t design origin/design
```

# 5 - Resolução de conflitos
#### Atualiza o arquivo com alterações no mesmo de usuários diferentes (merge)
###### Obs: Caso as alterações tenham sido efetuadas no mesmo local irá aparecer mensagem de conflito ainda e o mesmo deverá ser resolvido, escolhendo no arquivo o que deverá ser mantido.
``` bash
   git pull
```
# 6 - Boas práticas no uso do Git

#### Cria e já entra na branch
``` bash
   git checkout -b desenvolvimento
```

#### Pega o conteúdo da branch desenvolvimento e incorpora na branch atual
``` bash
   git merge desenvolvimento
```

#### Atualiza a branch desenvolvimento com base na branch master
``` bash
   git rebase master desenvolvimento
```

#### Caso tenha conflitos, resolver, após resolver executar os comandos:
``` bash
   git add proposta_1.html
   git rebase --continue
```

# 7 - Controle avançado de alterações
#### Retorna a branch para o estado anterior
``` bash
  git checkout proposta_1.html
```
#### Altera o estado atual da branch para o commit mais recente
``` bash
  git reset HEAD proposta_1.html
```
#### Desfazer um commit 
``` bash
  git reset b1a8fc958a5d9ed72249426071ae08d76dfe49f9
```
#### Desfazer alterações de um commit antigo (isso vai gerar um novo log referente as alterações descartadas)
``` bash
  git revert 2d5cb01e44cbcebaabe743d338e94a1ce6567413
```

#### Armazena as informações não comitadas
``` bash
  git stash
```

#### Exibe o conteúdo do stash
``` bash
  git stash list
```

#### Retoma o último registro do stash
``` bash
  git stash pop
```

#### Retoma um registro específico do stash
``` bash
  git stash apply stash@{0}
```

#### Apagar stash
``` bash
  git stash drop
```

#### Git bisect para procurar commits a serem desfeitos
``` bash
  git bisect start
  git bisect bad HEAD
  git bisect good b1a8fc958a5d9ed72249426071ae08d76dfe49f9

```

#### Vai retornando commits (Até mostrar a alteração que estamos procurando)
``` bash
  git bisect bad
```

#### Avança commits (Até mostrar a alteração que estamos procurando)
``` bash
  git bisect good
```
# 8 - Contribuição com opensource, técnicas avançadas e produtividade com o Git

#### Criar alias
##### Obs: No arquivo ficará assim:
###### [alias]
###### st = status
###### co = checkout

###### envia = !git checkout master && git pull checkout desenvolvimento && git rebase master && git checkout master && git merge desenvolvimento && git push
``` bash
  vim ~/ .gitconfig
```

#### Ver um commit por linha
``` bash
  git log --pretty=oneline
```

#### Não mostra a data do commit
``` bash
  git log --pretty=short
```

#### Também mostra o autor do commit original
``` bash
   git log --pretty=full
```

#### Personalizando o git log
``` bash
   git log --pretty='%an realizou o commit %h: %s'
```

#### Mostra a diferença nos arquivos alterados
``` bash
   git log -p
```

#### Mostra a diferença nos arquivos alterados de uma forma mais resumida
``` bash
   git log --stat

```

#### Mostra alterações do repoitório remoto
``` bash
   git fetch 
```

#### Mostra a diferença entre as branchs
``` bash
   git diff desenvolvimento/master
```

#### Incluindo alterações da branch desenvolvimento para a master
``` bash
    git merge desenvolvimento/master
```

#### Mostra graficamente os caminhos do arquivo
``` bash
   git log --graph
```
# 9 - Fazendo merges avançados com Cherry Pick

####
``` bash

```

####
``` bash

```

####
``` bash

```

####
``` bash

```

# 10 - Usando Git através de interfaces visuais

####
``` bash

```

####
``` bash

```

####
``` bash

```

####
``` bash

```


