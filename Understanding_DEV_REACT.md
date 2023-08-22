# ANOTAÇÕES DE AULA 
## CURSO DEV_REACT / ENTRA21-2023

## Autor: Edson Luiz Morais

### GIT E GITHUB

- Inicialmente, deve-se ter o Git instalado na máquina.  
- No Windows Explorer, deve-se ir até o diretório onde ficarão os arquivos do repositório local.
- Na guia onde consta o caminho do diretório, digitar 'cmd'.
- Isso fará com que abra o Command do Windows, já ná pasta selecionada, sem a necessidade de navegar até a mesma com comandos de diretório (cd).

#### Resumo dos principais comandos do Git:
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



### MARKDOWN

#### Cabeçalhos
      h1 # ... até  h6 ######  


- parágrafos são separados por uma linha em branco
- quebra de linha, 2 espaços em branco no fim da linha

#### Texto com ênfase
*itálico* ou _itálico_  
**negrito** ou __negrito__  
``````tachado``````  
´´´tachado´´´  

#### Listas não ordenadas
- item a
- item b
    - sub item b1
        - sub sub item b1a

#### Listas ordenadas
2. primeiro item
2. segundo item
2. terceiro item
começa de acordo com o número do primeiro item

#### Lista de tarefas
- [X] tarefa 1
- [ ] tarefa 2
- [X] tarefa 3

#### Link
[texto do Link1](http://example.com/ "Propriedade title, opcional")  
<a href="http://example.com/" title ="Propriedade title, opcional" >Texto do link2</a>

#### Imagem
![Calculadora Windows](/assets/calculadora.png "Foto da Calculadora Win...")

#### Vídeo
[![Vídeo Markdown - YouTube]](https://youtu.be/vZaldeUg6D0)

#### Trecho de código
```
   if var > 0 then 
        display "Valor positivo"
   else
        display "Valor Negativo"
   and-if 
```

#### Tabela
Cod | Nome  | Nota | Aprov 
--- |:-----:|-----:|----
1   |Paulo  |6,0   | não
2   |Joana  |7,3   | sim


#### Emoji

##### VSCode
- Apenas dar copiar e colar emojis da Emojoipedia;

https://emojipedia.org/

🧐

##### GitHub
- Apenas usar os comandos demonstrados nesta pagina:

https://gist.github.com/rxaviers/7360908

:blush:  
:smirk:

