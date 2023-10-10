# TYPE ASSERTION
Type assertion (afirmação de tipo) é um recurso em TypeScript que permite ao desenvolvedor dizer ao compilador que ele tem mais conhecimento sobre o tipo de uma variável do que o TypeScript pode inferir automaticamente. É semelhante ao type casting, mas é uma técnica que permite realizar uma conversão de tipo mais segura e confiável.

Em TypeScript, você pode usar a sintaxe `as` ou a sintaxe de "ângulos" (`<>`) para fazer uma afirmação de tipo. Aqui está um exemplo de como fazer uma afirmação de tipo com `as`:

```typescript
const valor: any = "123";
const número: number = valor as number; // Afirmação de tipo: converte explicitamente para number

console.log(número); // 123
```

E aqui está o mesmo exemplo usando a sintaxe de "ângulos":

```typescript
const valor: any = "123";
const número: number = <number>valor; // Afirmação de tipo: converte explicitamente para number

console.log(número); // 123
```

A principal diferença entre type assertion e type casting é que type assertion é mais seguro, pois não permite que você faça conversões entre tipos que não são compatíveis. O TypeScript verifica se a conversão é possível antes de permitir a afirmação de tipo.

Type assertion é útil quando você sabe que um valor é de um tipo específico, mas o TypeScript não pode inferir isso automaticamente. No entanto, é importante usá-lo com cautela e apenas quando você tem certeza de que a conversão é segura, para evitar erros em tempo de execução.

Além disso, o TypeScript oferece type assertion em situações em que você está trabalhando com tipos de união e deseja realizar operações em um tipo específico dentro da união. Por exemplo:

```typescript
type Pessoa = {
  nome: string;
  idade: number;
};

type Animal = {
  tipo: string;
};

function cumprimentar(entidade: Pessoa | Animal) {
  const nome = (entidade as Pessoa).nome || "Desconhecido";
  console.log(`Olá, ${nome}!`);
}

const pessoa: Pessoa = { nome: "Alice", idade: 30 };
const animal: Animal = { tipo: "Cachorro" };

cumprimentar(pessoa); // Saída: Olá, Alice!
cumprimentar(animal); // Saída: Olá, Desconhecido!
```

Neste exemplo, a afirmação de tipo `(entidade as Pessoa)` é usada para garantir que a variável `nome` seja acessada apenas se a entidade for do tipo `Pessoa`. Isso evita erros de compilação. 