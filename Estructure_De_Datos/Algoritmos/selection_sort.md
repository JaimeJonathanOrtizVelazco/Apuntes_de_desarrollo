# Selection Sort

Este algoritmo de ordenamiento lo que hace es ir buscando en cada ejecución (por todo el arreglo), los valores mas pequeños. Poniéndolos al inicio del arreglo. Es decir, que no necesitaremos iniciar las iteraciones en la posición 0 cada vez que vamos a buscar el valor mas pequeño, sino que como sabemos que en las primeras posiciones van a hacer los valores mas pequeños, vamos a recorrernos un indice y colocar el valor mas pequeño siguiente.

https://www.toptal.com/developers/sorting-algorithms/selection-sort
<br>
C++

```c++
#include <stdio.h>

void swap(int *x, int *y){
    int temp;
    temp = *x;
    *x= *y;
    *y = temp;
}

void selectionSort(int A[], int n){
    int i,j,k;
    for(i = 0; i< n -1 ; i++){
        for( j = k = i; j<n; j ++){
            if(A[j] < A[k]){
                k = j;
            }
        }
        swap(&A[i], &A[k]);
    }
}
int main(int argc, const char * argv[]) {
    int A[] = {11,13,7,2,6,9,4,5,10,3}, n = 10, i;
    selectionSort(A,n);

    for(i = 0;i< n; i++){
        printf("%d ",A[i]);
    }
}

```

Java

```java
import java.util.Arrays;

public class SelectionSort {
    // Este algoritmo lo que hace es ir moviéndose indice por indice e ir colocando en orden el valor
    // mas pequeño que vaya encontrando en el arreglo
    public static void sort(int[] values){
        int temp = 0;
        int size = values.length;
        int minValIndex = 0;
        for (int i = 0; i < size; i++){
            minValIndex = i;
            for (int j = i+1; j < size; j++){
                if(values[j] < values[minValIndex]){
                    minValIndex = j;
                }
            }
            temp = values[i];
            values[i] = values[minValIndex];
            values[minValIndex] = temp;
        }
    }

    public static void main(String[] args) {
        int[] values = {2,7,1,4,3,5,0,8,2,-1,2};
        sort(values);
        System.out.println(Arrays.toString(values));
    }
}
```
