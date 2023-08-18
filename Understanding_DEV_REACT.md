# ANOTAÇÕES DE AULA DE GIT E GITHUB

## Autor: Edson Luiz Morais  / Curso Entra21-2023

- Inicialmente, deve-se ter o Git instalado na máquina.  
- No Windows Explorer, deve-se ir até o diretório onde ficarão os arquivos do repositório local.
- Na guia onde consta o caminho do diretório, digitar 'cmd'.
- Isso fará com que abra o Command do Windows, já ná pasta selecionada, sem a necessidade de navegar até a mesma com comandos de diretório (cd).

### Resumo dos principais comandos do Git:
- git --version
    - apresenta a versão instalada do Git.
- git init
    - para inicializar o Git na referida pasta.
- git status
    - verificar o status dos arquivos (untracked, tracked, ...).
- git add <filename>
    - para alterar o status do arquivo para 'tracked'.
- git add .
    - para alterar o status de todos os arquivos para 'tracked'.
- git commit -m "mensagem"
    - para fazer o commit no arquivo e gerar uma nove versão do mesmo; utilizar uma mensagem que traga uma fácil identificação da alteração.
- git config -global user.name <nome>
    - configurar o nome
- git config -global user.email <email>
    - configurar o email
- git log --oneline
    - mostra no log o histórico de commits
- git push 
    - enviar o conteúdo do repositório local para o repositório remoto
- git pull
    - atualizar o conteúdo do repositório remoto para o repositório local
- git clone <link>
    - efetuar o clone do repositório remoto para o repositório local
