# SINTAXE DA LINGUAGEM:
## 0) FUNDAMENTOS:
Aqui está um exemplo de código TypeScript que utiliza operadores aritméticos, relacionais e lógicos com tipos primitivos, juntamente com explicações para cada parte do código:

```typescript
// Operadores Aritméticos
let a: number = 10;
let b: number = 5;

let soma: number = a + b; // Adição
let subtracao: number = a - b; // Subtração
let multiplicacao: number = a * b; // Multiplicação
let divisao: number = a / b; // Divisão
let resto: number = a % b; // Resto da divisão

console.log(`Soma: ${soma}`);
console.log(`Subtração: ${subtracao}`);
console.log(`Multiplicação: ${multiplicacao}`);
console.log(`Divisão: ${divisao}`);
console.log(`Resto da Divisão: ${resto}`);

// Operadores Relacionais
let x: number = 10;
let y: number = 20;

let igual: boolean = x === y; // Igualdade estrita
let diferente: boolean = x !== y; // Diferente estrito
let maior: boolean = x > y; // Maior que
let menor: boolean = x < y; // Menor que
let maiorOuIgual: boolean = x >= y; // Maior ou igual a
let menorOuIgual: boolean = x <= y; // Menor ou igual a

console.log(`Igual: ${igual}`);
console.log(`Diferente: ${diferente}`);
console.log(`Maior: ${maior}`);
console.log(`Menor: ${menor}`);
console.log(`Maior ou Igual: ${maiorOuIgual}`);
console.log(`Menor ou Igual: ${menorOuIgual}`);

// Operadores Lógicos
let p: boolean = true;
let q: boolean = false;

let and: boolean = p && q; // E lógico (AND)
let or: boolean = p || q; // Ou lógico (OR)
let notP: boolean = !p; // Negação lógica (NOT)

console.log(`E lógico (AND): ${and}`);
console.log(`Ou lógico (OR): ${or}`);
console.log(`Negação lógica (NOT) de p: ${notP}`);
```

Neste código:

- Os operadores aritméticos (`+`, `-`, `*`, `/` e `%`) são utilizados para realizar operações matemáticas básicas com as variáveis `a` e `b`.

- Os operadores relacionais (`===`, `!==`, `>`, `<`, `>=` e `<=`) são utilizados para comparar as variáveis `x` e `y` e retornar valores booleanos que indicam se as relações são verdadeiras ou falsas.

- Os operadores lógicos (`&&`, `||` e `!`) são utilizados para realizar operações lógicas com as variáveis booleanas `p` e `q`. Por exemplo, `&&` representa o "E lógico" (AND), `||` representa o "Ou lógico" (OR) e `!` representa a negação lógica (NOT).

Este exemplo demonstra como usar esses operadores com tipos primitivos em TypeScript para realizar cálculos, fazer comparações e avaliar expressões lógicas.

## 1) VARIAVEIS SIMPLES:
Aqui está um exemplo de declaração e uso de variáveis simples em TypeScript, juntamente com explicações:

```typescript
// Variáveis simples
let nome: string = "João"; // Declara uma variável 'nome' do tipo string e atribui o valor "João".
let idade: number = 30; // Declara uma variável 'idade' do tipo number e atribui o valor 30.
let estaTrabalhando: boolean = true; // Declara uma variável 'estaTrabalhando' do tipo boolean e atribui o valor true.

// Exibindo os valores das variáveis
console.log(`Nome: ${nome}`);
console.log(`Idade: ${idade}`);
console.log(`Está trabalhando: ${estaTrabalhando}`);
```

Explicações:

- `let nome: string = "João";`: Aqui, declaramos uma variável chamada `nome` e especificamos que seu tipo é `string`. Em seguida, atribuímos o valor `"João"` a essa variável. A variável `nome` armazena uma sequência de caracteres (uma string).

