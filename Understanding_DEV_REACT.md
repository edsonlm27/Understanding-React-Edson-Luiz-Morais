# ANOTAÇÕES DE AULA

## CURSO DEV_REACT / ENTRA21-2023

## Autor: Edson Luiz Morais

### GIT E GITHUB

- Inicialmente, deve-se ter o Git instalado na máquina.
- No Windows Explorer, deve-se ir até o diretório onde ficarão os arquivos do repositório local.
- Na guia onde consta o caminho do diretório, digitar 'cmd'.
- Isso fará com que abra o Command do Windows, já ná pasta selecionada, sem a necessidade de navegar até a mesma com comandos de diretório (cd).

#### Resumo dos principais comandos do Git:

https://www.freecodecamp.org/portuguese/news/10-comandos-do-git-que-todo-desenvolvedor-deveria-conhecer/

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
- git restore --staged <file>
  - para retornar de tracked para unstaged
- git commit -m "mensagem"
  - para fazer o commit no arquivo e gerar uma nove versão do mesmo; utilizar uma mensagem que traga uma fácil identificação da alteração.
- git config -global user.name (nome)
  - configurar o nome
- git config -global user.email (email)
  - configurar o email
- git push / enviar o conteúdo do repositório local para o repositório remoto
  - git push -u origin <nome-da-branch>
- git pull
  - atualizar o conteúdo do repositório remoto para o repositório local
- git log --oneline
  - mostra no log o histórico de commits
- git revert / desfazer as alterações em nosso espaço de trabalho local ou remotamente
  - git revert 3321844 (código hash ao lado do commit que desejamos desfazer)
- git clone (link) / efetuar o clone do repositório remoto para o repositório local
  - git clone <https://link-com-o-nome-do-repositório>
- git branch / criar, listar e excluir branches
  - git branch <nome-da-branch> / criar uma branch
  - git push -u <local-remoto> <nome-da-branch> / fazer o push da nova branch para o repositório remoto
  - git branch ou git branch --list / ver as branches
  - git branch -d <nome-da-branch> / excluir uma branch
- git checkout / trocar de uma branch para outra
  - git checkout <nome-da-branch> / fazer o checkout de arquivos e commits
  - git checkout -b <nome-da-branch> / criar e automaticamente trocar para a branch criada ao mesmo tempo
- git merge / unir a branch com a branch pai (dev ou master/main)

### MARKDOWN

#### Cabeçalhos

      h1 # ... até  h6 ######

- parágrafos são separados por uma linha em branco
- quebra de linha, 2 espaços em branco no fim da linha
- evitar usar símbolo da tag <a> com conteúdo dentro (não aparece)

#### Texto com ênfase

_itálico_ ou _itálico_  
**negrito** ou **negrito**  
`tachado`  
´´´tachado´´´

#### Listas não ordenadas

- item a
- item b
  - sub item b1
    - sub sub item b1a

#### Listas ordenadas

2. primeiro item
3. segundo item
4. terceiro item
   começa de acordo com o número do primeiro item

#### Lista de tarefas

- [x] tarefa 1
- [ ] tarefa 2
- [x] tarefa 3

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

| Cod | Nome  | Nota | Aprov |
| --- | :---: | ---: | ----- |
| 1   | Paulo |  6,0 | não   |
| 2   | Joana |  7,3 | sim   |

#### Emoji

##### VSCode

- Apenas dar copiar e colar emojis da Emojipedia;

https://emojipedia.org/

🧐

##### GitHub

- Apenas usar os comandos demonstrados nesta pagina:

https://gist.github.com/rxaviers/7360908

:blush:  
:smirk:

## HTML

- Linguagem de marcação, fazendo uso de várias tags.
- Atualmente na versão 5.
- Utilizada em conjunto com CSS e JavaScript.
- Recomendável seguir uma estrutura básica:

```
<!DOCTYPE html>
<html>

<head>

  <style>
      (CSS)
  </style>
</head>

<body>
  <header>
  </header>
  <main>
  </main>
  <footer>
  </footer>
    <script>
        (JavaScript)
    </script>
</body>

</html>
```

- Algumas tags podem fazer uso de atributos, obrigatórios e opcionais.
- Algumas tags precisam da tag de fechamento </html>, outras não.

## CSS

