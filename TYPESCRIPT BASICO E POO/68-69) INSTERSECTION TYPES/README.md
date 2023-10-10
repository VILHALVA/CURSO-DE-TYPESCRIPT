# INSTERSECTION TYPES
Intersection types (tipos de interseção) em TypeScript são usados para combinar múltiplos tipos em um novo tipo que contém todas as propriedades e métodos de cada tipo de origem. Ou seja, quando você cria uma interseção entre tipos, o novo tipo resultante terá todas as características dos tipos originais.

A sintaxe para criar um tipo de interseção é usar o operador `&` entre os tipos que você deseja combinar. Aqui está um exemplo simples:

```typescript
type Pessoa = {
  nome: string;
  idade: number;
};

type Endereço = {
  rua: string;
  cidade: string;
};

type PessoaComEndereço = Pessoa & Endereço;

const pessoaComEndereço: PessoaComEndereço = {
  nome: "Alice",
  idade: 30,
  rua: "Rua das Flores",
  cidade: "Cidade A",
};

console.log(pessoaComEndereço.nome);    // "Alice"
console.log(pessoaComEndereço.idade);   // 30
console.log(pessoaComEndereço.rua);     // "Rua das Flores"
console.log(pessoaComEndereço.cidade);  // "Cidade A"
```

Neste exemplo, criamos dois tipos, `Pessoa` e `Endereço`, que representam informações de uma pessoa e um endereço. Em seguida, criamos um novo tipo `PessoaComEndereço` que é uma interseção entre `Pessoa` e `Endereço`, combinando todas as propriedades de ambos os tipos. O objeto `pessoaComEndereço` é do tipo `PessoaComEndereço` e possui todas as propriedades de ambas as interfaces originais.

As interseções são especialmente úteis quando você precisa combinar tipos existentes para criar tipos mais complexos que representam objetos com múltiplas características. Elas permitem que você compartilhe propriedades e métodos entre tipos sem criar hierarquias de herança complexas.

Além disso, as interseções podem ser usadas com tipos de união para criar tipos mais flexíveis. Por exemplo:

```typescript
type Aluno = {
  nome: string;
  matrícula: string;
};

type Professor = {
  nome: string;
  departamento: string;
};

type Pessoa = Aluno | Professor; // União de tipos

const pessoa: Pessoa = {
  nome: "Bob",
  departamento: "Matemática",
}; // Válido, pois pertence a ambas as interfaces Aluno e Professor
```

Neste caso, usamos uma união de tipos para criar o tipo `Pessoa`, que pode representar tanto um aluno quanto um professor. A interseção de propriedades (como o nome) é compartilhada por ambos os tipos originais.