# CLASSES
Em TypeScript, assim como em muitas outras linguagens de programação orientadas a objetos, você pode criar classes para modelar objetos e definir seu comportamento. As classes são uma parte fundamental da programação orientada a objetos e são usadas para criar instâncias de objetos com propriedades e métodos específicos.

Aqui está um exemplo básico de como declarar e usar uma classe em TypeScript:

```typescript
class Pessoa {
  // Propriedades da classe
  nome: string;
  idade: number;

  // Método construtor - é executado quando uma nova instância da classe é criada
  constructor(nome: string, idade: number) {
    this.nome = nome;
    this.idade = idade;
  }

  // Método da classe
  saudacao() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

// Criando uma instância da classe Pessoa
const pessoa1 = new Pessoa("Alice", 30);

// Chamando o método saudacao da instância
pessoa1.saudacao(); // Saída: Olá, meu nome é Alice e tenho 30 anos.
```

Neste exemplo, declaramos uma classe `Pessoa` com propriedades `nome` e `idade`, um método construtor que inicializa essas propriedades e um método `saudacao` que imprime uma mensagem de saudação na tela.

Para criar uma instância da classe `Pessoa`, usamos o operador `new` e chamamos o construtor com os valores desejados para as propriedades. Em seguida, chamamos o método `saudacao` na instância para exibir a saudação.

Você também pode criar subclasses estendendo outras classes:

```typescript
class Estudante extends Pessoa {
  curso: string;

  constructor(nome: string, idade: number, curso: string) {
    super(nome, idade); // Chama o construtor da classe pai
    this.curso = curso;
  }

  saudacao() {
    console.log(`Olá, eu sou ${this.nome}, tenho ${this.idade} anos e estudo ${this.curso}.`);
  }
}

const estudante1 = new Estudante("Bob", 25, "Engenharia");
estudante1.saudacao(); // Saída: Olá, eu sou Bob, tenho 25 anos e estudo Engenharia.
```

Neste exemplo, declaramos uma classe `Estudante` que herda da classe `Pessoa`. A classe `Estudante` tem uma propriedade adicional `curso` e sobrescreve o método `saudacao` para incluir informações sobre o curso.

As classes são uma poderosa ferramenta para organizar e modelar objetos em seu código. Elas permitem criar abstrações reutilizáveis, encapsular dados e comportamentos, e facilitam o desenvolvimento orientado a objetos. 