# REST PARAMETERS
Os "rest parameters" (parâmetros rest) são uma característica do TypeScript (e do JavaScript) que permite que uma função receba um número indefinido de argumentos como uma lista ou array. Isso é útil quando você deseja criar funções que podem manipular qualquer quantidade de argumentos sem saber antecipadamente quantos serão passados.

A sintaxe para criar parâmetros rest é usar três pontos (`...`) seguidos pelo nome do parâmetro, que será um array contendo todos os argumentos adicionais passados para a função.

Aqui está um exemplo de como usar parâmetros rest em TypeScript:

```typescript
function somar(...numeros: number[]): number {
  let resultado = 0;
  for (let numero of numeros) {
    resultado += numero;
  }
  return resultado;
}

console.log(somar(1, 2, 3));          // Saída: 6
console.log(somar(10, 20, 30, 40));  // Saída: 100
```

Neste exemplo, a função `somar` aceita um número indefinido de argumentos como um array chamado `numeros`. A função, em seguida, percorre esse array e calcula a soma de todos os números passados como argumentos.

É importante notar que os parâmetros rest devem ser os últimos na lista de parâmetros da função, uma vez que eles coletam todos os argumentos adicionais. Você pode usar parâmetros rest em conjunto com parâmetros regulares:

```typescript
function juntarStrings(separador: string, ...strings: string[]): string {
  return strings.join(separador);
}

console.log(juntarStrings(", ", "Maçã", "Banana", "Laranja")); // Saída: "Maçã, Banana, Laranja"
```

Neste exemplo, a função `juntarStrings` aceita um parâmetro `separador` e, em seguida, um número indefinido de argumentos de string. Ela usa o método `join` para juntar as strings com o separador especificado.

Os parâmetros rest são uma maneira flexível de lidar com funções que podem receber um número variável de argumentos. Eles permitem que você crie funções mais genéricas e versáteis, tornando o código mais reutilizável e fácil de manter.