- `let idade: number = 30;`: Aqui, declaramos uma variável chamada `idade` e especificamos que seu tipo é `number`. Em seguida, atribuímos o valor `30` a essa variável. A variável `idade` armazena um número inteiro.

- `let estaTrabalhando: boolean = true;`: Neste caso, declaramos uma variável chamada `estaTrabalhando` e especificamos que seu tipo é `boolean`. Atribuímos o valor `true` a essa variável. A variável `estaTrabalhando` armazena um valor booleano, que pode ser `true` (verdadeiro) ou `false` (falso).

Depois de declarar e atribuir valores a essas variáveis, usamos `console.log` para exibir os valores das variáveis no console. Este é um exemplo simples de como declarar variáveis com tipos em TypeScript e como atribuir e exibir valores comuns nelas.

## 2) ESTRUTURA CONDICIONAL:
### ESTRUTURA IF-ELSE:
A estrutura condicional `if-else` em TypeScript (e em muitas outras linguagens de programação) permite que você execute diferentes blocos de código com base em uma condição. Aqui está um exemplo de como usar a estrutura `if-else`:

```typescript
let idade: number = 18;

if (idade >= 18) {
    console.log("Você é maior de idade."); // Este bloco será executado se a condição for verdadeira.
}
else {
    console.log("Você é menor de idade."); // Este bloco será executado se a condição for falsa.
}
```

Explicações:

- Declaramos uma variável `idade` e atribuímos o valor `18` a ela.

- Em seguida, usamos a estrutura `if` para testar uma condição. A condição é `idade >= 18`, que verifica se a `idade` é maior ou igual a `18`.

- Se a condição for verdadeira (ou seja, se a idade for maior ou igual a 18), o bloco de código dentro do primeiro conjunto de chaves `{}` será executado, e a mensagem "Você é maior de idade." será exibida no console.

- Se a condição for falsa (ou seja, se a idade for menor que 18), o bloco de código dentro do segundo conjunto de chaves `{}` após o `else` será executado, e a mensagem "Você é menor de idade." será exibida no console.

A estrutura `if-else` permite que você tome decisões com base em condições e execute diferentes blocos de código dependendo do resultado dessas condições. É uma parte fundamental da programação para criar lógica condicional em seus programas.

### ESTRUTURA SWITCH:
A estrutura `switch` em TypeScript (e em muitas outras linguagens de programação) é uma forma de executar diferentes blocos de código com base no valor de uma expressão. Ela é especialmente útil quando você tem múltiplas condições para verificar em relação a uma única variável. Aqui está um exemplo de como usar a estrutura `switch`:

```typescript
let diaSemana: number = 3;
let mensagem: string;

switch (diaSemana) {
    case 1:
        mensagem = "Segunda-feira";
        break;
    case 2:
        mensagem = "Terça-feira";
        break;
    case 3:
        mensagem = "Quarta-feira";
        break;
    case 4:
        mensagem = "Quinta-feira";
        break;
    case 5:
        mensagem = "Sexta-feira";
        break;
    case 6:
    case 7:
        mensagem = "Fim de semana";
        break;
    default:
        mensagem = "Dia inválido";
        break;
}

console.log(`Hoje é ${mensagem}`);
```

Explicações:

- Declaramos uma variável `diaSemana` e atribuímos o valor `3` a ela, representando a quarta-feira.

- Em seguida, usamos a estrutura `switch` para avaliar o valor da variável `diaSemana`.

- Cada `case` representa um valor possível que `diaSemana` pode ter. Se `diaSemana` corresponder a um dos valores dentro de `case`, o código dentro desse `case` será executado.

- Usamos `break` para sair do `switch` após a execução do bloco correspondente. Isso impede que os casos subsequentes sejam executados.

- Se `diaSemana` não corresponder a nenhum dos casos, o bloco de código dentro de `default` será executado.

