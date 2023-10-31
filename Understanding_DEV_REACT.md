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
- git config -global user.name (nome)
    - configurar o nome
- git config -global user.email (email)
    - configurar o email
- git log --oneline
    - mostra no log o histórico de commits
- git push 
    - enviar o conteúdo do repositório local para o repositório remoto
- git pull
    - atualizar o conteúdo do repositório remoto para o repositório local
- git clone (link)
    - efetuar o clone do repositório remoto para o repositório local




### MARKDOWN

#### Cabeçalhos
      h1 # ... até  h6 ######  


- parágrafos são separados por uma linha em branco
- quebra de linha, 2 espaços em branco no fim da linha
- evitar usar símbolo da tag <a> com conteúdo dentro (não aparece)

#### Texto com ênfase
*itálico* ou _itálico_  
**negrito** ou __negrito__  
```tachado```  
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
1. 	CSS inline: estilos aplicados diretamente em um elemento HTML, dentro do documento.
```
<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">Este é um parágrafo.</p>
```

2. 	CSS Interno/Incorporado: o elemento style permite aplicar várias regras de uma vez no próprio documento HTML
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
</>
</head>
```

3. 	CSS Externo: um documento com extensão .css permite aplicar regras a um website inteiro de uma vez.
```
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
```

- Os estilos cascateados possuem prioridade de cascateamento:
    * estilo embutido dentro de um elemento html
    * folhas de estilo internas e externas (na seção principal)
    * padrão do navegador

- Seletores utilizados para serem aplicados ao html:
    * simples: universal(*), tag(p), id(#), classe(.)
    * combinadores: espaço em branco, ">" e "+"
    * de pseudoclasse:  :active  :focus  :hover
    * de pseudoelementos:  :first-line   :first-letter
    * de atributos:  [att~=val]  [att|=val]

**Observação:**
- Seletores mais específicos se sobrepõem aos menos estpecíficos

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
- fluxograma	(início, fim)
- pseudo-código		algoritmo em tópicos	início, fim (com indentação)
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
### Operadores Relacionais
- atribuição (=)
- igualdade (==)  considera o valor, desprezando o tipo  
- igualdade estrita (===)  considera também o tipo
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
- string  - 'texto entre aspas simples' ou "aspas duplas" "123"  
    Existem 3 formas de declarar Strings: Aspas duplas, aspas simples e templateLiterals - 
    Crases (facilita quebra de linha)

- number  -  Sem o uso de aspas (27) (34.57) / em JS todos os números são number, tanto inteiros quanto decimais  
    Também são number: +Infinity, -Infinity, NaN (typeof)  
    Double precision 64-bit binary format IEEE 754 (Acontecem algumas imprecisões de arredondamento)  
    https://0.30000000000000004.com/  console.log(.1 + .2);  
    The decimal.js library provides an arbitrary-precision Decimal type for JavaScript
- boolean -  true ou false 
- Object - carregam alguns métodos
- function  
O JavaScript trata os valores de string vazia, o number 0, undefined, false e null como valores falsos (falsy)  
Todos os demais valores são tratados como valores verdadeiros (truthy)


### Tipos especiais de dados (2)
- null  (existe, mas tem uma ausência de valor e não a inexistência de propriedade)  
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
- multiplicação (*)
- divisão (/)
- resto da divisão (%)
- potenciação (**)
- radiciação (sem símbolo) / usar inverso da potenciação / x = num ** (1/raiz)
- também temos a biblioteca Math (PI, pow, sqrt, cbrt, random(), ...)

#### Notação exponencial
- var numExponencial = 2e3

#### Biblioteca Math
- Math.PI
- Math.pow(5, 6)
- Math.sqrt(25)
- Math.cbrt(27)
- Math.random()

##### Gerando números Pseudo-Aleatórios entre 0 e 10:
- numRand = parseInt(Math.random() * 10)

### Bases numéricas
- hexadecimal (0xf)
- octal (0o7)
- binário (0b1)

### Manipulação do DOM  
  
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
  
- setInterval()  
- clearInterval()  
- setTimeout()  







