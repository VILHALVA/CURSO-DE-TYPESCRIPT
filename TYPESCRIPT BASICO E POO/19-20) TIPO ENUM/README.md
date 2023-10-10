# TIPO ENUM
Em TypeScript, o tipo `enum` (enumeração) é uma construção que permite definir um conjunto nomeado de constantes com valores associados. Isso torna mais fácil representar um conjunto predefinido de valores em seu código, fornecendo nomes significativos para cada um desses valores.

Aqui está como você pode definir e usar um `enum` em TypeScript:

```typescript
enum DiasDaSemana {
  Segunda,    // 0
  Terça,      // 1
  Quarta,     // 2
  Quinta,     // 3
  Sexta,      // 4
  Sábado,     // 5
  Domingo     // 6
}
```

Neste exemplo, criamos um `enum` chamado `DiasDaSemana` que representa os dias da semana. Os valores dentro do `enum` são automaticamente atribuídos a números inteiros, começando por 0. Portanto, `Segunda` é associado a 0, `Terça` a 1, e assim por diante.

Você pode usar os valores do `enum` em seu código da seguinte maneira:

```typescript
let dia: DiasDaSemana = DiasDaSemana.Quarta;

if (dia === DiasDaSemana.Sábado || dia === DiasDaSemana.Domingo) {
  console.log("É fim de semana!");
} else {
  console.log("É um dia de semana.");
}
```

Neste exemplo, `dia` é declarado como uma variável do tipo `DiasDaSemana` e atribuído o valor `DiasDaSemana.Quarta`. Em seguida, usamos uma estrutura condicional para verificar se o valor de `dia` corresponde a um dos dias do fim de semana (Sábado ou Domingo) e exibimos uma mensagem apropriada.

Os `enums` são especialmente úteis quando você precisa representar um conjunto fixo de valores que têm um significado específico em seu código. Isso torna o código mais legível e menos propenso a erros, pois você não precisa lembrar de valores numéricos específicos. Além disso, o TypeScript também oferece a capacidade de atribuir valores personalizados a elementos do `enum`, caso você precise de valores diferentes dos padrões numéricos automáticos.