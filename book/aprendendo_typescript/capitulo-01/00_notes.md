### JavaScript
JavaScript foi projetado em 10 dias por Brendan Eich na Netscape em 1995 para ser acessível e fácil de usar em sites. A linguagem vem evoluindo desde 1995, e seu comitê diretivo, o TC39, tem lançado anualmente novas versões do ECMAScript.

#### A documentação do JavaScript
A documentação do JavaScript é frequentemente considerada vaga, sem formalização clara sobre como descrever parâmetros e valores de retorno de funções, entre outros aspectos. No entanto, muitos desenvolvedores têm usado o JSDoc em comentários para descrever como uma função, variável, etc., deve ser utilizada.

Por exemplo:

```javascript
/**
 * Função que soma dois números.
 * @param {number} a - O primeiro número a ser somado.
 * @param {number} b - O segundo número a ser somado.
 * @returns {number} - A soma dos dois números.
 */
function soma(a, b) {
  return a + b;
}

// Uso da função soma
const resultado = soma(3, 5);
console.log(resultado); // Saída: 8
```

Neste exemplo, o JSDoc é utilizado para documentar a função soma, especificando os parâmetros a e b e o valor de retorno da função.

### Typescript
- Uma linguagem de programação: TypeScript é uma linguagem de programação desenvolvida pela Microsoft que amplia o JavaScript adicionando tipos estáticos opcionais, facilitando a detecção de erros durante o desenvolvimento e melhorando a manutenção de código.
- Um verificador de tipos: O TypeScript inclui um poderoso sistema de verificação de tipos que analisa o código durante a compilação para garantir que os tipos estejam sendo usados de forma consistente e correta, ajudando os desenvolvedores a escrever código mais seguro e confiável.
- Um compilador: O compilador do TypeScript transforma o código TypeScript em código JavaScript padrão, permitindo que os desenvolvedores escrevam em TypeScript e executem suas aplicações em qualquer ambiente que suporte JavaScript.
- Um serviço de linguagem (language service): O serviço de linguagem do TypeScript fornece recursos avançados de edição e ferramentas de desenvolvimento, como autocompletar, refatoração de código e navegação inteligente, integrando-se perfeitamente aos editores de código populares, como o Visual Studio Code.

#### Instalando localmente

1. Certifique-se de ter o Node.js instalado na sua máquina.
   ```
   $ npm i -g typescript
   ```
   Execute `tsc --version` para verificar a versão instalada.

2. Execute localmente:
   ```
   tsc --init
   ```
Um arquivo `tsconfig.json` (um starter) será criado com as configurações que seu projeto TypeScript usará.

Notas:
- Um transpilador é uma ferramenta que lê o código-fonte escrito em uma linguagem e produz um código equivalente em outra com o mesmo nível de abstração.
- Starters são repositórios na forma de um modelo que permitem criar uma solução pré-configurada

Use o comando 
```typescript
tsc --skipLibCheck index.ts
```
Para converter o arquivo index.ts em index.js