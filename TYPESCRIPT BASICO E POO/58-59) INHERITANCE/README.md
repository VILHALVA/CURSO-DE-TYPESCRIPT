# INHERITANCE
A herança é um conceito fundamental na programação orientada a objetos que permite criar novas classes baseadas em classes existentes. Em TypeScript, você pode usar a herança para criar uma classe derivada (subclasse) que herda propriedades e métodos de uma classe base (superclasse). A classe derivada pode adicionar funcionalidades adicionais ou substituir funcionalidades existentes da classe base.

Aqui está um exemplo simples de herança em TypeScript:

```typescript
// Classe base (superclasse)
class Animal {
  nome: string;

  constructor(nome: string) {
    this.nome = nome;
  }

  fazerBarulho() {
    console.log("Fazendo barulho genérico...");
  }
}

// Classe derivada (subclasse)
class Cachorro extends Animal {
  constructor(nome: string) {
    super(nome); // Chama o construtor da classe base
  }

  fazerBarulho() {
    console.log("Latindo: Woof! Woof!");
  }

  correr() {
    console.log(`${this.nome} está correndo.`);
  }
}

const meuCachorro = new Cachorro("Rex");
console.log(`Nome: ${meuCachorro.nome}`); // Saída: Nome: Rex
meuCachorro.fazerBarulho(); // Saída: Latindo: Woof! Woof!
meuCachorro.correr();       // Saída: Rex está correndo.
```

Neste exemplo, temos uma classe base `Animal` com uma propriedade `nome` e um método `fazerBarulho`, e uma classe derivada `Cachorro` que herda de `Animal`. A classe `Cachorro` chama o construtor da classe base usando `super(nome)` para inicializar a propriedade `nome` e substitui o método `fazerBarulho` para fazer um barulho de latido.

A herança permite que você crie uma hierarquia de classes, onde as classes derivadas herdam propriedades e métodos da classe base, mas também podem ter suas próprias características exclusivas. É uma maneira eficaz de reutilizar código e criar uma estrutura de classes mais organizada.

Além disso, TypeScript suporta herança múltipla por meio da implementação de várias interfaces, permitindo que uma classe tenha várias fontes de herança de funcionalidade. No entanto, a herança múltipla de classes não é diretamente suportada em TypeScript para evitar problemas de ambiguidade, e você deve usar outros mecanismos, como mixins ou composição, para atingir funcionalidades semelhantes. 