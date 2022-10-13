# Git Workshop
Habilidades básicas para aumentar a chances de manter sua sanidade mental ao trabalhar com Git e economize tempo.

O objetivo desse workshop é apresentar um fluxo de trabalho básico que você encontrará na maioria dos projetos (com algumas variações).

Bom, agora que você é parte do time responsável por este repositório, vamos começar a trabalhar.

### Clone esse repositório
```sh
git clone git@github.com:projeto-ifpb/git-workshop.git
```

### Crie uma branch no seguinte formato: `feature/SEU_NOME`
```sh
git checkout -b feature/SEU_NOME
```

### Abra o arquivo `index.html` e adicione seu nome na lista

### Adicione o arquivo modificado ao stage
```sh
git add -p index.html # -p para adicionar as alterações parciais
```

### Escreva a mensagem do commit
```sh
git commit -m "adiciona MEU_NOME na index"
```

### Agora faça do jeito certo
```sh
git commit --amend -m "chore: adds my name to list"
# ou
git commit --amend
```


### Faça um push da sua branch para o repositório na "origem"
```sh
git push origin feature/SEU_NOME
```
Agora seu código está no repositório remoto, mas não na branch principal.

### O bom código é revisado
- Abra um pull request para a branch `main` do repositório original
- Envie o link do pull request para seus colegas para que eles possam revisar seu código
- Aguarde a revisão e possível seu pull request
- Agora temos dois caminhos possíveis:
    - [Rebase](#rebase)
    - [Merge](#merge)

### Rebase
Após a aprovação, faça o rebase da branch `main` na sua branch.
O Rebase consiste em pegar as alterações da branch `main` e aplicar na sua branch.
Basicamente pegar um conjunto de commits e juntar com outro conjunto de commits.
```sh
git checkout main # Vá para main
git pull origin main # Atualize o código local
git checkout feature/SEU_NOME # Volte para sua branch
git rebase main # Rebase
git push --force-with-lease origin feature/SEU_NOME # Atualizando sua branch remota
```

### Merge
Após a aprovação, faça o merge da sua branch na branch `main`.
O Merge consiste em pegar as alterações da sua branch e aplicar na branch `main`.
A principal diferença entre o rebase e o merge é que o merge cria um novo commit.


## E agora?
Isso aqui é o mínimo que você precisa saber para começar a trabalhar com Git, mas não é o suficiente para todos os casos. É importante que você aprenda o que faze outros comandos como:

- git init
- git reset --soft
- git reset --hard
- git set remote
- git stash
- git cherry-pick
- git rebase -i
- git merge --squash

Bom, se você tiver paciência recomendo que você acesse a documentação oficial do Git e leia os tutoriais disponíveis.