- No nosso exemplo, como `diaSemana` é igual a `3`, o bloco de código correspondente ao `case 3` será executado, atribuindo a mensagem "Quarta-feira" à variável `mensagem`.

- No final, exibimos a mensagem no console.

A estrutura `switch` é útil quando você precisa avaliar uma variável para múltiplas condições diferentes e executar blocos de código com base em correspondências específicas.

## 3) ESTRUTURA DE REPETIÇÃO:
### ESTRUTURA FOR:
A estrutura de repetição `for` em TypeScript (e em muitas outras linguagens de programação) é utilizada para executar um bloco de código repetidamente enquanto uma condição é verdadeira. A estrutura `for` é especialmente útil quando você precisa executar um conjunto específico de iterações. Aqui está um exemplo de como usar a estrutura `for`:

```typescript
// Exemplo de estrutura de repetição for
for (let i = 0; i < 5; i++) {
    console.log(`Iteração ${i}`);
}
```

Explicações:

- A estrutura `for` começa com a palavra-chave `for`, seguida por um conjunto de parênteses `()`.

- Dentro dos parênteses, você geralmente encontra três partes separadas por ponto e vírgula (`;`):
   1. Inicialização (`let i = 0;`): Isso define uma variável `i` e atribui o valor inicial, que é `0` no exemplo.
   2. Condição (`i < 5;`): Isso define a condição que determina quando o loop continuará a ser executado. Enquanto a condição for verdadeira, o loop continuará. No exemplo, o loop continua enquanto `i` for menor que `5`.
   3. Atualização (`i++`): Isso especifica como a variável de controle `i` é atualizada após cada iteração do loop. Em geral, é uma operação de incremento (`i++` é o mesmo que `i = i + 1`), mas você pode usar outros valores de atualização, se necessário.

- O bloco de código que deve ser executado em cada iteração é colocado entre chaves `{}`.

Neste exemplo, o `for` loop será executado cinco vezes, começando com `i = 0` e incrementando `i` a cada iteração até que `i` seja igual a `5`. Em cada iteração, ele imprimirá uma mensagem no console indicando o número da iteração.

Você pode personalizar a estrutura `for` para atender às suas necessidades específicas de iteração, ajustando a inicialização, a condição e a atualização, assim como o bloco de código a ser executado no loop. A estrutura `for` é uma ferramenta poderosa para controlar repetições em seu código.

### ESTRUTURA WHILE:
A estrutura de repetição `while` em TypeScript (e em muitas outras linguagens de programação) é usada para executar um bloco de código enquanto uma condição especificada for verdadeira. Ao contrário do `for`, o `while` não exige um número fixo de iterações. Ele continuará a executar até que a condição seja avaliada como falsa. Aqui está um exemplo de como usar a estrutura `while`:

```typescript
let contador: number = 0;

while (contador < 5) {
    console.log(`Iteração ${contador}`);
    contador++;
}
```

Explicações:

- A estrutura `while` começa com a palavra-chave `while`, seguida por um conjunto de parênteses `()`.

- Dentro dos parênteses, você especifica a condição que deve ser avaliada como verdadeira para continuar executando o bloco de código. No exemplo, a condição é `contador < 5`, o que significa que o loop continuará enquanto o valor da variável `contador` for menor que `5`.

- O bloco de código que deve ser executado em cada iteração é colocado entre chaves `{}`.

- Dentro do bloco de código, você geralmente faz alguma atualização na variável de controle para que a condição eventualmente se torne falsa e o loop seja encerrado. No exemplo, incrementamos `contador` em `1` a cada iteração usando `contador++`.

Neste exemplo, o `while` loop começará com `contador` igual a `0` e continuará a ser executado até que `contador` seja maior ou igual a `5`. A cada iteração, ele imprimirá uma mensagem no console indicando o número da iteração e incrementará o `contador` em `1`.

É importante ter cuidado ao usar o `while` loop para evitar loops infinitos. Certifique-se de que a condição dentro do `while` eventualmente se torne falsa para que o loop possa ser encerrado.

