# EXTENDS INTERFACES
Em TypeScript, você pode estender interfaces, o que significa criar uma nova interface que herda propriedades e métodos de outra interface existente. Isso é útil quando você deseja adicionar ou sobrescrever membros em uma nova interface, mantendo os membros da interface base. A herança de interfaces permite criar hierarquias de interfaces para descrever diferentes aspectos de um objeto ou comportamento.

Aqui está a sintaxe para estender interfaces em TypeScript:

```typescript
interface InterfaceBase {
  propriedadeBase: string;
  metodoBase(): void;
}

interface InterfaceEstendida extends InterfaceBase {
  novaPropriedade: number;
  novoMetodo(): string;
}
```

Neste exemplo, `InterfaceEstendida` estende `InterfaceBase`, o que significa que `InterfaceEstendida` herda `propriedadeBase` e `metodoBase` da `InterfaceBase`. Além disso, `InterfaceEstendida` adiciona novos membros, `novaPropriedade` e `novoMetodo`, que são exclusivos dela.

Aqui está um exemplo prático:

```typescript
interface Veículo {
  marca: string;
  ano: number;
}

interface Carro extends Veículo {
  modelo: string;
}

const meuCarro: Carro = {
  marca: "Toyota",
  ano: 2022,
  modelo: "Corolla",
};

console.log(`Marca: ${meuCarro.marca}`);
console.log(`Ano: ${meuCarro.ano}`);
console.log(`Modelo: ${meuCarro.modelo}`);
```

Neste exemplo, temos duas interfaces: `Veículo` e `Carro`. A interface `Carro` estende a interface `Veículo`, o que significa que ela herda as propriedades `marca` e `ano`. Além disso, a interface `Carro` adiciona a propriedade `modelo`. O objeto `meuCarro` segue o contrato da interface `Carro`, incluindo todas as propriedades herdadas e a nova propriedade.

Extender interfaces é útil para criar abstrações mais específicas e reutilizáveis em seu código. Isso ajuda a criar estruturas de código mais organizadas e a manter a legibilidade e manutenibilidade do seu código. 