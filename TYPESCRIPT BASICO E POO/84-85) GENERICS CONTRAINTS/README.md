# GENERICS CONTRAINTS
Em TypeScript, os "generics constraints" (restrições de tipos genéricos) são usados para impor que um tipo genérico deve atender a determinados critérios ou implementar certas propriedades e métodos específicos. As restrições são usadas para fornecer informações adicionais sobre o tipo genérico, permitindo que você escreva código mais seguro e específico.

Aqui está a sintaxe geral para definir restrições de tipos genéricos:

```typescript
function nomeDaFunção<T extends TipoRestrito>(parametro: T): void {
  // O código aqui pode usar propriedades ou métodos de T
}
```

- `T` é o tipo genérico.
- `extends` é usado para indicar a restrição.
- `TipoRestrito` é o tipo ou interface que você deseja usar como restrição.

Aqui estão alguns exemplos de como usar restrições de tipos genéricos:

**Exemplo 1: Restringindo a um tipo específico:**

```typescript
function imprimirComprimento<T extends { length: number }>(valor: T): void {
  console.log(`Comprimento: ${valor.length}`);
}

imprimirComprimento("Olá, mundo!"); // Comprimento: 12
imprimirComprimento([1, 2, 3, 4, 5]); // Comprimento: 5
```

Neste exemplo, a função `imprimirComprimento` aceita um argumento genérico `valor`, mas a restrição `T extends { length: number }` garante que `valor` deve ser de um tipo que tenha uma propriedade `length` do tipo `number`.

**Exemplo 2: Restringindo a um subtipo de uma interface:**

```typescript
interface Animal {
  nome: string;
  som(): void;
}

function fazerBarulho<T extends Animal>(animal: T): void {
  console.log(`O ${animal.nome} faz:`);
  animal.som();
}

const cachorro: Animal = {
  nome: "Rex",
  som() {
    console.log("Latido!");
  },
};

fazerBarulho(cachorro); // O Rex faz: Latido!
```

Neste exemplo, a função `fazerBarulho` aceita um argumento genérico `animal`, mas a restrição `T extends Animal` garante que `animal` deve ser de um tipo que implemente a interface `Animal`.

As restrições de tipos genéricos são úteis quando você deseja criar funções genéricas que possam trabalhar apenas com tipos específicos ou subtipos de tipos. Isso ajuda a melhorar a segurança de tipos e a tornar seu código mais previsível e legível. 