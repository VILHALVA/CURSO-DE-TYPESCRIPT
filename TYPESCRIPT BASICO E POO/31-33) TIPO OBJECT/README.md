# TIPO OBJECT
Em TypeScript, o tipo `object` é um tipo que representa qualquer objeto JavaScript não primitivo. Isso inclui objetos criados a partir de classes, objetos literais, funções e muito mais. Em resumo, o tipo `object` é usado para representar valores que não são dos tipos primitivos `number`, `string`, `boolean`, `null` ou `undefined`.

Aqui está como você pode usar o tipo `object` em TypeScript:

```typescript
let pessoa: object = { nome: "Alice", idade: 30 }; // Um objeto literal
let funcao: object = function() { console.log("Função!"); }; // Uma função

class Carro {
  constructor(marca: string) {
    this.marca = marca;
  }
  marca: string;
}

let meuCarro: object = new Carro("Toyota"); // Uma instância de classe
```

No exemplo acima, `pessoa` é uma variável do tipo `object` que armazena um objeto literal com propriedades `nome` e `idade`. `funcao` é uma variável que armazena uma função. `meuCarro` é uma variável que armazena uma instância de uma classe `Carro`.

Embora o tipo `object` possa representar qualquer objeto não primitivo, ele tem limitações quando se trata de acessar propriedades e métodos desses objetos. Uma variável do tipo `object` permite apenas acessar propriedades e métodos que são comuns a todos os objetos, ou seja, aqueles definidos no próprio tipo `object`. Isso significa que você não pode acessar propriedades ou chamar métodos específicos de objetos que não são do tipo `object`.

```typescript
let pessoa: object = { nome: "Alice", idade: 30 };
console.log(pessoa.nome); // Erro: Propriedade 'nome' não existe no tipo 'object'.
```

Para acessar propriedades específicas de um objeto, é recomendável usar interfaces ou tipos personalizados para descrever a estrutura do objeto com mais precisão. Isso permitirá que o TypeScript forneça informações de tipo mais úteis durante o desenvolvimento.

```typescript
interface Pessoa {
  nome: string;
  idade: number;
}

let pessoa: Pessoa = { nome: "Alice", idade: 30 };
console.log(pessoa.nome); // Isso funciona corretamente porque 'pessoa' tem o tipo 'Pessoa'.
```

Em resumo, o tipo `object` em TypeScript é usado para representar qualquer objeto JavaScript não primitivo. Embora seja genérico e flexível, é mais comum usar interfaces ou tipos personalizados para descrever objetos com precisão e obter benefícios completos do sistema de tipos do TypeScript.