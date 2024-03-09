# Quick Sort

Este algoritmo lo que hace es obtener un valor pivot (que es el valor que siempre esta mas a la izquierda [0]). Y a partir de ahi ir buscando desde la izquierda y la derecha con dos punteros, si el valor del lado izquierdo es mas grande que el valor pivote y si el valor del lado derecho es menor que el valor del pivote. Una vez encuentra las posiciones, intercambia los valores de l y h. Y a partir de aquí se va a hacer lo mismo mientras que l < h. Cuando ya no se cumpla se intercambia lo que este en la posición de l por el valor del pivote. Denotando la mitad ordenada. Después, se hace un divide y vencerás, tomamos el index del pivote y lo usamos como delimitador para ejecutar en redundancia quicksort en el lado izquierdo y derecho del arreglo.

https://www.toptal.com/developers/sorting-algorithms/quick-sort

C++

```c++
#include <stdio.h>

void swap(int *x, int *y){
    int temp;
    temp = *x;
    *x= *y;
    *y = temp;
}

int partition(int A[], int l, int h){
    int pivot = A[l];
    int i=l, j=h;

    do{
        do{i++;}while(A[i]<=pivot);
        while(A[j]>pivot){
            j--;
        };

        if(i<j){
            swap(&A[i], &A[j]);
        }
    }while(i<j);
    swap(&A[l], &A[j]);
    return j;
}

void quickSort(int A[], int l, int h ){
    if(l<h){
        int j = partition(A, l , h);
        quickSort(A, l, j);
        quickSort(A, j+1, h);
    }
}
int main(int argc, const char * argv[]) {
    int A[] = {11,13,7,12,16,9,24,5,10,3}, n = 11, i;
    quickSort(A,0,9);

    for(i = 0;i< n - 1; i++){
        printf("%d ",A[i]);
    }
}

```
