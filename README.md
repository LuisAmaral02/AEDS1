## Exercício 1 - MinMax - Custo Computacional
##### Data: 25/05/2021
##### Nome: Luis Augusto Amaral
Desafio: Encontrar máximo e mínimo de um vetor com o menor custo computacional.

#### Código original:

    #include <stdlib.h>
    #include <stdio.h>
    
    void MinMax(int *data, int *mi, int *ma){
        *mi = data[0];
        *ma = data[0];
    
        for (int i=1;i<10;i++){
            if (data[i] < *mi)
                *mi = data[i];
            if (data[i] > *ma)
                *ma = data[i];
        }
    }
    
    int main(){
        int data[10] = {22, 9, 33, 28, 13, 17, 01, 44, 90, 11};
        int mi, ma;
    
        MinMax(data, &mi, &ma);
    
        printf("Minimo: %d e maximo: %d", mi, ma);
        exit (0);
    }
   
   #### Código alterado:

    #include <stdlib.h>
    #include <stdio.h>
    
    void MinMax(int *data, int *mi, int *ma){
        *mi = data[0];
        *ma = data[0];
    
        for (int i=1;i<10;i++){
            if (data[i] < *mi)
                *mi = data[i];
            else if (data[i] > *ma)
                *ma = data[i];
        }
    }
    
    int main(){
        int data[10] = {22, 9, 33, 28, 13, 17, 01, 44, 90, 11};
        int mi, ma;
    
        MinMax(data, &mi, &ma);
    
        printf("Minimo: %d e maximo:%d", mi, ma);
        exit (0);
    }

### Relatório Final:

A solução mais eficaz que encontrei foi adicionar o else antes do segundo if. Assim sendo, como as duas condições não poderão ser satisfeitas, e apenas uma, esse else é possível, tornando o custo computacional menor em seu melhor caso: (n-1). Também tentei de outras formas, como pensar em algum jeito de um if "seletor" para entrar no for, mas não consegui sucesso, além de outras tentativas falhas. 



