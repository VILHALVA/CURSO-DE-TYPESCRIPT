# TIPO UNKNOWN
O tipo `unknown` é uma adição ao TypeScript que foi introduzida para ser uma alternativa mais segura ao tipo `any`. Enquanto o tipo `any` permite que uma variável seja de qualquer tipo, o tipo `unknown` impõe restrições adicionais para tornar o código mais seguro em termos de tipos.

Aqui está como o tipo `unknown` funciona em TypeScript:

1. **Atribuição Inicial Restrita:** Quando você declara uma variável como `unknown`, você pode atribuir qualquer valor a ela, mas essa variável não pode ser usada diretamente até que seu tipo seja "prova" de que é seguro fazer isso.

   ```typescript
   let valor: unknown = 42;
   let texto: string = valor; // Erro: O tipo 'unknown' não pode ser atribuído ao tipo 'string'.
   ```

   No exemplo acima, mesmo que `valor` tenha sido inicializado com um número, não é seguro atribuí-lo diretamente a uma variável de tipo `string`.

2. **Verificação de Tipo:** Para usar uma variável do tipo `unknown`, você deve primeiro verificar e garantir o tipo correto. Isso é feito por meio de estruturas condicionais, como `typeof`, `instanceof`, ou usando type guards.

   ```typescript
   let valor: unknown = "Texto desconhecido";
   if (typeof valor === "string") {
     let texto: string = valor; // Agora é seguro atribuir
   }
   ```

   Usando `typeof` neste exemplo, verificamos se `valor` é uma string antes de atribuí-lo a `texto`.

3. **Tipo de Retorno de Função:** Quando você define uma função com o tipo de retorno `unknown`, é necessário que a função retorne um valor do tipo `unknown` ou que use verificação de tipo para garantir que o valor retornado seja do tipo correto.

   ```typescript
   function parseJson(jsonString: string): unknown {
     try {
       return JSON.parse(jsonString);
     } catch (error) {
       return "Erro na análise JSON";
     }
   }

   let resultado = parseJson('{"chave": "valor"}');
   if (typeof resultado === "object") {
     console.log(resultado.chave); // É seguro acessar 'chave' após a verificação de tipo
   }
   ```

   Neste exemplo, a função `parseJson` retorna um valor do tipo `unknown`, e nós verificamos o tipo do resultado antes de acessar suas propriedades.

O tipo `unknown` é uma ferramenta útil para lidar com valores de origem desconhecida e, ao mesmo tempo, manter a segurança de tipos em seu código TypeScript. Ele ajuda a evitar erros relacionados a tipos e torna seu código mais robusto e seguro. É uma boa prática usar `unknown` sempre que você não tem certeza sobre o tipo de dado que está manipulando.