# ACCESS MODIFIER READONLY
Em TypeScript, o modificador `readonly` é usado para marcar uma propriedade de classe como somente leitura. Isso significa que uma vez que o valor dessa propriedade seja definido no construtor ou no momento da declaração, ele não pode ser alterado posteriormente. É útil para criar propriedades cujos valores devem ser definidos uma única vez e não podem ser modificados posteriormente.

Aqui está um exemplo de como usar o modificador `readonly` em TypeScript:

```typescript
class Carro {
  readonly marca: string;

  constructor(marca: string) {
    this.marca = marca;
  }

  alterarMarca(novaMarca: string) {
    // Erro de compilação: Propriedade 'marca' é somente leitura
    this.marca = novaMarca;
  }
}

const meuCarro = new Carro("Toyota");
console.log(meuCarro.marca); // Saída: Toyota

// Erro de compilação: Propriedade 'marca' é somente leitura
meuCarro.marca = "Honda";
```

Neste exemplo, a propriedade `marca` da classe `Carro` é marcada como somente leitura usando o modificador `readonly`. No construtor da classe, definimos o valor da propriedade `marca`, e uma vez definido, ele não pode ser alterado em nenhum outro lugar da classe ou fora dela.

É importante notar que o modificador `readonly` se aplica apenas ao nível da instância da classe. Isso significa que cada instância da classe pode ter um valor diferente para a propriedade somente leitura.

O modificador `readonly` é útil para criar propriedades imutáveis em classes, o que pode aumentar a segurança e prevenir erros de programação relacionados à modificação acidental de valores. Ele também pode ser usado para criar membros de classe que representam constantes ou configurações que não devem ser alteradas durante a execução do programa.