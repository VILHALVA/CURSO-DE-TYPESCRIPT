# GETTERS E SETTERS
Os "getters" e "setters" são recursos em TypeScript (e em outras linguagens de programação orientadas a objetos) que permitem controlar o acesso e a modificação de propriedades de uma classe de forma mais granular, implementando lógica personalizada quando uma propriedade é lida (get) ou escrita (set). Isso ajuda a manter o encapsulamento de dados e oferece maior controle sobre como os valores das propriedades são manipulados.

Vamos começar com os "getters" e depois passar para os "setters".

### Getters:

Um "getter" é um método que permite acessar o valor de uma propriedade de classe de forma controlada. Ele é definido usando a palavra-chave `get` seguida pelo nome do método. Um "getter" não recebe argumentos e deve retornar um valor.

Aqui está um exemplo de como usar um "getter":

```typescript
class Retângulo {
  private _largura: number;
  private _altura: number;

  constructor(largura: number, altura: number) {
    this._largura = largura;
    this._altura = altura;
  }

  // Getter para a largura
  get largura(): number {
    return this._largura;
  }

  // Getter para a altura
  get altura(): number {
    return this._altura;
  }

  // Getter para a área calculada
  get area(): number {
    return this._largura * this._altura;
  }
}

const retângulo = new Retângulo(10, 5);
console.log(`Largura: ${retângulo.largura}`); // Saída: Largura: 10
console.log(`Altura: ${retângulo.altura}`);   // Saída: Altura: 5
console.log(`Área: ${retângulo.area}`);       // Saída: Área: 50
```

Neste exemplo, a classe `Retângulo` possui "getters" para as propriedades `largura` e `altura`, bem como um "getter" calculado para a propriedade `area`. Quando você acessa essas propriedades, os "getters" são automaticamente chamados para fornecer os valores.

### Setters:

Um "setter" é um método que permite definir o valor de uma propriedade de classe de forma controlada. Ele é definido usando a palavra-chave `set` seguida pelo nome do método. Um "setter" recebe um valor como argumento e pode realizar validações ou lógica personalizada antes de atribuir o valor à propriedade.

Aqui está um exemplo de como usar um "setter":

```typescript
class ContaBancária {
  private _saldo: number;

  constructor(saldoInicial: number) {
    this._saldo = saldoInicial;
  }

  // Getter para o saldo
  get saldo(): number {
    return this._saldo;
  }

  // Setter para o saldo
  set saldo(novoSaldo: number) {
    if (novoSaldo >= 0) {
      this._saldo = novoSaldo;
    } else {
      console.log("Saldo não pode ser negativo.");
    }
  }
}

const conta = new ContaBancária(1000);
console.log(`Saldo atual: ${conta.saldo}`); // Saída: Saldo atual: 1000

// Usando o setter para definir um novo saldo
conta.saldo = 1500;
console.log(`Novo saldo: ${conta.saldo}`); // Saída: Novo saldo: 1500

// Tentando definir um saldo negativo (irá imprimir a mensagem do setter)
conta.saldo = -500; // Saída: Saldo não pode ser negativo.
```

Neste exemplo, a classe `ContaBancária` possui um "getter" para a propriedade `saldo` e um "setter" que verifica se o novo saldo é maior ou igual a zero antes de atribuí-lo. Isso garante que o saldo nunca seja negativo.

Os "getters" e "setters" são úteis quando você deseja controlar o acesso e a modificação de propriedades de classe e quando precisa realizar validações ou lógica personalizada ao fazê-lo. Eles ajudam a manter o encapsulamento de dados e a criar classes mais robustas e seguras.