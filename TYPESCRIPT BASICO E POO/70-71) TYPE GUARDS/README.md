# TYPE GUARDS
Os "Type guards" (guardas de tipo) são recursos em TypeScript que permitem testar e garantir que um valor seja de um tipo específico em tempo de execução. Eles são úteis quando você está trabalhando com tipos de união, interfaces e tipos personalizados e deseja realizar operações condicionais com base no tipo real de um valor.

Existem várias maneiras de criar "type guards" em TypeScript. Vamos explorar algumas delas:

1. **Verificação de tipo com `typeof`:** Você pode usar a palavra-chave `typeof` para verificar o tipo de variáveis primitivas, como strings, números e booleanos.

```typescript
function éString(valor: any): valor é string {
  return typeof valor === "string";
}

const x = "Olá, mundo!";
if (éString(x)) {
  console.log(x.toUpperCase()); // Válido, pois x é uma string
} else {
  console.log("x não é uma string.");
}
```

2. **Verificação de tipo com `instanceof`:** O operador `instanceof` é usado para verificar se um objeto é uma instância de uma classe.

```typescript
class Animal {
  nome: string;

  constructor(nome: string) {
    this.nome = nome;
  }
}

class Cachorro extends Animal {
  latir() {
    console.log("Woof! Woof!");
  }
}

function éCachorro(animal: Animal): animal é Cachorro {
  return animal instanceof Cachorro;
}

const meuAnimal: Animal = new Cachorro("Rex");

if (éCachorro(meuAnimal)) {
  meuAnimal.latir(); // Válido, pois meuAnimal é um Cachorro
}
```

3. **Verificação de tipo com propriedades ou métodos:** Você pode usar a presença de propriedades ou métodos específicos para verificar o tipo de um objeto.

```typescript
interface Carro {
  marca: string;
  modelo: string;
}

interface Moto {
  marca: string;
  cilindradas: number;
}

function éCarro(veículo: Carro | Moto): veículo é Carro {
  return "modelo" in veículo;
}

const meuVeículo: Carro | Moto = { marca: "Toyota", modelo: "Corolla" };

if (éCarro(meuVeículo)) {
  console.log(`Modelo: ${meuVeículo.modelo}`); // Válido, pois meuVeículo é um Carro
}
```

4. **Verificação de tipo com `as`: Você pode usar a sintaxe `as` para fazer uma conversão explícita de tipo e, ao mesmo tempo, informar ao TypeScript que você está confiante de que o valor é do tipo especificado.

```typescript
function duplicar(valor: string | number): string {
  if (typeof valor === "string") {
    // Usando type guard com as
    return valor + valor;
  } else {
    return (valor * 2).toString();
  }
}

const resultado1 = duplicar("123"); // "123123"
const resultado2 = duplicar(4);     // "8"
```

Os "type guards" são úteis para lidar com tipos de união de forma segura e para garantir que as operações sejam realizadas apenas nos valores que têm o tipo esperado. Eles ajudam a evitar erros de tempo de execução e tornam seu código mais robusto. 