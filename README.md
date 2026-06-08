
# C com certeza é uma das linguagens já feitas.



Criada por Dennis Ritchie entre 1969 e 1973 para reescrever o Unix em algo portável. Hoje está em kernels, firmwares, drivers, bancos de dados e compiladores. Qualquer coisa onde performance e controle de memória importam.

---

## Por que essa porcaria ainda é util

- Compila direto para código de máquina.
- Controle na memoria.
- Roda em qualquer coisa que tenha um compilador C (Doom roda em uma geladeira).
- A maioria das linguagens modernas (Python, Lua, Ruby) tem a base escrita em C.

---

## Tipos

| Tipo      | Tamanho típico | Exemplo            |
|-----------|----------------|--------------------|
| `char`    | 1 byte         | `'A'`      |
| `int`     | 4 bytes        | `42`        |
| `float`   | 4 bytes        | `6.7f`            |
| `double`  | 8 bytes        | `6.7676767`       |
| `void`    | -    |  Funções   |

Modificadores: `short`, `long`, `unsigned`, `signed`.

```c
int idade = 25;
float altura = 1.67f;
char inicial = 'N';
```

---

## Variáveis e constantes

```c
int x = 67;          // variável
const int MAX = 6767; // constante
#define AURA 6.7   // macro (substituição em tempo de compilação)
```

`#define` não tem tipo. `const` tem.

---

## Operadores

**Aritméticos:** `+` `-` `*` `/` `%`

**Relacionais:** `==` `!=` `<` `>` `<=` `>=`

**Lógicos:** `&&` `||` `!`

**Bitwise:** `&` `|` `^` `~` `<<` `>>`

**Incremento/Decremento:** `++` `--`

**Atribuição composta:** `+=` `-=` `*=` `/=`

---

## Condição

### if / else

```c
if (x > 0) {
    printf("positivo");
} else if (x < 0) {
    printf("negativo");
} else {
    printf("maionese");
}
```

### switch

```c
switch (opcao) {
    case 1:
        printf("meia");
        break;
    case 2:
        printf("sevenn");
        break;
    default:
        printf("67");
}
```

### Laço de repetição

```c
// for
for (int i = 0; i < 10; i++) {
    printf(i);
}

// while
while (condicao) {
}

// do-while
do {

} while (condicao);
```

`break` pula fora. `continue` volta pro começo.

---

## Funções

```c
// declaração (protótipo)
int soma(int a, int b);

// definição
int soma(int a, int b) {
    return a + b;
}

// função sem retorno
void imprime(int x) {
    printf(x);
}
```

C passa argumentos **por valor**. Para modificar a variável original, use ponteiros.

---

## Arrays/Vetores

```c
int numeros[5] = {10, 20, 30, 40, 50};
numeros[0];
numeros[4];

int matriz[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// Arrays em C são tão burros quanto uma porta que não sabe seu próprio tamanho, tem que ser controlado pelo programador.
```


---

## Strings

Strings são arrays de `char`

```c
char nome[26] = "Pindanmonhangabo da silva";
char outro[] = "Freddie Mercury"; 

strlen(nome);           // tamanho
strcpy(destino, fonte); // copia
strcat(destino, fonte); // junta
strcmp(a, b);           // compara (retorna 0 se iguais)
```

---

## Ponteiros

Não sei usar

---

## Alocação dinâmica de memória


`malloc` aloca sem inicializar. `calloc` aloca e zera. `realloc` redimensiona.

(não sei usar também)
---

## Structs

Agrupa tipos diferentes em um único tipo.

```c
struct Ponto {
    float x;
    float y;
};

struct Ponto p1 = {6f, 6.7f};
printf(p1.x);
```

---

## Entrada e saída

```c
#include <stdio.h>

// saída
printf("AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA");

// entrada
int n;
scanf("%d", &n); // lê um inteiro

char linha[100];
fgets(linha, sizeof(linha), stdin); // não sei oq isso aqui faz pra ser sincero, mas assumo que leia linha inteira
```

---

## Compilação
 Tem que usar algum compilador aí, tipo o gcc. Daí rodar o comando
---

## Referências

- [C (linguagem de programação)](https://pt.wikipedia.org/wiki/C_(linguagem_de_programa%C3%A7%C3%A3o))
- [C Reference (cppreference)](https://en.cppreference.com/w/c)
- [Introdução à Programação em C
](https://www.inf.ufpr.br/hexsel/ci067/01_intro.html)
- Claude pq o cara é bom demais no que faz kkkkkkkkkkk
