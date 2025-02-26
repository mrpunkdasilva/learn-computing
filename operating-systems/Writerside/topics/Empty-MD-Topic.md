# 2. Sintaxe Básica

Neste capítulo, vamos explorar os fundamentos da sintaxe Java, desde a estrutura básica de um programa até os operadores mais comuns. Esses conceitos são essenciais para começar a programar em Java.

---

#### **2.1 Estrutura de um Programa Java**
Todo programa Java começa com uma **classe** e um **método principal** (`main`). Aqui está um exemplo simples:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

- **Classe (`Main`):** Todo programa Java é organizado em classes. O nome da classe deve corresponder ao nome do arquivo (`Main.java`).
- **Método `main`:** É o ponto de entrada do programa. O Java procura por esse método para começar a execução.
- **`System.out.println`:** Usado para imprimir texto no console.

---

#### **2.2 Tipos de Dados**
Java possui dois tipos de dados principais: **primitivos** e **de referência**.

- **Tipos Primitivos:**
  - `int`: Números inteiros (ex: `int idade = 25;`).
  - `double`: Números decimais (ex: `double altura = 1.75;`).
  - `char`: Um único caractere (ex: `char letra = 'A';`).
  - `boolean`: Valores verdadeiros ou falsos (ex: `boolean isJavaFun = true;`).

- **Tipos de Referência:**
  - `String`: Sequência de caracteres (ex: `String nome = "Java";`).
  - `Arrays`: Coleção de elementos do mesmo tipo (ex: `int[] numeros = {1, 2, 3};`).
  - Objetos: Instâncias de classes.

---

#### **2.3 Variáveis e Convenções de Nomes**
- **Declaração de Variáveis:**
  - Sintaxe: `tipo nome = valor;` (ex: `int numero = 10;`).
  - Variáveis devem ser declaradas antes de serem usadas.

- **Convenções de Nomes:**
  - Use `camelCase` para nomes de variáveis e métodos (ex: `idadeDoUsuario`).
  - Use `PascalCase` para nomes de classes (ex: `Calculadora`).
  - Constantes devem ser em `UPPER_CASE` (ex: `PI = 3.14;`).

---

#### **2.4 Operadores**
Java possui vários tipos de operadores para realizar operações em variáveis e valores.

- **Operadores Aritméticos:**
  - `+` (adição), `-` (subtração), `*` (multiplicação), `/` (divisão), `%` (módulo).
  - Exemplo: `int soma = 10 + 5;`.

- **Operadores de Comparação:**
  - `==` (igual), `!=` (diferente), `>` (maior), `<` (menor), `>=` (maior ou igual), `<=` (menor ou igual).
  - Exemplo: `boolean isMaior = 10 > 5;`.

- **Operadores Lógicos:**
  - `&&` (E lógico), `||` (OU lógico), `!` (NÃO lógico).
  - Exemplo: `boolean resultado = (10 > 5) && (20 < 30);`.



##### **Tabela de Operadores em Java**

| **Categoria**         | **Operador** | **Descrição**                                                                 | **Exemplo**                          |
|------------------------|--------------|-------------------------------------------------------------------------------|--------------------------------------|
| **Aritméticos**        | `+`          | Adição                                                                       | `int soma = 10 + 5;`                 |
|                        | `-`          | Subtração                                                                    | `int diferenca = 10 - 5;`            |
|                        | `*`          | Multiplicação                                                                | `int produto = 10 * 5;`              |
|                        | `/`          | Divisão                                                                      | `double quociente = 10.0 / 3.0;`     |
|                        | `%`          | Módulo (resto da divisão)                                                    | `int resto = 10 % 3;`                |
| **Atribuição**         | `=`          | Atribuição simples                                                           | `int x = 10;`                        |
|                        | `+=`         | Atribuição com adição                                                        | `x += 5;` (equivale a `x = x + 5;`)  |
|                        | `-=`         | Atribuição com subtração                                                     | `x -= 3;` (equivale a `x = x - 3;`)  |
|                        | `*=`         | Atribuição com multiplicação                                                 | `x *= 2;` (equivale a `x = x * 2;`)  |
|                        | `/=`         | Atribuição com divisão                                                       | `x /= 2;` (equivale a `x = x / 2;`)  |
|                        | `%=`         | Atribuição com módulo                                                        | `x %= 3;` (equivale a `x = x % 3;`)  |
| **Comparação**         | `==`         | Igual a                                                                      | `boolean isIgual = (10 == 5);`       |
|                        | `!=`         | Diferente de                                                                 | `boolean isDiferente = (10 != 5);`   |
|                        | `>`          | Maior que                                                                    | `boolean isMaior = (10 > 5);`        |
|                        | `<`          | Menor que                                                                    | `boolean isMenor = (10 < 5);`        |
|                        | `>=`         | Maior ou igual a                                                             | `boolean isMaiorOuIgual = (10 >= 5);`|
|                        | `<=`         | Menor ou igual a                                                             | `boolean isMenorOuIgual = (10 <= 5);`|
| **Lógicos**            | `&&`         | E lógico (AND)                                                               | `boolean resultado = (10 > 5) && (20 < 30);` |
|                        | `||`         | OU lógico (OR)                                                               | `boolean resultado = (10 > 5) || (20 < 30);` |
|                        | `!`          | NÃO lógico (NOT)                                                             | `boolean isNotTrue = !(10 > 5);`     |
| **Incremento/Decremento** | `++`      | Incremento (adiciona 1)                                                      | `x++;` (equivale a `x = x + 1;`)     |
|                        | `--`         | Decremento (subtrai 1)                                                       | `x--;` (equivale a `x = x - 1;`)     |
| **Ternário**           | `? :`        | Operador ternário (if-else em uma linha)                                     | `int maior = (10 > 5) ? 10 : 5;`     |




---

### **Exemplo Prático**
Aqui está um exemplo que combina tudo o que vimos até agora:

```java
public class Exemplo {
    public static void main(String[] args) {
        // Declaração de variáveis
        int numero1 = 10;
        int numero2 = 20;

        // Operações aritméticas
        int soma = numero1 + numero2;
        double media = soma / 2.0;

        // Comparação e lógica
        boolean isMaior = numero2 > numero1;
        boolean isPar = (soma % 2) == 0;

        // Saída de dados
        System.out.println("Soma: " + soma);
        System.out.println("Média: " + media);
        System.out.println("Número 2 é maior que Número 1? " + isMaior);
        System.out.println("A soma é par? " + isPar);
    }
}
```

---

### **Próximos Passos**
Agora que você conhece a sintaxe básica do Java, no próximo capítulo vamos explorar **estruturas de controle**, como condicionais e loops, para tornar seus programas mais dinâmicos.
