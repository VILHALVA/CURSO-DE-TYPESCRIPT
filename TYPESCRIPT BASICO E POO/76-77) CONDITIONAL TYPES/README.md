# CONDITIONAL TYPES
Conditional types (tipos condicionais) são um recurso avançado em TypeScript que permite definir tipos com base em condições em tempo de compilação. Eles são especialmente úteis quando você deseja criar tipos genéricos que podem variar dependendo das características de outros tipos.

A sintaxe geral para tipos condicionais é a seguinte:

```typescript
T extends U ? X : Y
```

- `T` é o tipo que você deseja verificar.
- `U` é o tipo de referência para a verificação.
- `X` é o tipo que será atribuído se a verificação for verdadeira (se `T` for atribuível a `U`).
- `Y` é o tipo que será atribuído se a verificação for falsa (se `T` não for atribuível a `U`).

Aqui estão alguns exemplos de como usar tipos condicionais em TypeScript:

```typescript
type ÉNúmero<T> = T extends number ? true : false;

const éNúmero1: ÉNúmero<5> = true;    // true
const éNúmero2: ÉNúmero<"abc"> = false; // false
```

Neste exemplo, o tipo `ÉNúmero<T>` verifica se `T` é um número e retorna `true` se for ou `false` se não for.

Você também pode usar tipos condicionais para criar tipos mais complexos com base em tipos existentes. Por exemplo, você pode criar um tipo que extrai todas as chaves de um objeto:

```typescript
type ChavesDoObjeto<T> = {
  [K in keyof T]: K;
};

const chaves: ChavesDoObjeto<{ nome: string; idade: number }> = {
  nome: "nome",
  idade: "idade",
};
```

Neste exemplo, o tipo `ChavesDoObjeto<T>` usa um laço `in` para iterar pelas chaves de `T` e criar um tipo que associa cada chave a si mesma.

Outra aplicação útil de tipos condicionais é criar tipos que lidem com tipos de união. Por exemplo, você pode criar um tipo que extraia todos os tipos de uma união de tipos:

```typescript
type TiposDeUnião<T> = T extends any ? T : never;

type União = string | number | boolean;
type TiposDaUnião = TiposDeUnião<União>; // string | number | boolean
```

Neste exemplo, o tipo `TiposDeUnião<T>` verifica cada membro da união e, se `T` for atribuível a `any`, ele retorna esse membro. Isso é útil para criar tipos que descompactam tipos de união.

Os tipos condicionais são uma ferramenta avançada em TypeScript e podem ser usados para criar tipos genéricos complexos e flexíveis. Eles são especialmente úteis ao lidar com tipos de união, mapeamento de tipos e criação de tipos com base em condições específicas.