- CSS, ou Cascading Style Sheets, são folhas de estilo em cascata, para formatar a apresentação dos documentos de marcação, layout, animações, efeitos.
- Atualmente na versão 3.
- Utilizada em conjunto com HTML e JavaScript.
- Pode ser aplicado de três maneiras:

1.       CSS inline: estilos aplicados diretamente em um elemento HTML, dentro do documento.

```
<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">Este é um parágrafo.</p>
```

2.       CSS Interno/Incorporado: o elemento style permite aplicar várias regras de uma vez no próprio documento HTML

```
<head>
<style>
body {
    background-color: green;
}

h1 {
    color: brown;
    margin-left: 40px;
}
</style>
</head>
```

3.       CSS Externo: um documento com extensão .css permite aplicar regras a um website inteiro de uma vez.

```
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
```

- Os estilos cascateados possuem prioridade de cascateamento:

  - estilo embutido dentro de um elemento html
  - folhas de estilo internas e externas (na seção principal)
  - padrão do navegador

- Seletores utilizados para serem aplicados ao html:
  - simples: universal(\*), tag(p), id(#), classe(.)
  - combinadores: espaço em branco, ">" e "+"
  - de pseudoclasse: :active :focus :hover
  - de pseudoelementos: :first-line :first-letter
  - de atributos: [att~=val] [att|=val]

**Observação:**

- Seletores mais específicos se sobrepõem aos menos específicos

- Diversas aplicações do CSS:

  - Cor
  - Texto
  - Fonte
  - Background
  - etc

- Display: flex / grid

## Lógica de Programação

- Técnica de encadear pensamentos para atingir um determinado objetivo, em uma sequência lógica.

### Algoritmo

- Sequência finita de passos que levam à execução de uma tarefa.

#### Formas de representar um algoritmo

- descritivo
- fluxograma (início, fim)
- pseudo-código algoritmo em tópicos início, fim (com indentação)
- notação matemática (expressões)

#### Sugestões

- somente um verbo por frase
- frases em 3a pessoa (infinitivo)
- ser objetivo
- evitar palavras com sentido dúbio

#### Fases do algoritmo

- entrada de dados
- processamento
- saída de dados

## JavaScript (JS)

- JavaScript é uma poderosa linguagem de programação que pode adicionar interatividade a um site.
- A linguagem JS é fracamente tipada, e é aplicada juntamente com HTML e CSS.
- As variáveis JS podem ser declaradas:
  - automaticamente, onde o tipo é definido por inferência
  - usando let (escopo local)
  - usando var (escopo global)
  - const (valor constante, que não pode ser alterado)
- OBS: As palavras reservadas não podem ser usadas como nomes de variáveis.
- Utilizar camelCase para nomear as variáveis com mais de uma palavra.
- Comentários:

  ```
  // comentário de linha única

  /*  comentário
          de várias
  /*  linhas
  ```

- como aplicar o JS:

1.       JS Interno/Incorporado: o elemento script permite aplicar JS no próprio documento HTML

    ```
    <!DOCTYPE html>
    <html>
    <body>
    <h2>Demo JavaScript in Body</h2>
    <p id="demo">A Paragraph</p>
    <button type="button" onclick="myFunction()">Try it</button>
    <script>
        function myFunction() {
            document.getElementById("demo").innerHTML = "Paragraph changed.";
        }
    </script>
    </body>
    </html>
    ```

2.       arquivo JS Externo: um documento com extensão .js permite aplicar regras a um website inteiro de uma vez.
    ```
    <head>
        <script src="script.js"></script>
    </head>
    ```

### Operadores Relacionais

- atribuição (=)
- igualdade (==) considera o valor, desprezando o tipo
- igualdade estrita (===) considera também o tipo
- diferente de (!=), (!==)
- menor que (<)
- menor ou igual (<=)
- maior que (>)
- maior ou igual (>=)

### Operações Lógicas

- and (&&)
- or (||)
- not

#### Operações lógicas bit-a-bit

- var num = 9 & 3
- var num = 9 | 3

### Tipos de dados (5)

- string - 'texto entre aspas simples' ou "aspas duplas" "123"  
   Existem 3 formas de declarar Strings: Aspas duplas, aspas simples e templateLiterals -
  Crases (facilita quebra de linha)

- number - Sem o uso de aspas (27) (34.57) / em JS todos os números são number, tanto inteiros quanto decimais  
   Também são number: +Infinity, -Infinity, NaN (typeof)  
   Double precision 64-bit binary format IEEE 754 (Acontecem algumas imprecisões de arredondamento)  
   https://0.30000000000000004.com/ console.log(.1 + .2);  
   The decimal.js library provides an arbitrary-precision Decimal type for JavaScript
- boolean - true ou false
- Object - carregam alguns métodos
- function  
  O JavaScript trata os valores de string vazia, o number 0, undefined, false e null como valores falsos (falsy)  
  Todos os demais valores são tratados como valores verdadeiros (truthy)

### Tipos especiais de dados (2)

- null (existe, mas tem uma ausência de valor e não a inexistência de propriedade)
- undefined (ausência de declaração, inexistência de definição (ela nem existe))

### Tipos de Objetos (6)

- Object
- Date
- Array
- Number
- String
- Boolean

### Operadores para testar tipos de dados

- typeOf
- isNaN (Not a Number)

### Conversão Explícita no JS

#### Para string

- variavel = String(12345)
- x.toFixed(2)
- x.toExponential(3)
- x.toPrecision(4)

#### Para number

- Number('765')
- Number(true)
- parseFloat("10.5")
- parseInt("10.5")

#### Para boolean

- Forma simples de converter para boolean, negar 2 vezes – o vazio é convertido para false  
   console.log(!!"")
  Se preencher, converte para true - console.log(!!"abc")  
   Se escrever true, é true - console.log(!!"true")  
   Se escrever false, é true - console.log(!!"false")  
   Não converte explicitamente, verifica se tem algum valor  
   Se colocar um espaço (que é um caracter), já considera preenchido

### Operações Aritméticas

- soma (+)
- subtração (-)
- multiplicação (\*)
- divisão (/)
- resto da divisão (%)
- potenciação (\*\*)
- radiciação (sem símbolo) / usar inverso da potenciação / x = num \*\* (1/raiz)
- também temos a biblioteca Math (PI, pow, sqrt, cbrt, random(), ...)
- maneiras diferentes de escrever as operações:
  - a = a + 1 ==> a += 1 (ou ainda a++)
  - x = x _ 10 ==> x _= 10
  - y = y / 2 ==> y /= 2
  - k = k - 5 ==> k -= 5 (k--, diminui 1)

#### Notação exponencial

- var numExponencial = 2e3

#### Biblioteca Math

- Math.PI
- Math.pow(5, 6)
- Math.sqrt(25)
- Math.cbrt(27)
- Math.random()

##### Gerando números Pseudo-Aleatórios entre 0 e 10:

- numRand = parseInt(Math.random() \* 10)

### Bases numéricas

- hexadecimal (0xf)
- octal (0o7)
- binário (0b1)

### Manipulação do DOM (Document Object Model)

#### Capturando Elementos

- input type="text"  
  texto = document.getElementById("idTexto").value  
  texto2 = document.querySelector("#idTexto").value  
  texto3 = document.querySelectorAll(".inputTexto")

- input type="number"  
  numero = Number(document.getElementById("idNumero").value)

- input type="checkbox"  
  opcao1 = document.getElementById("idOpcao1").checked // retorna um boolean

- input type="radio"  
  masculino = document.getElementById("idMasculino").checked // retorna um boolean  
  capturando o radio selecionado:  
  sexo = document.querySelector("input[name=nmGenero]:checked").value

### Variáveis

- var (permite redeclaração e reatribuição)  
   (O var "vaza" escopos por conta do hoisting(execeto o escopo de função))  
   (sempre se mantém no escopo global ou no escopo de função; ele sofre o hoisting até o escopo mais próximo de uma função ou até o escopo mais próximo global que tiver)
- let (permite somente reatribuição)  
   (se restringe a qualquer tipo de bloco, seja uma função, um bloco if, um bloco while, for, ...)  
   (sofre o hoisting até o escopo do bloco, e não até o escopo global)
- const (não permite redeclaração nem reatribuição)  
   (se restringe ao escopo de bloco, e deve ser obrigatoriamente inicializada na declaração)
- hoisting (joga a declaração para cima, mas mantém a atribuição no mesmo lugar)

### Processamento Assíncrono

- JS: assíncrono, IO não bloqueante, single thread
- setInterval() / clearInterval(): set, executa uma determinada tarefa de tempos em tempos
- setTimeout() / clearTimeout(): executa uma função (pode ser nomeada ou anônima) após um determinado tempo

#### AJAX (Asynchronous JavaScript and XML)

- fazer uma requisição https para consumo de API (var xhr = new XMLHttpRequest - construtor)
- Métodos:
  - xhr.open(), prepara a requisição (passa o método - get, post, put, delete, ...)
  - xhr.addEventListener / load, escutar o retorno da requisição
  - xhr.send(), dispara a requisição
- retorna um json, xml, csv
- JSON.parse(enderecoJSON) para transformar em JS Object
- Para transformar um JS Object para JSON, usa-se o JSON.stringify(enderecoOBJ)
- resposta: xhr.responseText
- consultar a documentação da API (WebService) / O método depende do servidor (o viacep só aceita GET)
- O AJAX é uma forma mais antiga de trabalhar

#### FETCH (async await)

- O fetch API é um método do navegador, faz parte do DOM; não precisa colocar o GET (é o padrão dele); não retorna a resposta do servidor, e sim uma promise
  - async function()
  - await
  - return resposta.json()
- Promise: técnica para trabalhar com processamento assíncrono; esse objeto espera a resposta do servidor; tem 4 estados(pending, fullfilled ou resolved, rejected, settled)
- Com o await, fica esperando a promise mudar de estado(sair de pending), e pega os dados vindos do servidor
- Para ficar esperando, precisa do async na function
- O JSON já extrai o JS Object (o .json também retorna uma promise)
- Em arrow function, usa async await também.

### Bootstrap

- site: getbootstrap.com (oficial)
- w3schools.com/bootstrap

#### Bootstrap CDN (Content Delivery Network)

- CSS https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css
- JS https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js

#### Lembretes

- se configurar CSS próprio, este deve estar abaixo do css do bootstrap (última coisa a ser declarada)
- colocar tudo dentro de container (div, section, main, ...)
- escolher um container (-sm, -md, -lg, -xl, -xxl, -fluid)
- O simples fato de usar um container já o torna responsivo (mobile first)
- A ordem das classes do Bootstrap não importa
- Algumas classes: text, bg (background colors), border, shadow

### JSON (JavaScript Object Notation)

- formatação utilizada para estruturar dados em formato de texto e transmiti-los de um sistema para outro
- JSON => JS  
  vem no formato string, para usar no código: json.parse()
- JS => JSON  
  converter para string: json.stringify()
- Regras de sintaxe:
  - Os dados são em pares nome:valor
  - O nome é uma string, mas o valor pode ser qualquer tipo de dado
  - Dados são separados por vírgula
  - Chaves guardam objetos, colchetes guardam arrays
  - É necessário usar aspas duplas

### NODE

- Modules: require("") / module.exports
- node server.js
- nodemon server.js

#### npm (Node Package Manager)

- express, framework para o Node.js

#### Síntese de Comandos

- npm -v  
  verificar a versão instalada
- npm init
  iniciar um projeto Node; cria o arquivo package.json (inserção de variáveis) - npm init -y  
   inicializa as variáveis com valores default, não solicita preenchimento
- npm install express --save  
  instala o pacote express; cria o arquivo package-lock json e pasta node_modules
- npm install nodemon -g  
  instala o nodemon globalmente, e não só no projeto

#### instalar dependências

- npm i express --save
- npm i cors
- npm i body-parser

```
"dependencies": {
    "body-parser": "^1.20.2",
    "cors": "^2.8.5",
    "express": "^4.18.2"
  }
```

#### scripts para startar

- npm run dev
- npm run test
- npm run start

```
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node server.js",
    "dev": "nodemon server.js"
  }
```

### JWT (Json Web Token)

- é uma dependência externa, precisa ser importada, pelo npm install
- composto por 3 strings codificadas (cabeçalho, payload e token, com tempo de expiração)
- SECRET é uma senha que fica gravada no servidor
- no logout, jogar esse token em uma black-list – um array de tokens inválidos
- a Black-list deve estar no escopo global do servidor
- pode testar usando Insomnia, Postman, ...

### Armazenamento no navegador (variáveis - converter para json)

- json.parse, pegar um json e passar para JS obj
- json.stringify (converter para json)
- localStorage
  - localStorage.setItem("inventor", inventorJSON)
  - localStorage.getItem("inventor")
  - localStorage.removeItem("inventor")
- sessionStorage (sessionStorage funciona da mesma maneira, porém ele existe só enquanto o naveg estiver aberto; fechou o navegador, limpa automaticamente)
- cookies (tem mais detalhes)
- Storage e o cookies pode guardar no frontEnd
