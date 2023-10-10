# LOOP FOR
O loop `for` é uma estrutura de controle de fluxo em TypeScript (e em muitas outras linguagens de programação) que permite executar um bloco de código repetidamente com base em uma condição ou iteração específica. É frequentemente usado quando você sabe antecipadamente quantas vezes deseja executar o código.

Aqui está a sintaxe básica do loop `for` em TypeScript:

```typescript
for (inicialização; condição; incremento/decremento) {
  // Código a ser executado em cada iteração
}
```

- `inicialização`: É uma expressão que é executada apenas uma vez, no início do loop, geralmente usada para inicializar uma variável de controle.
- `condição`: É uma expressão booleana que é avaliada antes de cada iteração. Se for verdadeira, o loop continuará a ser executado; caso contrário, o loop será encerrado.
- `incremento/decremento`: É uma expressão que é executada após cada iteração, geralmente usada para atualizar a variável de controle.

Aqui está um exemplo simples de um loop `for` que imprime os números de 1 a 5:

```typescript
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

Neste exemplo, a variável `i` é inicializada como 1, e o loop é executado enquanto `i` for menor ou igual a 5. Após cada iteração, `i` é incrementada em 1.

Você também pode usar o loop `for` para percorrer elementos de um array ou qualquer outra coleção:

```typescript
let numeros: number[] = [1, 2, 3, 4, 5];

for (let i = 0; i < numeros.length; i++) {
  console.log(numeros[i]);
}
```

Neste exemplo, o loop `for` é usado para percorrer os elementos do array `numeros`.

Além disso, você pode usar a forma `for...of` para percorrer elementos de uma coleção iterável, como arrays, conjuntos ou strings:

```typescript
let frutas: string[] = ["Maçã", "Banana", "Laranja"];

for (let fruta of frutas) {
  console.log(fruta);
}
```

Este loop `for...of` é mais conciso e legível quando você deseja iterar sobre elementos de uma coleção.

O loop `for` é uma estrutura de controle de fluxo fundamental em programação e é usado para automatizar tarefas que requerem iteração ou repetição. Ele oferece controle preciso sobre o número de iterações e é uma ferramenta poderosa para muitos cenários de programação.