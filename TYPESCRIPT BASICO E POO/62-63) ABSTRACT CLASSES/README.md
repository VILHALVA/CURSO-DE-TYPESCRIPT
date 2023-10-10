# ABSTRACT CLASSES
As classes abstratas em TypeScript são classes que não podem ser instanciadas diretamente, mas servem como modelos para outras classes que são derivadas delas. Elas são usadas para definir interfaces, propriedades e métodos que as classes derivadas devem implementar. As classes abstratas são úteis quando você deseja criar uma estrutura comum para várias classes relacionadas, garantindo que determinados membros e comportamentos estejam presentes nas subclasses.

Para definir uma classe abstrata em TypeScript, você usa a palavra-chave `abstract` antes da declaração da classe. Além disso, você pode declarar membros (propriedades ou métodos) como abstratos usando a palavra-chave `abstract`, mas esses membros não podem ter uma implementação dentro da classe abstrata.

Aqui está um exemplo de como usar classes abstratas em TypeScript:

```typescript
abstract class Forma {
  cor: string;

  constructor(cor: string) {
    this.cor = cor;
  }

  // Método abstrato que deve ser implementado nas subclasses
  abstract calcularArea(): number;
}

class Retângulo extends Forma {
  largura: number;
  altura: number;

  constructor(cor: string, largura: number, altura: number) {
    super(cor);
    this.largura = largura;
    this.altura = altura;
  }

  calcularArea(): number {
    return this.largura * this.altura;
  }
}

class Círculo extends Forma {
  raio: number;

  constructor(cor: string, raio: number) {
    super(cor);
    this.raio = raio;
  }

  calcularArea(): number {
    return Math.PI * this.raio ** 2;
  }
}

const retângulo = new Retângulo("vermelho", 5, 10);
const círculo = new Círculo("azul", 3);

console.log(`Área do retângulo: ${retângulo.calcularArea()}`);
console.log(`Área do círculo: ${círculo.calcularArea()}`);
```

Neste exemplo, a classe `Forma` é uma classe abstrata que possui uma propriedade `cor` e um método abstrato `calcularArea()`. As subclasses `Retângulo` e `Círculo` herdam da classe `Forma` e implementam o método `calcularArea()` de acordo com suas respectivas formas geométricas.

É importante notar que as classes abstratas não podem ser instanciadas diretamente, mas você pode criar instâncias de suas subclasses. Além disso, as subclasses devem fornecer uma implementação para todos os métodos abstratos da classe abstrata, caso contrário, ocorrerá um erro de compilação.

As classes abstratas são úteis quando você deseja definir uma estrutura comum para várias classes relacionadas e garantir que certos membros e comportamentos sejam implementados nas subclasses. Elas ajudam a criar um código mais organizado e orientado a objetos. 