### ESTRUTURA DO-WHILE:
A estrutura de repetição `do-while` em TypeScript (e em muitas outras linguagens de programação) é usada para executar um bloco de código pelo menos uma vez, mesmo que a condição especificada seja inicialmente falsa. Após a primeira execução, o bloco continuará a ser executado enquanto a condição especificada for verdadeira. Aqui está um exemplo de como usar a estrutura `do-while`:

```typescript
let contador: number = 0;

do {
    console.log(`Iteração ${contador}`);
    contador++;
} while (contador < 5);
```

Explicações:

- A estrutura `do-while` começa com a palavra-chave `do`, seguida por um bloco de código entre chaves `{}`.

- Dentro do bloco de código, você especifica o código que deseja executar pelo menos uma vez. No exemplo, usamos `console.log` para imprimir uma mensagem no console e incrementamos a variável `contador`.

- Após o bloco de código, a estrutura `do-while` inclui a palavra-chave `while`, seguida por um conjunto de parênteses `()`.

- Dentro dos parênteses, você especifica a condição que determinará se o bloco de código deve continuar a ser executado. No exemplo, a condição é `contador < 5`, o que significa que o bloco de código será executado enquanto o valor da variável `contador` for menor que `5`.

Neste exemplo, o `do-while` loop começará com `contador` igual a `0`. O bloco de código será executado pelo menos uma vez, porque a condição é verificada após a primeira execução. Após a primeira execução, o bloco continuará a ser executado enquanto `contador` for menor que `5`. A cada iteração, ele imprimirá uma mensagem no console indicando o número da iteração e incrementará o `contador` em `1`.

A estrutura `do-while` é útil quando você precisa garantir que um bloco de código seja executado pelo menos uma vez, independentemente da condição inicial, e depois continuar a ser executado com base em uma condição de verificação.

## 4) VARIAVEIS COMPOSTAS:
### ARRAYS:
Em TypeScript (e em JavaScript), um array é uma estrutura de dados que permite armazenar e organizar uma coleção de elementos em uma única variável. Cada elemento em um array pode ser de qualquer tipo de dados, como números, strings, objetos, ou até mesmo outros arrays. Aqui está um exemplo de como criar, acessar e manipular arrays em TypeScript:

#### Criando um Array:
```typescript
// Criando um array de números
let numeros: number[] = [1, 2, 3, 4, 5];

// Criando um array de strings
let frutas: string[] = ["maçã", "banana", "laranja"];

// Criando um array vazio
let vazio: any[] = [];
```

Neste exemplo, criamos três arrays: `numeros`, `frutas`, e `vazio`. `numeros` é um array de números, `frutas` é um array de strings, e `vazio` é um array vazio que pode conter qualquer tipo de dado.

#### Acessando Elementos de um Array:
```typescript
console.log(numeros[0]); // Acessando o primeiro elemento do array numeros (índice 0)
console.log(frutas[1]);  // Acessando o segundo elemento do array frutas (índice 1)
```

Os índices dos elementos de um array começam em 0. Portanto, `numeros[0]` acessa o primeiro elemento do array `numeros`, que é `1`, e `frutas[1]` acessa o segundo elemento do array `frutas`, que é `"banana"`.

#### Alterando Elementos de um Array:
```typescript
numeros[2] = 99;         // Alterando o terceiro elemento do array numeros para 99
frutas[0] = "morango";   // Alterando o primeiro elemento do array frutas para "morango"
```

Você pode alterar os elementos de um array atribuindo um novo valor a um índice específico, como mostrado acima.

#### Adicionando e Removendo Elementos de um Array:
```typescript
numeros.push(6);           // Adicionando um elemento (6) ao final do array numeros
frutas.pop();              // Removendo o último elemento do array frutas
frutas.unshift("abacaxi"); // Adicionando um elemento ("abacaxi") no início do array frutas
```

