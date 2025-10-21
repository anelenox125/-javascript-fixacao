**Exercício de Fixação JavaScript**

**Nome: Anefatima B.S. Figueiredo**

**Data: 12/10/2025**

Seções no documento:

**1\. Variáveis e Tipos**

● Qual a diferença entre var, let e const?

var: Escopo global/função, sofre hoisting, pode ser redeclarada

let: Escopo de bloco, não pode ser redeclarada no mesmo escopo, valor mutável

const: Escopo de bloco, não pode ser redeclarada nem reassinalada, valor constante

● Liste os tipos primitivos do JavaScript com exemplos:

javascript

let nome = "João"; // string

let idade = 25; // number

let ativo = true; // boolean

let valor = null; // null

let indefinido; // undefined

let simbolo = Symbol("id"); // Symbol

● Qual a diferença entre null e undefined?

undefined: Variável declarada mas não atribuída

null: Valor atribuído intencionalmente para representar "vazio"

● Explique == e ===:

\==: Comparação com conversão de tipo (coerção)

javascript

console.log(5 == "5"); _// true_

console.log(1 == true); _// true_

console.log(0 == false); _// true_

console.log(null == undefined); _// true_

console.log("" == 0); _// true_

\===: Comparação estrita (mesmo valor E mesmo tipo)

javascript

console.log(5 === "5"); _// false (número ≠ string)_

console.log(1 === true); _// false (número ≠ booleano)_

console.log(0 === false); _// false (número ≠ booleano)_

console.log(null === undefined); _// false (tipos diferentes)_

console.log("" === 0); _// false (string ≠ número)_

**2\. Operadores e Expressões**

● Operadores matemáticos: +, -, \*, /, %, \*\*

1.  + (Adição)
2.  \- (Subtração)
3.  \* (Multiplicação)
4.  / (Divisão)
5.  % (Módulo - resto da divisão)
6.  \*\* (Exponenciação)

Exemplo:

javascript

let a = 10;

let b = 3;

console.log(a + b); _// 13_

console.log(a - b); _// 7_

console.log(a \* b); _// 30_

console.log(a / b); _// 3.333..._

console.log(a % b); _// 1 (porque 10 dividido por 3 é 3 com resto 1)_

console.log(a \*\* b); _// 1000 (10 elevado a 3)_

● Operadores lógicos: && (E), || (OU), ! (NÃO)

1.  && (E) - retorna o primeiro valor se for falso, senão retorna o segundo
2.  || (OU) - retorna o primeiro valor se for verdadeiro, senão retorna o segundo
3.  ! (NÃO) - inverte o valor booleano

Exemplo:

javascript

let idade = 25;

let temCarteira = true;

let temExperiencia = false;

_// AND (&&) - TODAS as condições devem ser verdadeiras_

console.log(idade >= 18 && temCarteira); _// true_

console.log(idade >= 18 && temCarteira && temExperiencia); _// false_

_// OR (||) - PELO MENOS UMA condição deve ser verdadeira_

console.log(idade >= 18 || temExperiencia); _// true_

console.log(temCarteira || temExperiencia); _// true_

_// NOT (!) - Inverte o valor booleano_

console.log(!temCarteira); _// false_

console.log(!temExperiencia); _// true_

● Preveja os resultados:

javascript

_// 1. Operadores matemáticos_

console.log(8 + 2 \* 3); _// 14 (2\*3=6 + 8)_

console.log((8 + 2) \* 3); _// 30_

console.log(17 % 5); _// 2_

console.log(2 \*\* 4); _// 16_

console.log("5" + 2); _// "52"_

console.log("5" - 2); _// 3_

_// 2. Operadores lógicos_

let a = true, b = false, c = true;

console.log(a && b); _// false_

console.log(a && c); _// true_

console.log(a || b); _// true_

console.log(b || b); _// false_

console.log(!a); _// false_

console.log(!b); _// true_

_// 3. Combinações_

let x = 10, y = 5, z = 15;

console.log(x > y && y < z); _// true_

console.log(x === 10 || z === 10);_// true_

console.log(!(x > y)); _// false_

console.log(x % y === 0); _// true_

_// 4. Casos especiais_

