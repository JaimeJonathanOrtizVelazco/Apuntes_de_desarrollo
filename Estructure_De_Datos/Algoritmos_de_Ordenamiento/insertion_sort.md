# Insertion Sort

Este algoritmo de ordenamiento básicamente lo que hace es iniciar iterando en la posición 1, tomar este valor como un valor tempera y empezar a recorrer los valores a la izquierda de la posición i de la iteración hacia la derecha hasta encontrar el lugar correcto donde se debe de color el valor temporal de i.

https://www.toptal.com/developers/sorting-algorithms/insertion-sort

<br>
C++

```c++
void swap(int *x, int *y){
    int temp;
    temp = *x;
    *x= *y;
    *y = temp;
}

void InsertionSort(int A[], int n){
    int i,j,x;
    for(i = 1; i<n; i++){
        j = i -1;
        x= A[i];
        while(j > -1 && A[j] >x){
            A[j+1] = A[j];
            j--;
        }
        A[j+1] = x;
    }
}

int main(int argc, const char * argv[]) {
    int A[] = {11,13,7,2,6,9,4,5,10,3}, n = 10, i;
    InsertionSort(A,n);

    for(i = 0;i< n; i++){
        printf("%d ",A[i]);
    }
}
```

Java

```java
public class InsertionSort {
    public static void sort(int[] values){
        int temp = 0;
        int size = values.length;
        for (int i = 1; i< size; i++){
            temp = values[i];
            int j;
            for (j = i -1; j >=0 && values[j] > temp; j--){
                values[j + 1] = values[j];
            }
            values[j+1] = temp;
        }
    }

    public static void main(String[] args) {
        int[] values = {2,7,1,4,3,5,0,8,2,-1,2};
        sort(values);
        System.out.println(Arrays.toString(values));
    }
}
```
