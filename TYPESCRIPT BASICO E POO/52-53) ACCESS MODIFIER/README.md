# ACCESS MODIFIER
Os modificadores de acesso em TypeScript são palavras-chave que controlam a visibilidade e a acessibilidade dos membros de uma classe, como propriedades e métodos. Eles determinam quem pode acessar e modificar esses membros dentro e fora da classe. TypeScript oferece três principais modificadores de acesso:

1. **Public:** Este é o modificador de acesso padrão. Membros marcados como `public` são acessíveis de qualquer lugar, tanto dentro quanto fora da classe.

```typescript
class Pessoa {
  public nome: string;

  constructor(nome: string) {
    this.nome = nome;
  }
}

const pessoa = new Pessoa("Alice");
console.log(pessoa.nome); // Acesso permitido, "Alice" será impresso
```

2. **Private:** Membros marcados como `private` são acessíveis somente dentro da classe em que são definidos. Eles não podem ser acessados fora da classe.

```typescript
class ContaBancaria {
  private saldo: number;

  constructor(saldoInicial: number) {
    this.saldo = saldoInicial;
  }

  sacar(valor: number) {
    if (valor <= this.saldo) {
      this.saldo -= valor;
    }
  }
}

const conta = new ContaBancaria(1000);
console.log(conta.saldo); // Erro de compilação: 'saldo' é privado e não pode ser acessado
```

3. **Protected:** Membros marcados como `protected` são acessíveis dentro da classe onde são definidos e também em subclasses (herança). Eles não podem ser acessados fora da classe nem de instâncias da classe.

```typescript
class Animal {
  protected nome: string;

  constructor(nome: string) {
    this.nome = nome;
  }
}

class Cachorro extends Animal {
  latir() {
    console.log(`${this.nome} está latindo.`);
  }
}

const cachorro = new Cachorro("Rex");
console.log(cachorro.nome); // Erro de compilação: 'nome' é protegido e não pode ser acessado
cachorro.latir(); // Acesso permitido, "Rex está latindo." será impresso
```

É importante notar que os modificadores de acesso em TypeScript são aplicados durante a verificação de tipos em tempo de compilação, o que ajuda a evitar erros de acesso a membros indevidamente. Eles também são úteis para encapsular o comportamento de uma classe, tornando-a mais segura e flexível.

Em resumo, os modificadores de acesso `public`, `private` e `protected` são usados em TypeScript para controlar o acesso aos membros de uma classe, ajudando a manter a encapsulação e a segurança de seus objetos e classes. 