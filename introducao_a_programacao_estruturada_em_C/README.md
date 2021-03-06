# INTRODUÇÃO A PROGRAMAÇÃO ESTRUTURADA EM C

## TEMA 4 - Estruturas de Decisão

### Módulo 2
    Aplicar os conceitos de estruturas de decisão encadeada e aninhada e de múltiplas alternativas.

1. Introdução: Para se utilizar o if ou else deve-se verificar qual a quantidade de comandos serão executados, se a verificação exigir apenas uma condição o uso de chaves torna-se opcional, caso se utilize mais de um comando é necessário utilizar chaves, assim como deve-se utilizar caso tenha que usar o *Else*
2. Caso tenha uma verificação que seja necessário utilizar dois *if*, essa estrutura recebe o nome de *if aninhado*
3. Estruturas de decisão aninhadas: Ocorre quando é necessário usar vários *if* internos.
4. if interno do tipo composto
```C
if(EXPRESSAO_CONDICIONAL_1){
    if(EXPRESSAO_CONDICIONAL_2){
        BLOCO_INSTRUCAO_1;
    } else {
        BLOCO_INSTRUCAO_2;
    }
}
```
5. if interno do tipo simples
```C
if(EXPRECAO_CONDICIONAL_1){
    if(EXPRECAO_CONDICIONAL_2){
        BLOCO_INSTRUCAO_1;
    }
}
```
6. Exemplos: 
```C
#include <stdio.h>

int main() {
    int opcao;

    printf("Entre com um numero inteiro:\n");
    scanf("%d", &opcao);

    if(opcao >= 0){
        if(opcao == 0){
            printf("\nNumero nulo.\n");
        } else {
            printf("\nNumero positivo.\n");
        } 
    }else{
        printf("\nNumero negativo.\n");
    }
}
```
7. ESTRUTURAS DE DECISÃO ENCADEADAS: São dispostas de forma sequencial, independentemente de serem simples ou complexas.
8. OPERADOR TERNÁRIO: É reconhecido com esse nome pois possu três campos na sua construção:
Variavel = expressao_logica ? valor_1 : valor_2

    A expressao_logica verifica uma condição, se for verdadeiro o valor_1 será executado se for falso, o valor_2 será executado
>Operador ternário também permite que seja realizado alinhamento, porém não é uma boa prática de programação.

9. ESTRUTURAS DE MÚLTIPLAS ALTERNATIVAS: Também conhecida como **switch-case**, permite que seja criada uma estrutura condicional que verificará o valor de uma variável de controle.
```C
switch(VARIAVEL) {
    case A: BLOCO_1;
        break;
    case B: BLOCO_2;
        break;
    case C: BLOCO_3;
        break;
    default: BLOCO_4;
}
```
>Outro ponto importante é que no caso de VARIAVEL não ser igual a nenhuma das opções, então o comando DEFAULT é executado. No entanto, deve-se salientar que este comando é opcional.

    Normalmente, o comando switch é utilizado quando são ofertadas aos usuários diversas opções para que eles possam escolher, geralmente, no decorrer do preenchimento de um formulário.

### CONCLUSÃO

1. CONSIDERAÇÕES FINAIS: Apresentou os conceitos de estrutura de decisão usando a linguagem C, que permite que as aplicações desenvolvidos sejam eficientes. Utilizando de *if* e *else* e seus aninhamentos e encadeamentos, além da estrutura *switch-case*.

===
## TEMA 5: ESTRUTURAS DE REPETIÇÃO

### Módulo 1 - Comando FOR:
    Utilizado para executar um comando muitas vezes, sempre que um sistema precise executar muitos comandos iguais, deve-se utilizar as estruturas de repetição

```C
for (inicializacao; condicao; incremento_decremento)
{
    Bloco_de_comando;
}
```
1. A variável de controle recebe o valor inicial, definido na inicialização
2. O valor da variável de controle é comparado com a condição
3. se a condição for verdadeira, executa o bloco e incrementa ou decrementa a variável de controle.

**1º problema**
```C
int num;
printf("Digite um número: \n");
scanf("%d", &num);

for(int i=0; i<20; i++){
    printf("%d", num);
}
```
**2º problema**
```C
int num, maior=0, i=0;

for (i; i<15; i++) {
    scanf("%d", &num);

    if(num>maior){
        maior = num;
    }
}
printf("%d", maior);
```
### Módulo 2 - Comando WHILE:
    Executa um bloco de código ENQUANTO uma condição for verdadeira.

### Módulo 3 - Comando DO-WHILE:
    Executa pelo menos uma vez e depois faz a verificação de continuidade.

## TEMA 6 - VETORES E MATRIZES

int vogais[100]; => [] -> Quantidade de índices que terá o vetor

    matriz:
    int matriz[3][3] -> [linha][coluna]