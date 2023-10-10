# DEFAULT PARAMETERS
Em TypeScript, assim como em JavaScript, você pode definir valores padrão para os parâmetros de uma função usando a sintaxe de "parâmetros padrão" (default parameters). Isso permite que você atribua valores pré-definidos aos parâmetros de uma função caso nenhum valor seja fornecido durante a chamada da função. Essa funcionalidade é útil quando você deseja garantir que uma função tenha valores válidos mesmo quando alguns parâmetros são omitidos.

Aqui está a sintaxe para definir parâmetros padrão em TypeScript:

```typescript
function nomeDaFuncao(parametro1: tipo = valorPadrao1, parametro2: tipo = valorPadrao2, ...) {
  // Corpo da função
}
```

Aqui estão alguns exemplos de como usar parâmetros padrão:

```typescript
// Exemplo 1: Função com um parâmetro padrão
function saudacao(nome: string = "mundo") {
  console.log(`Olá, ${nome}!`);
}

saudacao();         // Saída: Olá, mundo!
saudacao("Alice");  // Saída: Olá, Alice!

// Exemplo 2: Função com múltiplos parâmetros padrão
function criarPessoa(nome: string, idade: number = 30, cidade: string = "Desconhecida") {
  console.log(`Nome: ${nome}, Idade: ${idade}, Cidade: ${cidade}`);
}

criarPessoa("Bob");               // Saída: Nome: Bob, Idade: 30, Cidade: Desconhecida
criarPessoa("Eve", 25);           // Saída: Nome: Eve, Idade: 25, Cidade: Desconhecida
criarPessoa("Alice", 28, "NYC");  // Saída: Nome: Alice, Idade: 28, Cidade: NYC
```

Nestes exemplos, os parâmetros `nome`, `idade`, e `cidade` têm valores padrão definidos. Se você chamar a função sem fornecer um valor para esses parâmetros, os valores padrão serão usados.

É importante observar que os parâmetros padrão devem sempre estar no final da lista de parâmetros da função. Isso ocorre porque, se você chamar a função com argumentos, eles devem corresponder na ordem aos parâmetros declarados.

Os parâmetros padrão são uma funcionalidade útil que torna suas funções mais flexíveis e facilita o fornecimento de valores predefinidos para parâmetros que podem ser omitidos durante a chamada da função. Isso é especialmente útil quando você deseja fornecer um comportamento padrão para funções, tornando-as mais versáteis em diferentes cenários de uso.