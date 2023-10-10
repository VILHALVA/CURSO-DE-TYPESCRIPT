# TYPE ANOTATION
Em TypeScript, as anotações de tipo são usadas para especificar explicitamente os tipos de dados de variáveis, parâmetros de função e valores de retorno de função. Elas fornecem uma maneira de definir os tipos esperados de valores em seu código, tornando mais fácil identificar erros relacionados a tipos durante o desenvolvimento e melhorando a capacidade das ferramentas de fornecer sugestões de código e auto-completar.

Aqui está como você pode usar anotações de tipo em TypeScript:

### Anotações de Tipo para Variáveis:

```typescript
let idade: number; // Declara uma variável 'idade' com a anotação de tipo 'number'
idade = 25;       // Válido, pois 'idade' é esperada ser um número
idade = '25';     // Erro: O tipo '"25"' não é atribuível ao tipo 'number'
```

Neste exemplo, `idade` é explicitamente anotada como um `number`, portanto o TypeScript emitirá um erro se você tentar atribuir um valor que não seja um número a ela.

### Anotações de Tipo para Parâmetros de Função:

```typescript
function saudacao(nome: string): string {
  return `Olá, ${nome}!`;
}

const cumprimento = saudacao('João'); // 'cumprimento' será do tipo 'string'
const cumprimentoIncorreto = saudacao(42); // Erro: O argumento do tipo '42' não é atribuível ao parâmetro do tipo 'string'
```

Na função `saudacao`, o parâmetro `nome` é anotado como `string`, e a função é esperada retornar uma `string`. TypeScript faz a verificação dessas anotações de tipo, ajudando a identificar erros de tipo logo no início.

### Anotações de Tipo para Valores de Retorno de Função:

```typescript
function somar(a: number, b: number): number {
  return a + b;
}

const resultado = somar(10, 20);  // 'resultado' será do tipo 'number'
const resultadoInvalido = somar('10', 20); // Erro: O argumento do tipo '"10"' não é atribuível ao parâmetro do tipo 'number'
```

Na função `somar`, os parâmetros `a` e `b` são anotados como `number`, e a função é esperada retornar um `number`. TypeScript verifica essas anotações de tipo, ajudando a prevenir erros de tipo no código.