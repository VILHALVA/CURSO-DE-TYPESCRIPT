# TIPO STRING
Em TypeScript, o tipo `string` é usado para representar dados textuais, como palavras, frases, ou qualquer sequência de caracteres. Strings são um dos tipos de dados mais comuns em linguagens de programação e são amplamente utilizadas em aplicativos para armazenar e manipular informações de texto.

Aqui está como você pode declarar e usar variáveis do tipo `string` em TypeScript:

```typescript
let nome: string = "Alice";  // Declarando uma variável 'nome' do tipo string
let saudacao: string = `Olá, ${nome}!`;  // Usando templates de string para criar uma mensagem
```

Neste exemplo, `nome` é declarada como uma variável do tipo `string`, contendo o valor "Alice". Em seguida, usamos uma string interpolada (template de string) para criar uma saudação personalizada usando o valor da variável `nome`.

Além disso, o tipo `string` também é comumente usado para representar caminhos de arquivo, URLs, texto HTML e muito mais.

Operações com strings são amplamente suportadas em TypeScript. Você pode usar operadores para concatenar strings, acessar caracteres individuais e muito mais:

```typescript
let palavra1: string = "Olá, ";
let palavra2: string = "mundo!";
let frase: string = palavra1 + palavra2; // Concatenando strings

let primeiraLetra: string = palavra1[0]; // Acessando o primeiro caractere
```

Além disso, TypeScript oferece uma série de métodos e funções para manipulação de strings, como `length`, `charAt`, `substring`, `toUpperCase`, `toLowerCase`, entre outros.

```typescript
let texto: string = "Exemplo de manipulação de strings";
let tamanho: number = texto.length; // Obtendo o tamanho da string
let caractere: string = texto.charAt(0); // Obtendo o primeiro caractere
let subtexto: string = texto.substring(8, 15); // Obtendo uma parte da string
let maiusculas: string = texto.toUpperCase(); // Convertendo para maiúsculas
let minusculas: string = texto.toLowerCase(); // Convertendo para minúsculas
```

Em resumo, o tipo `string` em TypeScript é usado para representar dados textuais e é amplamente utilizado em aplicativos para lidar com texto, mensagens, conteúdo da web e muito mais. É importante lembrar que strings são imutáveis em JavaScript/TypeScript, o que significa que, uma vez criadas, elas não podem ser modificadas; você cria novas strings com base nas operações que realiza.