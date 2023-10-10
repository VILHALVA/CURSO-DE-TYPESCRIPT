# GENERIC CLASSES
Em TypeScript, você pode criar classes genéricas que permitem que você crie classes que podem ser parametrizadas por tipos. Isso significa que você pode escrever uma classe que funcione com diferentes tipos de dados, enquanto ainda mantém a segurança de tipos. As classes genéricas são especialmente úteis quando você deseja criar estruturas de dados ou componentes que podem ser reutilizados com tipos diferentes.

Aqui está a sintaxe geral para criar uma classe genérica:

```typescript
class NomeDaClasse<TipoGenérico> {
  // Propriedades e métodos da classe que podem usar o TipoGenérico
}
```

Aqui estão alguns exemplos de como criar e usar classes genéricas:

**Exemplo 1: Uma classe genérica simples:**

```typescript
class Caixa<T> {
  private valor: T;

  constructor(valor: T) {
    this.valor = valor;
  }

  obterValor(): T {
    return this.valor;
  }
}

const caixaDeNúmero = new Caixa<number>(42);
const númeroArmazenado: number = caixaDeNúmero.obterValor();

const caixaDeTexto = new Caixa<string>("Olá, mundo!");
const textoArmazenado: string = caixaDeTexto.obterValor();
```

Neste exemplo, criamos a classe genérica `Caixa`, que pode armazenar e retornar valores de qualquer tipo `T`. Usamos `number` e `string` como tipos concretos ao instanciar objetos `Caixa`.

**Exemplo 2: Uma classe genérica com restrições de tipo:**

```typescript
interface Animal {
  nome: string;
}

class ColeçãoDeAnimais<T extends Animal> {
  private animais: T[] = [];

  adicionar(animal: T): void {
    this.animais.push(animal);
  }

  listarNomes(): string[] {
    return this.animais.map((animal) => animal.nome);
  }
}

const coleçãoDeCachorros = new ColeçãoDeAnimais<{ nome: string }>();
coleçãoDeCachorros.adicionar({ nome: "Rex" });
coleçãoDeCachorros.adicionar({ nome: "Fido" });

const nomesDeCachorros: string[] = coleçãoDeCachorros.listarNomes();
```

Neste exemplo, criamos a classe genérica `ColeçãoDeAnimais`, que pode ser usada para armazenar objetos que implementam a interface `Animal`. A restrição `T extends Animal` garante que apenas objetos com a estrutura de `Animal` possam ser armazenados na coleção.

As classes genéricas são uma maneira poderosa de criar componentes reutilizáveis que podem funcionar com diferentes tipos de dados. Elas ajudam a melhorar a segurança de tipos e a reduzir a duplicação de código, tornando o código mais flexível e eficiente. 