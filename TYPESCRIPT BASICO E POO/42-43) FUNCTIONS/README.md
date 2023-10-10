# FUNCTIONS
Funções são blocos de código que realizam tarefas específicas em um programa. Em TypeScript, as funções são uma parte fundamental da linguagem e podem ser usadas para organizar e reutilizar o código. As funções podem ter parâmetros que aceitam valores de entrada e podem retornar um valor como resultado.

Aqui está como declarar e usar funções em TypeScript:

```typescript
// Declaração de uma função simples sem parâmetros e sem valor de retorno
function saudacao() {
  console.log("Olá, mundo!");
}

// Chamando a função
saudacao(); // Saída: Olá, mundo!
```

Neste exemplo, declaramos uma função chamada `saudacao` que não aceita nenhum parâmetro e não retorna nenhum valor. Quando a função é chamada usando `saudacao()`, ela imprime "Olá, mundo!" no console.

Aqui está um exemplo de função com parâmetros e um valor de retorno:

```typescript
// Função que recebe dois números como parâmetros e retorna a soma deles
function soma(a: number, b: number): number {
  return a + b;
}

// Chamando a função e atribuindo o resultado a uma variável
let resultado: number = soma(5, 3);
console.log(resultado); // Saída: 8
```

Neste exemplo, declaramos uma função chamada `soma` que aceita dois parâmetros `a` e `b`, ambos do tipo `number`. A função retorna a soma dos dois números como um valor do tipo `number`. Ao chamar a função `soma(5, 3)`, o resultado é 8, que é atribuído à variável `resultado`.

Funções também podem ter parâmetros opcionais e valores padrão:

```typescript
// Função com parâmetro opcional
function saudacaoPersonalizada(nome?: string) {
  if (nome) {
    console.log(`Olá, ${nome}!`);
  } else {
    console.log("Olá, mundo!");
  }
}

saudacaoPersonalizada();         // Saída: Olá, mundo!
saudacaoPersonalizada("Alice");  // Saída: Olá, Alice!
```

Neste exemplo, a função `saudacaoPersonalizada` aceita um parâmetro opcional `nome` do tipo `string`. Se nenhum nome for fornecido, a função saúda o mundo; caso contrário, ela saúda a pessoa com o nome fornecido.

Além disso, você também pode usar funções de flecha (arrow functions) para criar funções de forma mais concisa:

```typescript
const quadrado = (x: number): number => x * x;
console.log(quadrado(4)); // Saída: 16
```

As funções são componentes essenciais da programação em TypeScript e permitem que você crie código organizado, modular e reutilizável. Elas são usadas para encapsular a lógica do programa em unidades independentes e facilitam a manutenção e o desenvolvimento de código mais legível.