# SWITCH CASE
A estrutura `switch...case` em TypeScript (e em muitas outras linguagens de programação) é usada para avaliar uma expressão e executar diferentes blocos de código com base no valor dessa expressão. É uma alternativa ao uso de múltiplas declarações `if...else if...else`.

Aqui está como usar o `switch...case` em TypeScript:

```typescript
let diaSemana: number = 3;
let nomeDia: string;

switch (diaSemana) {
  case 1:
    nomeDia = "Segunda-feira";
    break;
  case 2:
    nomeDia = "Terça-feira";
    break;
  case 3:
    nomeDia = "Quarta-feira";
    break;
  case 4:
    nomeDia = "Quinta-feira";
    break;
  case 5:
    nomeDia = "Sexta-feira";
    break;
  default:
    nomeDia = "Fim de semana";
}
```

Neste exemplo, o valor da variável `diaSemana` é avaliado na estrutura `switch`. Dependendo do valor de `diaSemana`, o código dentro do bloco `case` correspondente será executado. No final de cada bloco `case`, é importante usar a instrução `break` para sair do `switch`. O bloco `default` é executado quando nenhum dos casos corresponde ao valor de `diaSemana`.

É importante notar que o uso do `break` é fundamental para evitar a execução de múltiplos blocos `case` quando não é desejado. Sem a instrução `break`, o fluxo de controle continuaria após o primeiro bloco `case` correspondente.

Você também pode usar valores literais ou expressões como casos:

```typescript
let numero: number = 5;
let mensagem: string;

switch (true) {
  case numero === 0:
    mensagem = "Zero";
    break;
  case numero > 0 && numero <= 5:
    mensagem = "Entre 1 e 5";
    break;
  default:
    mensagem = "Valor fora do intervalo";
}
```

Neste exemplo, a estrutura `switch` avalia a expressão `true` e, com base no valor de `numero`, executa o bloco `case` correspondente.

O `switch...case` é útil quando você precisa realizar diferentes ações com base em uma única expressão ou valor. No entanto, é importante lembrar de usar a instrução `break` para evitar execuções indesejadas e, quando possível, considerar a legibilidade do código, optando por estruturas `if...else` ou outros mecanismos de controle de fluxo quando for mais apropriado.