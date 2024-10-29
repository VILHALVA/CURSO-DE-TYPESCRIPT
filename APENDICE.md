# APÊNDICE
---

## RECURSOS QUE O TYPESCRIPT TEM QUE O JAVASCRIPT NÃO TEM:
TypeScript oferece diversos recursos avançados que o JavaScript não possui nativamente, tornando-o uma escolha popular para grandes projetos de desenvolvimento front e backend. Aqui estão alguns dos principais recursos que destacam o TypeScript em relação ao JavaScript:

### 1. **TIPAGEM ESTÁTICA**
   - O TypeScript permite definir tipos explícitos para variáveis, parâmetros de função, e retornos. Isso ajuda a identificar erros antes mesmo da execução, algo que o JavaScript, sendo uma linguagem de tipagem dinâmica, não fornece.
   ```typescript
   let age: number = 30;
   ```

### 2. **INTERFACES E TIPOS CUSTOMIZADOS**
   - Interfaces permitem a definição de contratos para objetos, promovendo consistência e padronização. Também é possível criar tipos customizados, algo inexistente no JavaScript.
   ```typescript
   interface User {
       name: string;
       age: number;
   }
   ```

### 3. **ENUMERAÇÕES (ENUMS)**
   - `Enums` são uma forma de definir um conjunto de valores nomeados. São particularmente úteis para representar estados ou opções fixas.
   ```typescript
   enum Direction {
       Up,
       Down,
       Left,
       Right
   }
   ```

### 4. **CLASSES COM MODIFICADORES DE ACESSO**
   - TypeScript adiciona modificadores de acesso (`public`, `private`, `protected`), permitindo maior controle sobre a visibilidade dos métodos e propriedades de uma classe.
   ```typescript
   class Car {
       private engine: string;
       constructor(engine: string) {
           this.engine = engine;
       }
   }
   ```

### 5. **GENERICS**
   - Generics permitem criar funções e classes que podem trabalhar com diferentes tipos de dados sem perder a segurança de tipos.
   ```typescript
   function identity<T>(arg: T): T {
       return arg;
   }
   ```

### 6. **CHECAGEM DE ERROS E INFERÊNCIA DE TIPOS EM TEMPO DE COMPILAÇÃO**
   - O TypeScript faz uma verificação de erros em tempo de compilação, detectando inconsistências de tipos, nomes incorretos e outros problemas antes do código ser executado.

### 7. **TIPOS DE UNIÃO E INTERSEÇÃO**
   - TypeScript suporta a criação de tipos que podem combinar múltiplos tipos através de união (`|`) ou interseção (`&`).
   ```typescript
   type Result = Success | Failure;
   ```

### 8. **TIPAGEM ESTRUTURAL**
   - O TypeScript utiliza tipagem estrutural, o que permite verificar a compatibilidade de tipos baseada na estrutura e não apenas no nome.

### 9. **DECORATORS**
   - Embora ainda em estágio experimental, decorators são suportados no TypeScript e oferecem uma maneira poderosa de adicionar metadados e modificar o comportamento de classes e métodos.

Esses recursos tornam o TypeScript uma ferramenta robusta para projetos complexos, especialmente aqueles que requerem manutenção e colaboração extensiva.

---

## COPILAÇÃO AUTOMATICA:
Para criar e configurar um projeto TypeScript com compilação automática, você pode seguir as etapas abaixo. Este exemplo usa o `tsc` para compilar o TypeScript e `nodemon` para reiniciar automaticamente o servidor sempre que houver alterações no código.

### PASSO 1: INICIALIZAR O PROJETO:
1. **Crie um diretório para o seu projeto e navegue até ele:**
   ```bash
   mkdir meu-projeto-ts
   cd meu-projeto-ts
   ```

2. **Inicialize um novo projeto Node.js:**
   ```bash
   npm init -y
   ```

### PASSO 2: INSTALAR DEPENDÊNCIAS:
1. **Instale o TypeScript e os tipos para Node.js como dependências:**
   ```bash
   npm install typescript @types/node --save-dev
   ```

2. **Instale o Nodemon como uma dependência de desenvolvimento:**
   ```bash
   npm install nodemon --save-dev
   ```

### PASSO 3: CONFIGURAR O TYPESCRIPT:
1. **Crie um arquivo `tsconfig.json` na raiz do projeto com a seguinte configuração:**
   ```json
   {
     "compilerOptions": {
       "target": "es6",
       "module": "commonjs",
       "outDir": "./dist",
       "rootDir": "./src",
       "strict": true
     },
     "include": ["src/**/*"]
   }
   ```

### PASSO 4: CONFIGURAR O `PACKAGE.JSON`:
1. **Atualize o `package.json` para incluir os scripts necessários:**
   ```json
   {
     "name": "codigo",
     "version": "1.0.0",
     "main": "dist/APP.js",
     "scripts": {
       "build": "tsc",
       "start": "npm run build && node dist/APP.js",
       "test": "npm run build && nodemon dist/APP.js"
     },
     "keywords": [],
     "author": "",
     "license": "ISC",
     "description": "",
     "dependencies": {
       "@types/node": "^20.12.12",
       "typescript": "^5.4.5"
     },
     "devDependencies": {
       "nodemon": "^3.1.4"
     }
   }
   ```

### PASSO 5: ESTRUTURAR O PROJETO:
1. **Crie o diretório `src` na raiz do projeto:**
   ```bash
   mkdir src
   ```

2. **Dentro do diretório `src`, crie um arquivo TypeScript, por exemplo, `APP.ts`:**
   ```typescript
   // src/APP.ts
   console.log("Olá, TypeScript!");
   ```

### PASSO 6: COMPILAR E EXECUTAR O PROJETO:
1. **Para compilar o código TypeScript, use:**
   ```bash
   npm run build
   ```

2. **Para iniciar o projeto, use:**
   ```bash
   npm start
   ```

3. **Para executar o projeto com reinicialização automática ao salvar, use:**
   ```bash
   npm test
   ```

### PASSO 7: DESENVOLVIMENTO COM AUTO-COMPILAÇÃO:
1. **Configure o `nodemon` para observar as alterações nos arquivos TypeScript e recompilar automaticamente:**

   Crie um arquivo `nodemon.json` na raiz do projeto com a seguinte configuração:
   ```json
   {
     "watch": ["src"],
     "ext": "ts",
     "exec": "npm run build && node dist/APP.js"
   }
   ```

Agora, ao usar `npm test`, o Nodemon observará as mudanças nos arquivos TypeScript dentro do diretório `src`, recompilará o projeto e reiniciará a aplicação automaticamente.

### RESUMO DOS SCRIPTS:
- **`npm run build`**: Compila o código TypeScript.
- **`npm start`**: Compila o código e, em seguida, executa o arquivo de saída `APP.js`.
- **`npm test`**: Compila o código e executa o arquivo de saída com Nodemon para reinicialização automática.

### ESTRUTURA FINAL DO PROJETO:
Seu projeto deve ter a seguinte estrutura:

```
meu-projeto-ts/
├── dist/
│   └── APP.js
├── src/
│   └── APP.ts
├── node_modules/
├── package.json
├── package-lock.json
├── tsconfig.json
└── nodemon.json
```

