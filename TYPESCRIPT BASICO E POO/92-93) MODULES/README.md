# MODULES
Módulos em TypeScript são uma maneira de organizar e estruturar seu código em partes separadas e reutilizáveis. Eles são essenciais para a construção de aplicativos maiores e mais fáceis de manter, permitindo dividir o código em partes menores e gerenciáveis.

Aqui está uma visão geral básica dos módulos em TypeScript:

1. **Declaração de Módulos:**

   Em TypeScript, você pode criar módulos usando a palavra-chave `module` (módulo). Um módulo é basicamente um arquivo TypeScript que agrupa classes, funções ou variáveis relacionadas. Por exemplo:

   ```typescript
   // Arquivo: minhasFuncoes.ts
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

   Para usar módulos em outros arquivos, você deve importá-los usando a palavra-chave `import` (importar). Por exemplo:

   ```typescript
   // Arquivo: principal.ts
   import { MinhasFuncoes } from "./minhasFuncoes";

   const resultadoSoma = MinhasFuncoes.somar(5, 3);
   const resultadoSubtracao = MinhasFuncoes.subtrair(10, 7);
   ```

   Neste exemplo, importamos o módulo `MinhasFuncoes` do arquivo `minhasFuncoes.ts` e usamos suas funções no arquivo `principal.ts`.

3. **Exportação de Módulos:**

   Para tornar classes, funções ou variáveis disponíveis para outros módulos, você deve exportá-los usando as palavras-chave `export` (exportar). Por exemplo:

   ```typescript
   // Arquivo: minhaClasse.ts
   export class MinhaClasse {
     constructor(public nome: string) {}
   }
   ```

   Neste exemplo, exportamos a classe `MinhaClasse`, tornando-a acessível a outros módulos.

4. **Módulos em Pastas:**

   Você também pode organizar seus módulos em pastas. Cada arquivo TypeScript em uma pasta é considerado um módulo separado. Por exemplo:

   ```
   minhaPasta/
   ├── moduloA.ts
   ├── moduloB.ts
   └── principal.ts
   ```

   Você pode importar módulos de outras pastas usando caminhos relativos ou absolutos, como `import { MinhaFuncao } from "./minhaPasta/moduloA"`.

5. **Exportação Padrão:**

   Além de exportar membros individuais, você pode exportar um membro padrão de um módulo usando a sintaxe `export default` (exportar padrão). Isso permite importar esse membro sem usar chaves de desestruturação. Por exemplo:

   ```typescript
   // Arquivo: meuModulo.ts
   const mensagem = "Olá, mundo!";
   export default mensagem;
   ```

   ```typescript
   // Arquivo: principal.ts
   import mensagem from "./meuModulo";
   console.log(mensagem); // "Olá, mundo!"
   ```

Módulos são essenciais para estruturar seu código em aplicativos TypeScript maiores. Eles promovem a organização do código, reutilização e manutenção, permitindo dividir o código em partes lógicas e gerenciáveis. Você pode usar módulos para criar uma arquitetura modular e escalável para seus projetos TypeScript. 