- O método `push` é usado para adicionar um elemento ao final de um array.
- O método `pop` é usado para remover o último elemento de um array.
- O método `unshift` é usado para adicionar um elemento ao início de um array.

#### Obtendo o Comprimento de um Array:
```typescript
console.log(numeros.length);  // Obtendo o número de elementos no array numeros
console.log(frutas.length);   // Obtendo o número de elementos no array frutas
```

O atributo `length` de um array permite obter o número de elementos presentes no array.

Arrays são uma estrutura de dados fundamental em TypeScript e JavaScript, amplamente utilizados para armazenar e manipular conjuntos de informações de forma eficaz. Eles oferecem uma maneira versátil de trabalhar com dados em seu código.

### OBJETOS:
Em TypeScript (e em JavaScript), objetos são uma das estruturas de dados mais importantes e versáteis. Eles permitem que você organize e armazene dados relacionados em pares chave-valor. Cada par chave-valor é conhecido como uma propriedade do objeto. Aqui está um exemplo de como criar, acessar e manipular objetos em TypeScript:

#### Criando um Objeto:
```typescript
// Criando um objeto de pessoa
let pessoa: { nome: string; idade: number } = {
    nome: "Alice",
    idade: 30
};
```

Neste exemplo, criamos um objeto `pessoa` com duas propriedades: `nome` (uma string) e `idade` (um número).

#### Acessando Propriedades de um Objeto:
```typescript
console.log(pessoa.nome);   // Acessando a propriedade "nome" do objeto pessoa
console.log(pessoa.idade);  // Acessando a propriedade "idade" do objeto pessoa
```

Você pode acessar as propriedades de um objeto usando a notação de ponto (`objeto.propriedade`), como mostrado acima.

#### Alterando Propriedades de um Objeto:
```typescript
pessoa.nome = "Bob";     // Alterando o valor da propriedade "nome" para "Bob"
pessoa.idade = 35;       // Alterando o valor da propriedade "idade" para 35
```

Você pode alterar o valor de uma propriedade de objeto atribuindo um novo valor a ela.

#### Adicionando Propriedades a um Objeto:
```typescript
pessoa.email = "bob@example.com"; // Adicionando uma nova propriedade "email" ao objeto pessoa
```

Você pode adicionar novas propriedades a um objeto simplesmente atribuindo um valor a uma chave que não existe.

#### Deletando Propriedades de um Objeto:
```typescript
delete pessoa.idade; // Deletando a propriedade "idade" do objeto pessoa
```

Você pode deletar uma propriedade de um objeto usando o operador `delete`.

#### Objeto com Métodos:
Além de armazenar dados, objetos também podem conter métodos (funções) que são chamados para realizar ações relacionadas ao objeto. Aqui está um exemplo:

```typescript
let carro = {
    marca: "Toyota",
    modelo: "Camry",
    ano: 2020,
    ligar: function () {
        console.log("O carro está ligado.");
    },
    desligar: function () {
        console.log("O carro está desligado.");
    }
};

carro.ligar(); // Chama o método "ligar" do objeto carro
carro.desligar(); // Chama o método "desligar" do objeto carro
```

Neste exemplo, o objeto `carro` possui duas propriedades (marca, modelo, ano) e dois métodos (ligar e desligar).

Os objetos são fundamentais para a programação em TypeScript e JavaScript, permitindo que você modele e manipule dados de maneira eficaz. Eles são frequentemente usados para representar entidades do mundo real e suas características.

## 5) FUNÇÕES:
Em TypeScript (e em JavaScript), funções são blocos de código que podem ser definidos e reutilizados para executar tarefas específicas. As funções são uma parte fundamental da programação e oferecem uma maneira de organizar, reutilizar e modularizar seu código. Aqui está um exemplo de como criar, chamar e usar funções em TypeScript:

