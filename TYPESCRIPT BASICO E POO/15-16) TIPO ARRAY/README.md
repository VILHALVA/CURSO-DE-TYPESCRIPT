# TIPO ARRAY
Em TypeScript, o tipo `Array` é usado para representar uma coleção de elementos de um mesmo tipo. Os arrays são estruturas de dados fundamentais em programação e permitem armazenar e acessar vários valores sob um mesmo nome.

Há duas maneiras comuns de definir um array em TypeScript:

### Usando a sintaxe de colchetes:

```typescript
let numeros: number[] = [1, 2, 3, 4, 5]; // Array de números
let nomes: string[] = ["Alice", "Bob", "Charlie"]; // Array de strings
```

Neste exemplo, `numeros` é um array de números e `nomes` é um array de strings. Os colchetes (`[]`) são usados para indicar que estamos definindo um array.

### Usando a classe `Array`:

```typescript
let numeros: Array<number> = [1, 2, 3, 4, 5]; // Array de números
let nomes: Array<string> = ["Alice", "Bob", "Charlie"]; // Array de strings
```

Aqui, também estamos criando arrays de números e strings, mas utilizando a classe `Array` com o tipo entre os símbolos de maior e menor (`<>`).

#### Acessando elementos de um array:

Você pode acessar elementos de um array usando um índice, que começa em 0 para o primeiro elemento e aumenta de um em um.

```typescript
let numeros: number[] = [10, 20, 30];
console.log(numeros[0]); // Acessando o primeiro elemento: 10
console.log(numeros[1]); // Acessando o segundo elemento: 20
```

#### Modificando elementos de um array:

Você pode modificar um elemento em um array atribuindo um novo valor a uma posição específica.

```typescript
let frutas: string[] = ["Maçã", "Banana", "Laranja"];
frutas[1] = "Pera"; // Modificando o segundo elemento
console.log(frutas); // Output: ["Maçã", "Pera", "Laranja"]
```

#### Propriedade `length`:

A propriedade `length` é usada para obter o número de elementos em um array.

```typescript
let numeros: number[] = [1, 2, 3, 4, 5];
console.log(numeros.length); // Output: 5
```

#### Iterando sobre um array:

Você pode percorrer os elementos de um array usando loops, como `for` ou `for...of`.

```typescript
let numeros: number[] = [10, 20, 30];

// Usando for
for (let i = 0; i < numeros.length; i++) {
  console.log(numeros[i]);
}

// Usando for...of
for (let numero of numeros) {
  console.log(numero);
}
```

Em resumo, os arrays em TypeScript são coleções de elementos do mesmo tipo, permitindo armazenar e acessar vários valores sob um mesmo nome. Eles são uma parte essencial de muitos programas e são usados para organizar e manipular dados de forma eficaz.