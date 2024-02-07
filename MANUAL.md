# MANUAL
## EXECUTANDO O CÓDIGO
Você pode executar programas TypeScript tanto pelo Prompt de Comando (CMD) quanto pelo Visual Studio Code. Aqui estão os passos básicos para fazer isso em ambos os ambientes:

### EXECUTANDO PELO CMD:
1. **Verifique a Instalação**: Certifique-se de que você tenha o TypeScript instalado globalmente em sua máquina. Você pode verificar isso executando o seguinte comando no CMD:

   ```bash
   tsc -v
   ```

   Isso deve exibir a versão do TypeScript, o que significa que está instalado corretamente.

2. **Crie um Arquivo TypeScript**: Crie um arquivo TypeScript (com a extensão `.ts`) em um diretório de sua escolha.

3. **Escreva seu Código TypeScript**: Abra o arquivo `.ts` em um editor de texto ou IDE de sua escolha e escreva seu código TypeScript.

4. **Compilação TypeScript**: No CMD, navegue até o diretório onde está localizado o arquivo `.ts` e execute o seguinte comando para compilar o TypeScript em JavaScript:

   ```bash
   tsc arquivo.ts
   ```

   Isso irá gerar um arquivo JavaScript correspondente com o mesmo nome (por exemplo, `arquivo.js`) no mesmo diretório.

5. **Execute o Código JavaScript**: Agora que você tem o arquivo JavaScript, pode executá-lo normalmente usando o Node.js, por exemplo:

   ```bash
   node arquivo.js
   ```

   Isso executará o código JavaScript resultante.

### EXECUTANDO PELO VISUAL STUDIO CODE:
O Visual Studio Code é uma IDE que oferece suporte nativo ao TypeScript e facilita a execução de código TypeScript.

1. **Instale o Visual Studio Code**: Certifique-se de ter o Visual Studio Code instalado em sua máquina. Você pode baixá-lo em [https://code.visualstudio.com/](https://code.visualstudio.com/) e instalá-lo.

2. **Crie um Projeto**: Abra o Visual Studio Code e crie um novo projeto ou abra um projeto existente que contenha arquivos TypeScript.

3. **Crie um Arquivo TypeScript**: Crie um novo arquivo TypeScript (com a extensão `.ts`) no projeto ou abra um arquivo TypeScript existente.

4. **Escreva seu Código TypeScript**: Escreva seu código TypeScript no arquivo.

5. **Compilação Automática**: O Visual Studio Code compila automaticamente seu código TypeScript em JavaScript à medida que você o escreve. Você não precisa executar manualmente o compilador TypeScript.

6. **Execute o Código TypeScript**: Você pode executar diretamente seu código TypeScript pressionando `F5` para depurar o código ou clicando com o botão direito do mouse no arquivo TypeScript e escolhendo "Run Code".

   Certifique-se de que você tenha o Node.js instalado para executar o código JavaScript resultante.

O Visual Studio Code simplifica muito o desenvolvimento em TypeScript, pois integra automaticamente o processo de compilação e execução, tornando-o uma ótima escolha para trabalhar com TypeScript.
