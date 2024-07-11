# COPILAÇÃO AUTOMATICA
Para criar e configurar um projeto TypeScript com compilação automática, você pode seguir as etapas abaixo. Este exemplo usa o `tsc` para compilar o TypeScript e `nodemon` para reiniciar automaticamente o servidor sempre que houver alterações no código.

## PASSO 1: INICIALIZAR O PROJETO:
1. **Crie um diretório para o seu projeto e navegue até ele:**
   ```bash
   mkdir meu-projeto-ts
   cd meu-projeto-ts
   ```

2. **Inicialize um novo projeto Node.js:**
   ```bash
   npm init -y
   ```

## PASSO 2: INSTALAR DEPENDÊNCIAS:
1. **Instale o TypeScript e os tipos para Node.js como dependências:**
   ```bash
   npm install typescript @types/node --save-dev
   ```

2. **Instale o Nodemon como uma dependência de desenvolvimento:**
   ```bash
   npm install nodemon --save-dev
   ```

## PASSO 3: CONFIGURAR O TYPESCRIPT:
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

## PASSO 4: CONFIGURAR O `PACKAGE.JSON`:
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

## PASSO 5: ESTRUTURAR O PROJETO:
1. **Crie o diretório `src` na raiz do projeto:**
   ```bash
   mkdir src
   ```

2. **Dentro do diretório `src`, crie um arquivo TypeScript, por exemplo, `APP.ts`:**
   ```typescript
   // src/APP.ts
   console.log("Olá, TypeScript!");
   ```

## PASSO 6: COMPILAR E EXECUTAR O PROJETO:
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

## PASSO 7: DESENVOLVIMENTO COM AUTO-COMPILAÇÃO:
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

## RESUMO DOS SCRIPTS:
- **`npm run build`**: Compila o código TypeScript.
- **`npm start`**: Compila o código e, em seguida, executa o arquivo de saída `APP.js`.
- **`npm test`**: Compila o código e executa o arquivo de saída com Nodemon para reinicialização automática.

## ESTRUTURA FINAL DO PROJETO:
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

Agora você tem um projeto TypeScript configurado com compilação automática e reinicialização do servidor, pronto para desenvolvimento contínuo! 