### Criando uma Função:
```typescript
// Definindo uma função simples que recebe dois números e retorna a soma
function somar(a: number, b: number): number {
    return a + b;
}
```

Neste exemplo, criamos uma função chamada `somar` que recebe dois parâmetros (a e b), ambos do tipo número, e retorna a soma deles como um número.

### Chamando uma Função:
```typescript
let resultado: number = somar(5, 3);
console.log(resultado); // Exibirá 8 no console
```

Para chamar uma função, você simplesmente a referencia pelo nome, seguido dos parênteses contendo os argumentos que você deseja passar para a função. No exemplo acima, chamamos a função `somar` com os argumentos `5` e `3`, e armazenamos o resultado retornado na variável `resultado`.

### Funções com Retorno:
As funções podem retornar valores, que podem ser de qualquer tipo de dados, dependendo da definição da função. No exemplo anterior, a função `somar` retorna um número. Você pode usar a declaração `return` para especificar o valor a ser retornado.

### Funções sem Retorno:
Nem todas as funções precisam retornar um valor. Algumas funções são usadas para realizar ações ou tarefas, mas não produzem um valor de retorno. Nesse caso, o tipo de retorno da função é `void`. Por exemplo:

```typescript
function saudacao(nome: string): void {
    console.log(`Olá, ${nome}!`);
}

saudacao("Alice"); // Exibirá "Olá, Alice!" no console
```

### Parâmetros de Função Opcionais:
Você pode tornar os parâmetros de função opcionais, adicionando um ponto de interrogação `?` ao final do nome do parâmetro. Isso significa que você pode chamar a função com ou sem esse parâmetro. Por exemplo:

```typescript
function saudacaoPersonalizada(nome: string, saudacao?: string): void {
    if (saudacao) {
        console.log(`${saudacao}, ${nome}!`);
    } else {
        console.log(`Olá, ${nome}!`);
    }
}

saudacaoPersonalizada("Alice"); // Exibirá "Olá, Alice!" no console
saudacaoPersonalizada("Bob", "Bom dia"); // Exibirá "Bom dia, Bob!" no console
```

### Arrow Functions (Funções de Flecha):
Em TypeScript, você também pode criar funções de flecha (arrow functions) que são uma forma mais concisa de definir funções. Aqui está um exemplo:

```typescript
const dobrar = (numero: number): number => numero * 2;

console.log(dobrar(5)); // Exibirá 10 no console
```

As arrow functions são frequentemente usadas em contextos onde funções curtas e simples são necessárias.

As funções são uma parte fundamental da programação em TypeScript, permitindo que você abstraia a lógica do seu código em blocos reutilizáveis e modulares. Elas desempenham um papel crucial na organização e estruturação do seu programa.

## 6) CLASS POO:
Vou criar um exemplo de classe em TypeScript que demonstra os quatro pilares da Programação Orientada a Objetos (POO): encapsulamento, herança, polimorfismo e abstração.

```typescript
// Pilar do Encapsulamento
class Animal {
    private nome: string;

    constructor(nome: string) {
        this.nome = nome;
    }

    public emitirSom(): void {
        console.log("Som genérico de animal.");
    }

    public getNome(): string {
        return this.nome;
    }

    public setNome(nome: string): void {
        this.nome = nome;
    }
}

// Pilar da Herança
class Mamifero extends Animal {
    constructor(nome: string) {
        super(nome);
    }

    // Pilar do Polimorfismo
    public emitirSom(): void {
        console.log(`${this.getNome()} faz um som de mamífero.`);
    }
}

// Pilar da Abstração
abstract class Ave extends Animal {
    constructor(nome: string) {
        super(nome);
    }

    public abstract voar(): void;
}

class Pato extends Ave {
    constructor(nome: string) {
        super(nome);
    }

    public voar(): void {
        console.log(`${this.getNome()} voa como um pato.`);
    }
}

// Uso das classes
const cachorro = new Mamifero("Bobby");
const pato = new Pato("Donald");

cachorro.emitirSom(); // Exibirá "Bobby faz um som de mamífero."
pato.emitirSom(); // Exibirá "Donald faz um som de mamífero."
pato.voar(); // Exibirá "Donald voa como um pato."
```

