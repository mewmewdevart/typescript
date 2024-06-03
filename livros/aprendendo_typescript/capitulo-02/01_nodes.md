### O sistema de tipos
O poder do JavaScript vem da flexibilidade; cuidado com isso!

#### O que é inferir?
"Inferir" refere-se ao processo pelo qual o compilador deduz automaticamente o tipo de uma variável, função ou expressão com base no contexto em que é usada.  
Por exemplo:

```typescript
let singer = "Beyonce";
```
O TypeScript poderá inferir, entender que a variável `singer` é do tipo `string`.

#### Exemplos de tipos básicos:

```typescript
// boolean
let isDone: boolean = false;

// number
let decimal: number = 6;
let hex: number = 0xf00d;
let binary: number = 0b1010;
let octal: number = 0o744;

// string
let color: string = "blue";
color = 'red';

// null
let n: null = null;

// undefined
let u: undefined = undefined;

// bigint
let big: bigint = 100n;

// symbol
let sym1: symbol = Symbol("key1");
let sym2: symbol = Symbol("key2");

// TypeScript inferência de tipos
let count = 42; // inferido como number
let name = "Alice"; // inferido como string
```

#### Comportamentos dos tipos em ação:

1. **Lendo o código e detectando todos os tipos e valores que existem:**

```typescript
let age: number = 25;
let name: string = "John";
let isStudent: boolean = true;
```

2. **Para cada valor, vendo que tipo sua declaração inicial indica que ele pode conter:**

```typescript
let score = 100; // inferido como number
score = "A"; // Erro: Type 'string' is not assignable to type 'number'
```

3. **Para cada valor, vendo todas as maneiras de como ele é usado posteriormente no código:**

```typescript
let total: number = 0;
total += 10; // OK
total = "ten"; // Erro: Type 'string' is not assignable to type 'number'
```

4. **Alertando ao usuário se o uso de um valor não for correspondente ao seu tipo:**

```typescript
let price: number = 9.99;
price = "free"; // Erro: Type 'string' is not assignable to type 'number'
```

### Tipos de erros
Os mais comuns são:

#### De sintaxe:
Impedem que o TypeScript seja convertido para JavaScript.

Exemplo:

```typescript
let number = 42  // Erro: ';' expected.
console.log(number)
```

#### De tipo:
Algo incompatível é detectado pelo verificador de tipos.

Exemplo:

```typescript
let age: number = 25;
age = "vinte e cinco"; // Erro: Type 'string' is not assignable to type 'number'
```

Mais exemplos de erros:

#### Erro de sintaxe:

```typescript
function greet(name: string) {
  console.log("Hello, " + name)
    // '}' expected.
```

#### Erro de tipo:

```typescript
let isAvailable: boolean = true;
isAvailable = 1; // Erro: Type 'number' is not assignable to type 'boolean'
```

⚠️ | Não é permitido atribuir 1 ou 0 a uma variável do tipo boolean, mesmo que em algumas linguagens de programação esses valores possam ser considerados equivalentes a true e false

#### Outro erro de sintaxe:

```typescript
if (true {
  console.log("True"); // ')' expected.
}
```


#### Outro erro de tipo:

```typescript
function sum(a: number, b: number): number {
  return a + b;
}

let result = sum(10, "20"); // Erro: Argument of type 'string' is not assignable to parameter of type 'number