# INTERFACES
Em TypeScript, as interfaces são um recurso poderoso que permite definir contratos para a estrutura de um objeto. As interfaces são usadas para declarar a forma esperada de um objeto, especificando quais propriedades e métodos ele deve ter. Isso ajuda a garantir que os objetos cumpram determinados requisitos sem a necessidade de herança de classe.

Para definir uma interface em TypeScript, você usa a palavra-chave `interface`. Aqui está uma sintaxe básica:

```typescript
interface Pessoa {
  nome: string;
  idade: number;
}

const pessoa: Pessoa = {
  nome: "Alice",
  idade: 30,
};
```

Neste exemplo, definimos uma interface chamada `Pessoa` que descreve a estrutura esperada de um objeto Pessoa, incluindo as propriedades `nome` e `idade`. Em seguida, criamos um objeto `pessoa` que segue o contrato da interface `Pessoa`.

Interfaces podem ser usadas em vários contextos em TypeScript:

1. **Declaração de objeto:** Você pode usar interfaces para definir a estrutura de objetos. Isso é útil para garantir que os objetos tenham as propriedades corretas.

```typescript
interface Ponto {
  x: number;
  y: number;
}

const ponto: Ponto = { x: 10, y: 20 };
```

2. **Implementação de classes:** Você pode implementar interfaces em classes para garantir que a classe tenha os métodos e propriedades definidos na interface.

```typescript
interface Animal {
  fazerBarulho(): void;
}

class Cachorro implements Animal {
  fazerBarulho() {
    console.log("Woof! Woof!");
  }
}
```

3. **Extensão de interfaces:** Você pode estender uma interface com outra interface para adicionar ou sobrescrever propriedades e métodos.

```typescript
interface Forma {
  cor: string;
}

interface Retângulo extends Forma {
  largura: number;
  altura: number;
}
```

4. **Uso em parâmetros de função:** Você pode usar interfaces para especificar o formato esperado dos argumentos de uma função.

```typescript
interface Opções {
  nome: string;
  idade: number;
}

function saudacao(opcoes: Opções) {
  console.log(`Olá, ${opcoes.nome}! Você tem ${opcoes.idade} anos.`);
}
```

As interfaces são uma ferramenta poderosa para criar código mais seguro, flexível e legível. Elas ajudam a documentar a estrutura dos objetos e a garantir que seu código siga contratos específicos. Além disso, as interfaces são frequentemente usadas em conjunto com tipos genéricos para criar abstrações reutilizáveis em TypeScript. 