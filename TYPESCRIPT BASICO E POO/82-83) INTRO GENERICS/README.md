# INTRO GENERICS
Generics, em TypeScript, são um recurso poderoso que permite escrever código flexível e reutilizável, independentemente dos tipos de dados que você manipula. Eles permitem que você crie funções, classes e tipos que podem ser personalizados para trabalhar com diferentes tipos de dados, mantendo a segurança de tipos.

A principal ideia por trás dos generics é criar código que não seja específico de um tipo, mas que possa ser adaptado para trabalhar com vários tipos de dados sem comprometer a segurança de tipos.

Aqui está uma introdução básica ao uso de generics em TypeScript:

1. **Funções Genéricas:**

   Você pode criar funções genéricas que trabalham com diferentes tipos de entrada. Por exemplo, uma função que retorna o primeiro elemento de um array, independentemente do tipo do array:

   ```typescript
   function primeiroElemento<T>(array: T[]): T | undefined {
     return array.length > 0 ? array[0] : undefined;
   }

   const números = [1, 2, 3, 4, 5];
   const primeiroNúmero: number | undefined = primeiroElemento(números);

   const palavras = ["maçã", "banana", "laranja"];
   const primeiraPalavra: string | undefined = primeiroElemento(palavras);
   ```

   Neste exemplo, `T` é um tipo genérico que pode ser qualquer tipo. A função `primeiroElemento` aceita um array de tipo `T` e retorna um valor do tipo `T` ou `undefined`.

2. **Classes Genéricas:**

   Você também pode criar classes genéricas. Por exemplo, uma classe genérica `Caixa` que pode armazenar um valor de qualquer tipo:

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

   Neste exemplo, a classe `Caixa` usa o tipo genérico `T` para armazenar e retornar valores de qualquer tipo.

3. **Tipos Genéricos:**

   Você pode criar tipos genéricos para definir estruturas de dados que funcionam com vários tipos. Por exemplo, um tipo genérico `Par` que representa um par de valores:

   ```typescript
   type Par<A, B> = {
     primeiro: A;
     segundo: B;
   };

   const parDeNúmeros: Par<number, number> = {
     primeiro: 10,
     segundo: 20,
   };

   const parDeStrings: Par<string, string> = {
     primeiro: "Olá",
     segundo: "Mundo",
   };
   ```

   Neste exemplo, o tipo `Par` é genérico e aceita dois tipos de argumentos, `A` e `B`.

Generics são especialmente úteis quando você deseja escrever código que seja flexível o suficiente para ser reutilizado com diferentes tipos de dados. Eles fornecem uma maneira de criar abstrações seguras de tipos em TypeScript, permitindo que você escreva código genérico que funciona com uma variedade de tipos sem comprometer a segurança de tipos.