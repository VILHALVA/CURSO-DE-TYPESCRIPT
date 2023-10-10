# TIPO VOID
Em TypeScript, o tipo `void` é usado para indicar que uma função não retorna nenhum valor. Isso significa que a função pode realizar alguma ação, mas não produzirá um resultado que pode ser atribuído a uma variável. O tipo `void` também pode ser usado como o tipo de retorno de uma função para indicar explicitamente que a função não tem um valor de retorno.

Aqui estão algumas maneiras de usar o tipo `void` em TypeScript:

1. **Funções que não retornam valor:**

   ```typescript
   function mostrarMensagem(): void {
     console.log("Olá, mundo!");
   }

   mostrarMensagem(); // Chama a função que não retorna um valor
   ```

   Neste exemplo, a função `mostrarMensagem` não retorna nenhum valor, indicado pelo tipo `void`. Ela apenas imprime uma mensagem no console.

2. **Funções com tipo de retorno `void`:**

   ```typescript
   function saudacao(nome: string): void {
     console.log(`Olá, ${nome}!`);
   }

   let resultado: void = saudacao("Alice"); // 'resultado' é do tipo 'void'
   ```

   A função `saudacao` aceita um argumento `nome` e não retorna nenhum valor útil, portanto, seu tipo de retorno é explicitamente especificado como `void`.

3. **Funções de retorno de callback:**

   O tipo `void` é frequentemente usado em funções de retorno de chamadas (callbacks) que são usadas para realizar tarefas assíncronas, como operações de I/O. Essas funções podem executar ações, mas não retornam valores diretamente.

   ```typescript
   function processarDados(callback: () => void): void {
     // Realiza algum processamento
     callback(); // Chama a função de retorno de callback
   }

   processarDados(() => {
     console.log("Dados processados com sucesso.");
   });
   ```

   Neste exemplo, `processarDados` aceita uma função de retorno de callback que não retorna um valor. A função de callback é chamada após o processamento de dados.

Em resumo, o tipo `void` em TypeScript é usado para indicar que uma função não retorna um valor ou como o tipo de retorno de uma função que não tem valor de retorno útil. É útil para funções que realizam ações, como impressão no console ou execução de tarefas assíncronas, mas não geram resultados que precisam ser atribuídos a variáveis.