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
``` bash

```

# 7 - Controle avançado de alterações
``` bash

```

# 8 - Contribuição com opensource, técnicas avançadas e produtividade com o Git
``` bash


```

# 9 - Fazendo merges avançados com Cherry Pick
``` bash


```

# 10 - Usando Git através de interfaces visuais
``` bash


```


