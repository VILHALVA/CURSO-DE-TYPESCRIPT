# DIFERENÇA DE TIPOS
A diferença entre `Boolean` (com "B" maiúsculo) e `boolean` (com "b" minúsculo) está relacionada à diferença entre tipos de dados primitivos e objetos em JavaScript e TypeScript.

1. **`boolean` (minúsculo)**:
   - O `boolean` é um tipo de dado primitivo em JavaScript e TypeScript.
   - Ele representa um valor booleano, que pode ser `true` (verdadeiro) ou `false` (falso).
   - É usado para armazenar valores booleanos simples, como o resultado de uma expressão condicional.

   Exemplo em TypeScript:
   ```typescript
   let isActive: boolean = true;
   ```

2. **`Boolean` (maiúsculo)**:
   - `Boolean` é um objeto construtor em JavaScript e TypeScript.
   - Ele é usado para criar objetos booleanos. Você pode usar `new Boolean(value)` para criar um objeto booleano, onde `value` é `true` ou `false`.
   - Em comparação com o tipo primitivo `boolean`, o objeto `Boolean` tem propriedades e métodos adicionais, mas geralmente não é usado com frequência, pois é mais comum trabalhar com o tipo primitivo `boolean`.

   Exemplo em TypeScript:
   ```typescript
   let isActive: Boolean = new Boolean(true); // Objeto Boolean
   ```

   No exemplo acima, `isActive` é uma variável que armazena um objeto `Boolean`, não um valor primitivo `boolean`.

É importante notar que, na prática, é preferível usar o tipo primitivo `boolean` (minúsculo) quando você precisa representar valores booleanos simples, como resultados de condições, variáveis de estado, etc. O uso do objeto `Boolean` (maiúsculo) é raro na maioria dos casos e geralmente não é necessário, a menos que você tenha requisitos específicos que exijam um objeto booleano com propriedades e métodos adicionais. Portanto, ao lidar com valores booleanos simples, use `boolean` (minúsculo).