Neste exemplo, temos:

1. **Encapsulamento**: A classe `Animal` possui uma propriedade privada `nome` que só pode ser acessada através dos métodos `getNome` e `setNome`. Isso encapsula o estado interno da classe.

2. **Herança**: A classe `Mamifero` herda da classe `Animal` usando `extends`. Isso permite que a classe `Mamifero` reutilize e estenda o comportamento da classe `Animal`.

3. **Polimorfismo**: O método `emitirSom` é sobrescrito na classe `Mamifero`. Isso demonstra o polimorfismo, onde a mesma interface (método) é implementada de maneira diferente em classes diferentes.

4. **Abstração**: A classe abstrata `Ave` define um método abstrato `voar`. As classes que herdam de `Ave`, como `Pato`, devem implementar esse método, forçando a abstração e garantindo que as classes derivadas forneçam uma implementação concreta.

## 7) INTEGRAÇÃO COM A WEB:
Vou fornecer um exemplo de integração entre front-end e back-end com um aplicativo web simples. Usaremos TypeScript no back-end e JavaScript no front-end, juntamente com Node.js e Express para o servidor back-end e HTML para o front-end.

### Back-End (Node.js com Express):
```typescript
// Importar as dependências
import express from 'express';

// Configurar o servidor Express
const app = express();
const porta = 3000;

// Rota de exemplo: retornar uma lista de tarefas
app.get('/tarefas', (req, res) => {
    const tarefas = [
        { id: 1, descricao: 'Fazer compras' },
        { id: 2, descricao: 'Estudar TypeScript' },
    ];
    res.json(tarefas);
});

// Iniciar o servidor
app.listen(porta, () => {
    console.log(`Servidor rodando na porta ${porta}`);
});
```

Neste exemplo, criamos um servidor Express simples que possui uma rota `/tarefas` que retorna uma lista de tarefas como JSON quando acessada.

### Front-End (JavaScript e HTML):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Front-End</title>
</head>
<body>
    <h1>Lista de Tarefas</h1>
    <ul id="lista-tarefas"></ul>

    <script>
        // Função para carregar a lista de tarefas do servidor
        async function carregarTarefas() {
            const response = await fetch('http://localhost:3000/tarefas');
            const tarefas = await response.json();

            const listaTarefas = document.getElementById('lista-tarefas');

            tarefas.forEach((tarefa) => {
                const item = document.createElement('li');
                item.textContent = tarefa.descricao;
                listaTarefas.appendChild(item);
            });
        }

        // Chamando a função para carregar as tarefas quando a página carrega
        window.onload = carregarTarefas;
    </script>
</body>
</html>
```

Neste exemplo, temos um documento HTML simples que exibe uma lista de tarefas. Usamos JavaScript para fazer uma solicitação ao servidor back-end para obter a lista de tarefas usando a função `fetch`.

### Passos para Testar:
1. Certifique-se de que o Node.js está instalado e execute o código do servidor back-end em um arquivo TypeScript (por exemplo, `backend.ts`) usando `tsc` para compilar e `node` para executar.
2. Abra o navegador e acesse `http://localhost:3000/tarefas` para verificar se o servidor back-end está funcionando corretamente.
3. Abra o arquivo HTML no navegador para ver a lista de tarefas carregada do servidor.

Este é um exemplo muito simples de integração entre front-end e back-end, demonstrando como o front-end faz uma solicitação HTTP ao back-end para obter dados. Em uma aplicação real, você lidaria com mais complexidade, como autenticação, autorização, manipulação de formulários e muito mais.