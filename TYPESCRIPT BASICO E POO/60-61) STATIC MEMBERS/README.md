# STATIC MEMBERS
Membros estáticos (ou "static members") em TypeScript são membros de classe que pertencem à própria classe, não às instâncias individuais da classe. Isso significa que você pode acessar membros estáticos diretamente na classe, sem a necessidade de criar uma instância da classe. Os membros estáticos são compartilhados por todas as instâncias da classe e são usados principalmente para armazenar informações ou comportamentos que se aplicam à classe como um todo, em vez de a uma instância específica.

Para definir membros estáticos em TypeScript, você usa a palavra-chave `static` antes da declaração da propriedade ou do método dentro da classe. Aqui está um exemplo de como usar membros estáticos:

```typescript
class Calculadora {
  static pi: number = 3.14159;

  static calcularCircunferencia(raio: number): number {
    return 2 * this.pi * raio;
  }
}

console.log(Calculadora.pi); // Saída: 3.14159

const raio = 5;
const circunferencia = Calculadora.calcularCircunferencia(raio);
console.log(`Circunferência com raio ${raio} = ${circunferência}`); // Saída: Circunferência com raio 5 = 31.4159
```

Neste exemplo, a classe `Calculadora` possui um membro estático `pi`, que armazena o valor de π, e um método estático `calcularCircunferencia` que calcula a circunferência de um círculo com base no raio fornecido. Você pode acessar tanto a propriedade `pi` quanto o método `calcularCircunferencia` diretamente na classe `Calculadora` sem criar uma instância da classe.

Os membros estáticos são úteis para armazenar constantes, funções de utilidade geral ou qualquer informação que seja compartilhada por todas as instâncias da classe. Eles são especialmente úteis quando você deseja encapsular funcionalidades relacionadas à classe, em vez de associá-las a instâncias individuais.

Lembre-se de que os membros estáticos não têm acesso às propriedades ou métodos de instâncias da classe, pois eles pertencem à classe em si. Portanto, eles são chamados usando o nome da classe, como `Calculadora.pi` no exemplo acima. 