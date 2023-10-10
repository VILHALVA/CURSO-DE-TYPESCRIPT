# IF ELSE
As estruturas condicionais `if` e `else` são fundamentais em TypeScript (e em muitas outras linguagens de programação) para controlar o fluxo do seu programa com base em condições. Elas permitem que você execute diferentes blocos de código com base em se uma expressão condicional é verdadeira ou falsa.

Aqui está como usar `if` e `else` em TypeScript:

```typescript
let idade: number = 18;

if (idade >= 18) {
  console.log("Você é maior de idade."); // Este bloco será executado se a condição for verdadeira
} else {
  console.log("Você é menor de idade."); // Este bloco será executado se a condição for falsa
}
```

Neste exemplo, a variável `idade` é avaliada na condição do `if`. Se `idade` for maior ou igual a 18, o bloco dentro do `if` será executado e "Você é maior de idade." será impresso no console. Caso contrário, o bloco dentro do `else` será executado e "Você é menor de idade." será impresso.

Você também pode encadear várias instruções `if...else if...else` para testar várias condições em sequência:

```typescript
let nota: number = 85;

if (nota >= 90) {
  console.log("Aprovado com nota A");
} else if (nota >= 80) {
  console.log("Aprovado com nota B");
} else if (nota >= 70) {
  console.log("Aprovado com nota C");
} else {
  console.log("Reprovado");
}
```

Neste exemplo, o programa avalia a nota do aluno em várias faixas e imprime a mensagem apropriada com base na nota.

Você também pode usar operadores lógicos, como `&&` (E) e `||` (OU), para criar condições mais complexas:

```typescript
let temperatura: number = 28;
let diaEnsolarado: boolean = true;

if (temperatura > 30 && diaEnsolarado) {
  console.log("Vai ser um ótimo dia para ir à praia!");
} else if (temperatura > 25 || diaEnsolarado) {
  console.log("Pode ser um dia agradável para sair.");
} else {
  console.log("Melhor ficar em casa hoje.");
}
```

Neste exemplo, o programa decide se é um bom dia para ir à praia com base na temperatura e se o dia está ensolarado.

As estruturas condicionais `if` e `else` são ferramentas poderosas para controlar o fluxo de execução do seu código e tomar decisões com base em condições específicas. Elas são fundamentais para a lógica condicional em TypeScript e em muitas outras linguagens de programação.