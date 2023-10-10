# GENERICS INTERFACES
Em TypeScript, você pode criar interfaces genéricas que permitem definir estruturas de dados flexíveis que podem trabalhar com vários tipos de dados, mantendo a segurança de tipos. Isso é particularmente útil quando você deseja definir interfaces para objetos que podem ter diferentes formatos, mas ainda precisa de verificação de tipos.

Aqui está a sintaxe geral para criar uma interface genérica:

```typescript
interface NomeDaInterface<TipoGenérico> {
  // Definição de propriedades e métodos que podem usar o TipoGenérico
}
```

Aqui estão alguns exemplos de como criar e usar interfaces genéricas:

**Exemplo 1: Interface genérica simples:**

```typescript
interface Caixa<T> {
  valor: T;
}

const caixaDeNúmero: Caixa<number> = { valor: 42 };
const caixaDeTexto: Caixa<string> = { valor: "Olá, mundo!" };
```

Neste exemplo, criamos a interface genérica `Caixa`, que pode ser usada para definir objetos com uma propriedade `valor` de qualquer tipo `T`. Usamos `number` e `string` como tipos concretos ao criar objetos `Caixa`.

**Exemplo 2: Interface genérica com métodos:**

```typescript
interface Lista<T> {
  adicionar(item: T): void;
  listar(): T[];
}

class ListaDeNúmeros implements Lista<number> {
  private itens: number[] = [];

  adicionar(item: number): void {
    this.itens.push(item);
  }

  listar(): number[] {
    return this.itens;
  }
}

const listaDeNúmeros = new ListaDeNúmeros();
listaDeNúmeros.adicionar(1);
listaDeNúmeros.adicionar(2);
const números: number[] = listaDeNúmeros.listar();
```

Neste exemplo, criamos a interface genérica `Lista` que define métodos para adicionar e listar itens de qualquer tipo `T`. A classe `ListaDeNúmeros` implementa essa interface com o tipo concreto `number`.

**Exemplo 3: Interface genérica com tipos de retorno genéricos:**

```typescript
interface Função<T, R> {
  (param: T): R;
}

const duplicar: Função<number, number> = (x) => x * 2;
const cumprimentar: Função<string, string> = (nome) => `Olá, ${nome}!`;
```

Neste exemplo, criamos a interface genérica `Função` que representa uma função com um parâmetro de tipo `T` e um tipo de retorno `R`. Em seguida, criamos funções concretas com tipos específicos ao usar a interface genérica.

As interfaces genéricas são úteis quando você deseja definir estruturas de dados ou contratos de objeto que funcionem com vários tipos de dados. Elas fornecem uma maneira de criar abstrações seguras de tipos em TypeScript, permitindo que você escreva código flexível e reutilizável. 