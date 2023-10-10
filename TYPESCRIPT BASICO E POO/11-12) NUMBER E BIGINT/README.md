# NUMBER E BIGINT
Em TypeScript, os tipos `number` e `bigint` são usados para representar números, mas com diferenças significativas em suas capacidades e alcances.

## Tipo `number`:
O tipo `number` é usado para representar números em JavaScript, incluindo inteiros e números de ponto flutuante. Ele é a forma padrão de representar números.

Exemplo de uso do tipo `number`:

```typescript
let idade: number = 25;  // Número inteiro
let altura: number = 1.75;  // Número de ponto flutuante
```

## Tipo `bigint`:
O tipo `bigint` é uma adição mais recente ao JavaScript (e, por consequência, ao TypeScript) e é usado para representar números inteiros arbitrariamente grandes. Isso é útil quando você precisa trabalhar com números inteiros muito grandes que não podem ser representados com precisão usando o tipo `number`.

Exemplo de uso do tipo `bigint`:

```typescript
let numeroGrande: bigint = 1234567890123456789012345678901234567890n;  // Número inteiro grande
```

## Diferenças entre `number` e `bigint`:
- O tipo `number` representa números de ponto flutuante, o que significa que ele tem limites de precisão e alcance para inteiros muito grandes.
- O tipo `bigint` representa inteiros exatos e não tem limites em relação ao tamanho dos números inteiros que pode representar com precisão.

É importante notar que ao trabalhar com `bigint`, você precisa adicionar um sufixo `n` ao número para indicar que é do tipo `bigint`.

Exemplo de operações com `bigint`:

```typescript
let num1: bigint = 100n;
let num2: bigint = 200n;

let soma: bigint = num1 + num2;
let multiplicacao: bigint = num1 * num2;

console.log("Soma:", soma);  // Soma: 300n
console.log("Multiplicação:", multiplicacao);  // Multiplicação: 20000n
```

Em resumo, o tipo `number` é usado para representar números de ponto flutuante e inteiros dentro de um alcance específico, enquanto o tipo `bigint` é usado para representar inteiros exatos, especialmente aqueles que são muito grandes e não podem ser representados com precisão pelo tipo `number`.