# Merge Sort

Lo que se hace en este algoritmo es aplicar la funcion de divide y venceras. Vamos a tomar subsstring pequeños del arreglo, los vamos a ordenar en un nuevo arreglo y posteriormente vamos a remplazar este arreglo ordenado en las posiciones del substring al que empezamos a manipular.

https://www.toptal.com/developers/sorting-algorithms/merge-sort

C++ Version Recursiva

```c++
#include <stdio.h>

void swap(int *x, int *y){
    int temp;
    temp = *x;
    *x= *y;
    *y = temp;
}


void Merge(int A[],int l, int mid, int h){
    int i = l,j=mid+1,k = l;
    int B[100];
    while(i<=mid && j<=h){
        if ( A[i] < A[j]){
            B[k++] = A[i++];
        } else{
            B[k++] = A[j++];
        }
    }
    for(;i<= mid;i++){
        B[k++] = A[i];
    }
    for(;j<=h;j++){
        B[k++] = A[j];
    }
    for(int i=l;i<=h;i++){
        A[i] = B[i];
    }
}


void RecursiveMergeSort(int A[], int low, int high){
    if (low < high){
        // Calculate mid point
        int mid = low + (high-low)/2;

        // Sort sub-lists
        RecursiveMergeSort(A, low, mid);
        RecursiveMergeSort(A, mid+1, high);

        // Merge sorted sub-lists
        Merge(A, low, mid, high);
    }
}


int main(int argc, const char * argv[]) {
    int A[] = {11,13,7,12,16,9,24,5,10,3}, n = 10, i;
    RecursiveMergeSort(A, 0, n-1);


    for(i = 0;i< n; i++){
        printf("%d ",A[i]);
    }
}
```

C++ Version Interativa

```c++
#include <stdio.h>

void swap(int *x, int *y){
    int temp;
    temp = *x;
    *x= *y;
    *y = temp;
}


void Merge(int A[],int l, int mid, int h){
    int i = l,j=mid+1,k = l;
    int B[100];
    while(i<=mid && j<=h){
        if ( A[i] < A[j]){
            B[k++] = A[i++];
        } else{
            B[k++] = A[j++];
        }
    }
    for(;i<= mid;i++){
        B[k++] = A[i];
    }
    for(;j<=h;j++){
        B[k++] = A[j];
    }
    for(int i=l;i<=h;i++){
        A[i] = B[i];
    }
}

void IMergeSort(int A[], int n){
    int p,l,h,mid,i;

    for(p=2; p <= n; p=p*2){
        for(i = 0; i+p-1<n;i=i+p){
            l =i;
            h = i+p-1;
            mid= (l+h) / 2;
            Merge(A, l, mid, h);
        }
    }
    if(p/2 < n){
        Merge(A,0,p/2-1,n);
    }
}

int main(int argc, const char * argv[]) {
    int A[] = {11,13,7,12,16,9,24,5,10,3}, n = 10, i;
    IMergeSort(A,n-1);

    for(i = 0;i< n; i++){
        printf("%d ",A[i]);
    }
}

```
