# webfrontend-2025-3-semana-git-e-github-extra

### Desafio Git Rebase - Hacker Edition 🚀
#### Desafio: Domine o Git Rebase
# TESTANDO O DESAFIO #

Neste desafio, o seu objetivo é aprender a utilizar o `git rebase` de forma eficaz, reordenando commits para manter o histórico de commits limpo e linear. Vamos simular uma situação comum em projetos colaborativos, onde você terá que reorganizar seus commits antes de enviar suas alterações para o repositório remoto.

## Cenário do Desafio
Você está trabalhando em uma feature importante e criou vários commits para salvar seu progresso. No entanto, antes de enviar suas alterações para o repositório remoto, você percebe que seu histórico de commits está desorganizado ou contém commits irrelevantes. Seu objetivo é utilizar o git rebase para melhorar a clareza e a organização do histórico de commits.

Etapas do Desafio:

## 🔗[O que é rebase](https://www.atlassian.com/br/git/tutorials/rewriting-history/git-rebase)


### Passo 1: Criação do Ambiente
Clone o repositório de teste:

Se você já possui um repositório local, vá para a pasta do repositório. Caso contrário, clone o repositório:

~~~javascript
git clone <URL_DO_REPOSITORIO>
~~~

Crie uma nova branch:

Como boa prática, crie uma nova branch para realizar suas alterações:


~~~javascript
git checkout -b minha-feature
~~~


### Passo 2: Crie Vários Commits

Faça algumas alterações nos arquivos do projeto e crie vários commits. Exemplo:

Faça uma alteração no arquivo README.md e crie um commit:

~~~javascript
git add .
git commit -m "Primeira alteração no README"
~~~


#### Faça uma segunda alteração em outro arquivo e crie outro commit:

~~~javascript
git add .
git commit -m "Segunda alteração no outro arquivo"
~~~


#### Faça mais uma terceira alteração em qualquer arquivo e crie um commit:

~~~javascript
git add .
git commit -m "Terceira alteração no terceiro arquivo"
~~~


Agora você tem três commits que podem ser reordenados, modificados ou combinados.

### Passo 3: Reordenando Commits com Git Rebase

Agora que você tem alguns commits no seu histórico, vamos começar a reorganizá-los usando `git rebase`.

Verifique o histórico de commits:

Veja os commits que você acabou de criar:

~~~javascript
git log --oneline
~~~


Inicie o rebase interativo:


Use o comando abaixo para iniciar o rebase dos últimos três commits:

~~~javascript
git rebase -i HEAD~3
~~~


Reorganize ou combine os commits:

No editor que abrir, você verá algo como:

~~~javascript
pick 1a2b3c4 Primeira alteração no README
pick 5d6e7f8 Segunda alteração no outro arquivo
pick 9g0h1i2 Terceira alteração no terceiro arquivo

~~~

Agora, você pode:

- Reordenar: Mova os commits para a ordem desejada.
- Unificar: Deixar todas as alterações em um unico `commit`



Envie as alterações:
~~~javascript
git push origin minha-feature --force
~~~

#### Dicas:

Use git rebase -i para sempre revisar e organizar seus commits antes de enviar para o repositório remoto.
Caso você precise abortar o rebase, use git rebase --abort para voltar ao estado anterior.
O rebase é ideal para manter o histórico limpo, mas em equipes grandes, tenha cuidado com o --force para não sobrescrever mudanças importantes.
Agora é sua vez! Use o git rebase para manter seu histórico de commits limpo e organizado. Isso será essencial para manter a qualidade do seu trabalho em projetos colaborativos maiores. Boa sorte! 💻
