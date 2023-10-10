# TIPO TUPLE
Em TypeScript, o tipo `tuple` (ou tupla em português) é uma estrutura de dados que permite definir um array com um número fixo de elementos, onde cada elemento pode ter um tipo de dado diferente. Diferentemente de um array normal, onde todos os elementos têm o mesmo tipo, em uma tupla, você especifica os tipos de cada elemento individualmente.

Aqui está como você pode definir e usar uma tupla em TypeScript:

```typescript
let pessoa: [string, number] = ["Alice", 30];
```

Neste exemplo, `pessoa` é uma tupla que contém dois elementos: o primeiro é uma string ("Alice") e o segundo é um número (30). A ordem dos tipos deve coincidir com a ordem dos elementos na tupla.

Você pode acessar os elementos de uma tupla usando índices:

```typescript
let nome: string = pessoa[0]; // Acessando o primeiro elemento ("Alice")
let idade: number = pessoa[1]; // Acessando o segundo elemento (30)
```

Você também pode utilizar a desestruturação (destructuring) para atribuir os valores da tupla a variáveis:

```typescript
let [nome, idade] = pessoa; // Desestruturando a tupla
console.log(`Nome: ${nome}, Idade: ${idade}`);
```

Uma característica importante das tuplas é que o TypeScript faz a verificação de tipo durante a atribuição. Se você tentar atribuir valores de tipos diferentes ou acessar um índice fora do intervalo da tupla, o TypeScript irá gerar um erro:

```typescript
let pessoa: [string, number] = ["Alice", 30];
pessoa[0] = 42; // Erro: O tipo '42' não é atribuível ao tipo 'string'
pessoa[2] = "Bob"; // Erro: O índice está fora do intervalo da tupla
```

As tuplas são úteis quando você precisa representar um conjunto fixo de valores de tipos diferentes em uma estrutura de dados. Elas fornecem um grau adicional de segurança de tipos em relação aos arrays tradicionais, garantindo que os tipos dos elementos sejam exatamente o que você especificou.