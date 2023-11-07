
# Versionamento de Código com Git e GitHub
Anotações sobre o curso Versionamento de Código com Git e GitHub realizado pela instrutora [Elidiana Andrade](https://github.com/elidianaandrade) através da [Digital Innovation One](https://www.dio.me/).

## Afinal o que é GIT?

O Git é um Sistema de Controle de Versão Distribuído, sendo gratuito e Open Source (Código aberto), possuindo ramificações (Branching) e fusões(Merging) eficientes tornando-o leve e rápido.
É usado principalmente por desenvolvedores de software para acompanhar as alterações no código-fonte de seus projetos. Funciona como um "salvamento automático" para o código. Em vez de salvar apenas a versão atual do projeto, o Git armazena todas as versões anteriores, permitindo que você volte no tempo para qualquer ponto e veja ou restaure o código daquele momento.
Sendo útil para colaboração em equipe, acompanhamento de alterações, experimentação sem medo de perder o trabalho e correção de erros, entre outras coisas. O Git também permite que você trabalhe em seus projetos localmente em seu computador e, em seguida, compartilhe as alterações com outras pessoas usando serviços de hospedagem, como o GitHub.

## O que é GitHub?

O GitHub é uma plataforma online que simplifica o desenvolvimento de software colaborativo. Ele oferece um lugar para hospedar, compartilhar e colaborar em projetos de código aberto. Desenvolvedores podem acompanhar alterações, resolver problemas e colaborar usando o Git, um sistema de controle de versão. É usado para projetos públicos e privados, tornando-o essencial para o desenvolvimento de software em equipe. Organizações e desenvolvedores individuais utilizam o GitHub para gerenciar e compartilhar seu código-fonte de forma eficaz, promovendo a colaboração e o controle de versões.


## Comandos do Git
Após ter baixado o git em sua máquina, pode-se seguir alguns passos para configurar o git.

### - Configurações iniciais do Git

configurando nome de usuario e email (globalmente):
```bash
$ git config --global user.name "Nome sobrenome"
```
```bash
$ git config --global user.email seuemail@email.com
```
Configurando o nome da Branch padrão para main:

```bash
$ git config --global init.defaultBranch main
```

### - Armazenando Credenciais
Você pode armazenar suas credenciais para reduzir o número de vezes em que se digita o nome de usuário e senha.

Salvando no cache:

```bash
$ git config --global credential.helper cache
```

Ou salvando permanentemente:

```bash
$ git config --global credential.helper store
```
Documentação: [https://git-scm.com/book/pt-br/v2/Git-Tools-Credential-Storage](https://git-scm.com/book/pt-br/v2/Git-Tools-Credential-Storage).

### - Criando um repositório local

Acesse a pasta que deseja transformar em um repositório Git pelo terminal ou clique no atalho em "Git Bash Here":

Inicialize um repósitório Git no diretório escolhido:
```bash
$ git init
```

Conecte o repositório local com o repositório remoto:
```bash
$ git remote add origin https://github.com/username/nome-do-repositorio.git
```

### - Clonando um repositório

Para clonar um repositório no Git, acesse seu repositório no GitHub e siga os passos.

Em "Code", copie o código HTTPS ou SSH (dependendo de como autenticou sua conta) do repositório no GitHub.

Abra o GitBash e insira o camando git clone e depois cole o código copiado:

```bash
$ git clone https://github.com/username/nome-do-repositorio.git
```
### - Salvando alterações no repositório local

Criando um commit.

Adicione o conteúdo que deseja inserir no commit:
```bash
$ git add nome-do-arquivo-que-deseja-add
```

Caso deseje adicionar todas as alterações realizadas no projeto basta usar o comando:

```bash
$ git add .
```
Crie um commit e adicione uma mensagem descritiva entre as aspas, que é um breve resumo do que você fez no commit:

```bash
$ git commit -m "mensagem"
```

### - Desfazendo alterações no repositório local

Alterando a mensagem do ultimo commit:

```bash
$ git commit --amend
```

Alterando a mensagem sem abrir o editor:

```bash
$ git commit --amend -m "nova mensagem"
```

### - Desfazendo alterações no repositório local
O git reset é útil para corrigir erros, reorganizar commits e ajustar o histórico do Git, mas pode causar perda de dados se não for usado corretamente.

Desfazendo um commit:

```bash
$ git reset
```
Esse comando desfaz commits, mas mantém as alterações preparadas para um novo commit, não apaga nada:
```bash
$ git reset --soft
```
Desfazer commits e preparar as alterações para um novo commit:
```bash
$ git reset --mixed
```
Desfaz completamente commits e descarta as alterações.
```bash
$ git reset --hard
```


### - Enviando alterações para o repositório remoto

Esse comando envia as alterações do repositorio local para o remoto:

```bash
$ git push
```

"Puxar" as alterações do repositório remoto para o local (busca e mescla):

```bash
$ git pull
```

### - Trabalhando com Branches

Trocar de Branch e criar uma nova:

```bash
$ git checkout -b nova-branch
```

Deletar uma Branch

```bash
$ git branch -d nome-da-branch
```

Ver o último commit de cada Branch:

```bash
$ git branch -v
```

## Referências

 - [Digital Innovation One](https://www.dio.me/)
 - [Elidiana Andrade](https://github.com/elidianaandrade/dio-curso-git-github)
 - [GIT. Documentation](https://git-scm.com/doc)
 - [GITHUB. Documentation](https://docs.github.com/pt)

