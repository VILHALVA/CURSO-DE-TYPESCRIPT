# NULL UNDEFINED
Em TypeScript (e JavaScript), `null` e `undefined` são dois valores que representam a ausência de valor. Embora eles sejam semelhantes nesse aspecto, eles têm usos um pouco diferentes.

**`null`:**
- `null` é um valor que representa a ausência intencional de qualquer objeto, valor ou referência a objeto.
- É frequentemente usado para indicar que uma variável ou propriedade de objeto não possui um valor válido ou está vazia.
- `null` é um valor atribuível e comparável a qualquer tipo de dado, exceto `undefined`.
- Deve ser atribuído explicitamente para indicar que uma variável não possui um valor válido.

Exemplo:

```typescript
let nome: string | null = null; // Atribui 'null' para indicar que 'nome' está vazio
```

**`undefined`:**
- `undefined` é um valor que representa a ausência de valor atribuído a uma variável ou propriedade de objeto.
- É frequentemente o valor padrão atribuído a uma variável ou propriedade que não foi inicializada com um valor.
- `undefined` é atribuível a qualquer tipo de dado, incluindo `null`.
- É frequentemente usado para verificar se uma variável ou propriedade foi definida ou inicializada.

Exemplo:

```typescript
let idade: number | undefined; // 'idade' é declarada, mas não possui um valor inicial

if (idade === undefined) {
  console.log("A idade não foi definida.");
}
```

Geralmente, a diferença mais importante entre `null` e `undefined` é que `null` é um valor que você atribui a uma variável ou propriedade para indicar que ela está vazia ou sem valor intencionalmente, enquanto `undefined` é frequentemente usado para indicar que uma variável ou propriedade não foi inicializada com um valor.

Além disso, é uma boa prática evitar atribuir `null` ou `undefined` a menos que seja estritamente necessário e em vez disso, usar valores padrão ou verificar se uma variável já possui um valor antes de usá-la para evitar erros inesperados.