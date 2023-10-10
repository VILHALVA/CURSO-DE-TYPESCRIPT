# INTRODUCION A MODULES
Módulos são uma parte importante do sistema de módulos em TypeScript e JavaScript, que permitem organizar e estruturar seu código em partes separadas e reutilizáveis. Isso é fundamental para projetos grandes e complexos, pois ajuda a dividir o código em arquivos menores e mais gerenciáveis, promovendo a reutilização e a manutenção do código.

Vamos dar uma introdução básica aos módulos em TypeScript:

1. **Declaração de Módulos:**

   Em TypeScript, você pode criar módulos usando a palavra-chave `module`. Um módulo é basicamente um arquivo TypeScript que agrupa um conjunto de classes, funções ou variáveis relacionadas. Por exemplo:

   ```typescript
   // arquivo: minhaFuncao.ts
   module MinhasFuncoes {
     export function somar(a: number, b: number): number {
       return a + b;
     }

     export function subtrair(a: number, b: number): number {
       return a - b;
     }
   }
   ```

   Neste exemplo, criamos um módulo chamado `MinhasFuncoes` que contém duas funções exportadas: `somar` e `subtrair`.

2. **Importação de Módulos:**

   Para usar módulos em outros arquivos, você deve importá-los usando a palavra-chave `import`. Por exemplo:

   ```typescript
   // arquivo: main.ts
   import { MinhasFuncoes } from "./minhaFuncao";

   const resultadoSoma = MinhasFuncoes.somar(5, 3);
   const resultadoSubtracao = MinhasFuncoes.subtrair(10, 7);
   ```

   Neste exemplo, importamos o módulo `MinhasFuncoes` do arquivo `minhaFuncao.ts` e usamos suas funções no arquivo `main.ts`.

3. **Exportação de Módulos:**

   Para tornar classes, funções ou variáveis disponíveis para outros módulos, você deve exportá-los usando as palavras-chave `export`. Por exemplo:

   ```typescript
   // arquivo: minhaClasse.ts
   export class MinhaClasse {
     constructor(public nome: string) {}
   }
   ```

   Neste exemplo, exportamos a classe `MinhaClasse`, tornando-a acessível a outros módulos.

4. **Módulos em Pasta:**

   Você também pode organizar seus módulos em pastas. Cada arquivo TypeScript em uma pasta é considerado um módulo separado. Por exemplo:

   ```
   minhaPasta/
   ├── moduloA.ts
   ├── moduloB.ts
   └── main.ts
   ```

   Você pode importar módulos de outras pastas usando o caminho relativo ou absoluto, como `import { MinhaFuncao } from "./minhaPasta/moduloA"`.

5. **Exportação Padrão:**

   Além da exportação de membros individuais, você pode exportar um membro padrão de um módulo usando a palavra-chave `export default`. Isso permite que você importe esse membro sem usar chaves de desestruturação. Por exemplo:

   ```typescript
   // arquivo: meuModulo.ts
   const mensagem = "Olá, mundo!";
   export default mensagem;
   ```

   ```typescript
   // arquivo: main.ts
   import mensagem from "./meuModulo";
   console.log(mensagem); // "Olá, mundo!"
   ```

Essa é uma introdução básica ao uso de módulos em TypeScript. Eles são uma parte fundamental da estruturação de código em projetos maiores e permitem uma melhor organização, reutilização e manutenção do código. Você pode usar módulos para dividir seu código em partes lógicas e criar uma arquitetura mais modular e escalável. 