# SATISFIES OPERATOR
As palavras-chave "satisfies" e "satisfies property" não são parte do idioma TypeScript. Pode ser um equívoco ou confusão com relação aos conceitos e sintaxes existentes em TypeScript.

Se referindo à verificação de propriedades ou satisfação de tipos, normalmente usamos "extends" para isso, especialmente ao trabalhar com tipos condicionais e parâmetros de tipos genéricos. O operador `extends` é usado para garantir que um tipo satisfaça uma determinada condição.

Aqui está um exemplo de como usamos o operador `extends` para garantir que um tipo satisfaça uma propriedade específica:

```typescript
type TemPropriedadeNome<T> = T extends { nome: any } ? true : false;

interface Pessoa {
  nome: string;
  idade: number;
}

const possuiNome: TemPropriedadeNome<Pessoa> = true; // Retorna true porque Pessoa possui a propriedade "nome"
```

Neste exemplo, estamos criando um tipo condicional `TemPropriedadeNome` que verifica se um tipo `T` possui uma propriedade "nome". Se possuir, o tipo condicional retorna `true`, caso contrário, retorna `false`.

