# Bubble Sort

Basicamente este ira comparando uno a un los valores del arreglo. Si el valor anterior es mayor que el siguiente, estos intercambian lugares y continuamos la validacion con el nuevo valor intercambiado; es decir, el valor mas grande que a sido intercambiado, de esta manera, siempre tendremos los valores mas grandes al final del arreglo de manera ordernada. Por lo que, no sera necesaria iterar hasta el ultimo valor del arreglo.

https://www.toptal.com/developers/sorting-algorithms/bubble-sort
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

void Bubble(int A[], int n){
    int i, j, flag = 0;
    for(i = 0; i < n -1;i++){
        flag = 0;
        for(j = 0; j < n -i-1; j ++){
            if(A[j] > A[j + 1]){
                swap(&A[j], &A[j+1]);
                flag = 1;
            }
        }
        if ( flag == 0){
            break;
        }
    }
}

int main(int argc, const char * argv[]) {
    int A[] = {3,7,9,10}, n = 4, i;
    Bubble(A,n);

    for(i = 0;i< n; i++){
        printf("%d ",A[i]);
    }
}

```

Java

```java
import java.util.Arrays;

public class BubbleSort {
    // Bubble sort cambia el valor de v[i] por v[i+1] si este ultimo es menor que v[i].
    // Colocando los valores mas grandes hasta el final del arreglo.
    // Con esto podemos evitar iterar hasta el ultimo valor mas alto del arreglo, es decir, como
    // los valores mas grandes estan hasta al final de manera ordenada, ya necesitamos validar esos valores
    public static void sort(int [] values){
        int size = values.length - 1;
        boolean ordered = false;
        int lastIndex = size;
        while(!ordered){
            ordered = true;
            for (int j = 0; j <  lastIndex; j++){
                if (values[j] > values[j+1]){
                    int temp = values[j];
                    values[j] = values[j+1];
                    values[j+1] = temp;
                    ordered = false;
                }
            }
            lastIndex --;
            System.out.println(Arrays.toString(values));
        }
    }

    public static void main(String[] args) {
        int[] values = {2,7,1,4,3,5,0,8,2,-1,2};
        sort(values);
        System.out.println(Arrays.toString(values));
    }
}
```