console.log(0 && "Hello"); _// 0 (primeiro valor falso)_

console.log("Hello" && "World"); _// "World" (último valor verdadeiro)_

console.log(null || "Default"); _// "Default" (primeiro valor verdadeiro)_

console.log(0 || false || "OK"); _// "OK"_

**3\. Estruturas de Controle**

● Explique if, else if e else:

javascript

if (condição1) {

// executa se condição1 for true

} else if (condição2) {

// executa se condição2 for true

} else {

// executa se todas forem false

}

● Como usar switch?

javascript

switch(dia) {

case 1:

console.log("Domingo");

break;

case 2:

console.log("Segunda");

break;

default:

console.log("Dia inválido");

}

● Exemplo de verificação de maioridade:

javascript

let idade = 18;

if (idade >= 18) {

console.log("Maior de idade");

} else {

console.log("Menor de idade");

}

**4\. Loops e Repetições**

● Tipos de loops: for, while, do...while, for...of, for...in

● **Imprimir números de 1 a 5:**

javascript

// Com for

for (let i = 1; i <= 5; i++) {

console.log(i);

}

// Com while

let i = 1;

while (i <= 5) {

console.log(i);

i++;

}

● **Explique break:**

break interrompe completamente a execução do loop

Usado quando encontramos o que procurávamos e não precisamos continuar

**5\. Funções**

● O que é uma função?

Bloco de código reutilizável que executa uma tarefa específica.

● Diferença entre função declarada e função expressa:

javascript

// Função declarada - hoisting

function soma(a, b) {

return a + b;

}

// Função expressa - sem hoisting

const multiplicar = function(a, b) {

return a \* b;

};

● Função de saudação:

javascript

function saudacao(nome) {

return \`Olá, ${nome}! Seja bem-vindo(a)!\`;

}

6\. Mini-casos práticos

● Verificação de número par ou ímpar:

javascript

function verificarParImpar(numero) {

if (numero % 2 === 0) {

return "Par";

} else {

return "Ímpar";

}

}

● Lista de compras:

javascript

let listaCompras = \["Arroz", "Feijão", "Leite", "Ovos", "Pão"\];

console.log(listaCompras\[0\]); // "Arroz"

● Somar números de 1 a 10:

javascript

let soma = 0;

for (let i = 1; i <= 10; i++) {

soma += i;

}

console.log(soma); // 55

7\. Reflexão

● Por que conhecer tipos e operadores ajuda a programar melhor?

Permite prever comportamentos do código, evitar erros de tipo, e escrever lógica mais eficiente.

● Por que usar console.log() é importante para debug?

Permite verificar valores em tempo de execução, identificar onde o código falha, e entender o fluxo de execução.

● Como planejar variáveis, funções e loops antes de programar?

\- Identificar que dados serão necessários (variáveis)

\- Pensar em tarefas repetitivas (loops)

\- Agrupar funcionalidades relacionadas (funções)

\- Escrever pseudocódigo antes do código real

**. Planejamento de Variáveis**

**Perguntas a fazer:**

*   Quais dados preciso armazenar?
*   Quais dados mudam durante a execução?
*   Quais são constantes?

**Exemplo Prático - Sistema de Notas:**

javascript

_// ANTES de codificar, planeje:_

const NUMERO\_ALUNOS = 30; _// Constante_

let notas = \[\]; _// Array para armazenar_

let mediaTurma = 0; _// Valor que será calculado_

let alunoAprovado = false; _// Flag booleana_

const NOTA\_MINIMA = 7; _// Constante de regra de negócio_

**2. Planejamento de Funções**

**Use a abordagem "Uma responsabilidade":**

javascript

_// Em vez de uma função gigante, planeje funções específicas:_

_// ✓ BOM - Cada função tem um propósito claro_

function calcularMedia(notas) {} _// Calcula média_

function verificarAprovacao(media) {} _// Verifica se passou_

function gerarRelatorio(aluno, media) {} _// Gera output_

_// ✗ RUIM - Uma função faz tudo_

function processarTudo() {} _// Muito complexa_

**3. Planejamento de Loops**

**Pense em:**

*   O que se repete?
*   Quantas vezes?
*   Precisa de condições de parada?