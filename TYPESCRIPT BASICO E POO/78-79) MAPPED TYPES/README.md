# MAPPED TYPES
Mapped types (tipos mapeados) são um recurso avançado em TypeScript que permitem criar tipos novos com base em tipos existentes. Eles são especialmente úteis para transformar ou criar tipos com base nas propriedades de um tipo existente. Os tipos mapeados são frequentemente usados para automatizar a criação de tipos com base em estruturas de dados existentes.

A sintaxe geral para criar um tipo mapeado é a seguinte:

```typescript
type NovoTipo = {
  [PropriedadeExistente in TipoExistente]: NovoTipoDaPropriedade;
};
```

- `NovoTipo` é o tipo resultante após a aplicação do tipo mapeado.
- `PropriedadeExistente` é a propriedade no tipo existente que você deseja iterar.
- `TipoExistente` é o tipo existente no qual você está mapeando as propriedades.
- `NovoTipoDaPropriedade` é o tipo que você deseja atribuir à propriedade no novo tipo.

Aqui estão alguns exemplos de como usar tipos mapeados em TypeScript:

**Exemplo 1: Transformando propriedades de um tipo:**

```typescript
type Pessoa = {
  nome: string;
  idade: number;
};

type PessoaOpcional = {
  [P in keyof Pessoa]?: Pessoa[P];
};

const pessoa: PessoaOpcional = {}; // Todas as propriedades são opcionais
```

Neste exemplo, usamos um tipo mapeado para criar `PessoaOpcional`, que torna todas as propriedades de `Pessoa` opcionais.

**Exemplo 2: Adicionando ou removendo propriedades:**

```typescript
type Pessoa = {
  nome: string;
  idade: number;
};

type PessoaComSobrenome = {
  sobrenome: string;
} & Pessoa;

const pessoa: PessoaComSobrenome = {
  nome: "Alice",
  idade: 30,
  sobrenome: "Smith",
};
```

Neste exemplo, usamos um tipo mapeado para adicionar a propriedade `sobrenome` a `Pessoa` para criar `PessoaComSobrenome`.

**Exemplo 3: Transformando tipos em tipos de união:**

```typescript
type Cores = "vermelho" | "azul" | "verde";

type Opções = {
  [P in Cores]: boolean;
};

const opções: Opções = {
  vermelho: true,
  azul: false,
  verde: true,
};
```

Neste exemplo, usamos um tipo mapeado para criar `Opções` com base nas cores disponíveis em `Cores`, criando um objeto com todas as cores como propriedades booleanas.

Os tipos mapeados são uma ferramenta poderosa para criar tipos de forma dinâmica com base em tipos existentes. Eles permitem automatizar tarefas comuns de definição de tipos e criar tipos que refletem a estrutura de dados de forma mais precisa.