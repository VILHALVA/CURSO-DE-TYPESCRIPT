# LOOP WHILE
O loop `while` é uma estrutura de controle de fluxo em TypeScript (e em muitas outras linguagens de programação) que permite executar um bloco de código repetidamente enquanto uma condição específica for verdadeira. Ele é frequentemente usado quando você não sabe antecipadamente quantas vezes deseja executar o código, mas sabe que deseja continuar enquanto uma determinada condição for atendida.

Aqui está a sintaxe básica do loop `while` em TypeScript:

```typescript
while (condição) {
  // Código a ser executado enquanto a condição for verdadeira
}
```

- `condição`: É uma expressão booleana que é avaliada antes de cada iteração. Se for verdadeira, o loop continuará a ser executado; caso contrário, o loop será encerrado.

Aqui está um exemplo simples de um loop `while` que imprime os números de 1 a 5:

```typescript
let i = 1;

while (i <= 5) {
  console.log(i);
  i++;
}
```

Neste exemplo, o loop `while` é executado enquanto a variável `i` for menor ou igual a 5. A cada iteração, o valor de `i` é incrementado em 1.

É importante ter cuidado ao usar loops `while`, pois você precisa garantir que a condição eventualmente se torne falsa, caso contrário, o loop continuará indefinidamente (loop infinito). Certifique-se de que algo dentro do loop está mudando para que a condição se torne falsa em algum momento.

Você também pode usar o loop `do...while`, que é semelhante ao loop `while`, mas garante que o bloco de código seja executado pelo menos uma vez, mesmo que a condição inicial seja falsa:

```typescript
let contador = 0;

do {
  console.log("Este código será executado pelo menos uma vez.");
  contador++;
} while (contador < 3);
```

Neste exemplo, o código dentro do loop `do...while` será executado pelo menos uma vez antes de verificar a condição.

O loop `while` é útil quando você precisa repetir uma ação com base em uma condição que só será conhecida durante a execução do programa. No entanto, como mencionado anteriormente, é importante garantir que a condição eventualmente se torne falsa para evitar loops infinitos. 