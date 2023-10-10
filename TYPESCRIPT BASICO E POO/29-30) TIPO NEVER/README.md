# TIPO NEVER
O tipo `never` é um tipo especial em TypeScript que representa um valor que nunca ocorre ou uma função que nunca retorna. Ele é frequentemente usado para indicar situações que resultam em erros ou lançam exceções, ou para funções que entram em um loop infinito, de modo que nunca retornam normalmente.

Aqui estão algumas situações em que o tipo `never` é comumente usado:

1. **Funções que lançam exceções:**

   ```typescript
   function erro(mensagem: string): never {
     throw new Error(mensagem);
   }

   erro("Isso é um erro!"); // A função nunca retorna normalmente
   ```

   Neste exemplo, a função `erro` lança uma exceção e, portanto, nunca retorna normalmente. Ela é do tipo `never`.

2. **Funções que entram em loop infinito:**

   ```typescript
   function loopInfinito(): never {
     while (true) {
       console.log("Isso é um loop infinito!");
     }
   }

   loopInfinito(); // A função nunca retorna normalmente
   ```

   A função `loopInfinito` entra em um loop infinito e nunca retorna normalmente. Portanto, seu tipo é `never`.

3. **Funções que não podem ser alcançadas:**

   ```typescript
   function funcaoInalcançavel(): never {
     throw new Error("Essa função não deveria ser chamada.");
   }

   function condicional(flag: boolean): string {
     if (flag) {
       return "Verdadeiro";
     } else {
       return funcaoInalcançavel(); // Chamando uma função que lança uma exceção
     }
   }
   ```

   Neste caso, a função `funcaoInalcançavel` lança uma exceção e, portanto, a função `condicional` nunca retornará com o valor de `funcaoInalcançavel`. Assim, seu tipo de retorno é `never`.

O tipo `never` é útil para indicar que algo inesperado aconteceu em seu código e que a execução não deve continuar normalmente. É uma maneira eficaz de lidar com situações excepcionais e garantir que erros sejam identificados durante a análise de tipo em tempo de compilação.

Além disso, é importante observar que `never` é um subtipo de todos os outros tipos em TypeScript, o que significa que você pode atribuir `never` a variáveis de outros tipos, mas não o contrário. Isso ocorre porque `never` representa um conjunto vazio de valores possíveis.