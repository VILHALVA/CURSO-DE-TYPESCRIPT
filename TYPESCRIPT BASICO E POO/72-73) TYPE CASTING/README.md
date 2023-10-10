# TYPE CASTING
Type casting, ou conversão de tipo, é um recurso em TypeScript que permite que você explicitamente converta um valor de um tipo para outro tipo quando você tem certeza de que a conversão é segura. O TypeScript oferece duas formas principais de realizar type casting: usando a sintaxe `as` e usando o operador angular `<>`.

1. **Type Casting com `as`:** A sintaxe `as` é uma maneira segura de realizar type casting em TypeScript. Você usa a palavra-chave `as` seguida do tipo para o qual deseja converter o valor.

```typescript
const valor: any = "123";
const número: number = valor as number; // Conversão de string para number

console.log(número); // 123
```

2. **Type Casting com `<>` (Angular Brackets):** Esta é outra forma de realizar type casting, mas não é tão segura quanto o `as`, pois pode causar erros em tempo de compilação se não for feita corretamente.

```typescript
const valor: any = "123";
const número: number = <number>valor; // Conversão de string para number

console.log(número); // 123
```

É importante notar que, embora type casting seja uma maneira de converter um valor de um tipo para outro, ele não realiza uma conversão real dos dados em tempo de execução. Em vez disso, ele instrui o compilador TypeScript a tratá-lo como se fosse do tipo especificado. Isso significa que type casting não garante a integridade dos dados, e é responsabilidade do programador garantir que a conversão seja segura.

É aconselhável usar type casting com cuidado e apenas quando você tem certeza de que a conversão não resultará em erros em tempo de execução. Além disso, é uma boa prática usar outras técnicas, como type guards, para verificar e garantir a validade dos valores antes de realizar type casting. 