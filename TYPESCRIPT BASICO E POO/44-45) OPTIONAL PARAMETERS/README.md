# OPTIONAL PARAMETERS
Em TypeScript, você pode criar parâmetros opcionais em funções para permitir que você chame a função com ou sem esses parâmetros. Isso é útil quando você deseja tornar alguns argumentos de função não obrigatórios. Para criar parâmetros opcionais, você utiliza o operador `?` após o nome do parâmetro na declaração da função.

Aqui está um exemplo de como criar parâmetros opcionais em funções:

```typescript
function saudacao(nome?: string) {
  if (nome) {
    console.log(`Olá, ${nome}!`);
  } else {
    console.log("Olá, mundo!");
  }
}

saudacao();         // Saída: Olá, mundo!
saudacao("Alice");  // Saída: Olá, Alice!
```

Neste exemplo, o parâmetro `nome` é opcional na função `saudacao`. Quando você chama a função sem fornecer um valor para `nome`, ela assume o valor padrão `undefined`. Dentro da função, verificamos se `nome` tem um valor antes de usar para evitar erros.

É importante notar que os parâmetros opcionais devem sempre estar no final da lista de parâmetros da função. Isso ocorre porque, se você chamar a função com argumentos, eles devem corresponder na ordem aos parâmetros declarados.

Você também pode usar valores padrão para parâmetros opcionais, o que permite que você forneça um valor padrão que será usado se nenhum valor for passado durante a chamada da função:

```typescript
function saudacaoComPadrao(nome: string = "mundo") {
  console.log(`Olá, ${nome}!`);
}

saudacaoComPadrao();         // Saída: Olá, mundo!
saudacaoComPadrao("Alice");  // Saída: Olá, Alice!
```

Neste exemplo, o parâmetro `nome` possui um valor padrão de `"mundo"`. Se nenhum valor for fornecido durante a chamada da função, o valor padrão será usado automaticamente.

Os parâmetros opcionais e os valores padrão são úteis quando você deseja fornecer flexibilidade em suas funções, permitindo que os usuários da função escolham quais argumentos desejam passar e quais podem ser omitidos. Isso torna suas funções mais versáteis e fáceis de usar em diferentes situações.