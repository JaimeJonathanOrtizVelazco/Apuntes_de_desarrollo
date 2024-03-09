# Búsqueda Binaria / Binary Search

Es un tipo de algoritmo de búsqueda que sigue la estrategia de divide y vencerás. Funciona en arreglos ordenados al dividir de manera repetida el intervalo de búsqueda a la mitad. Por lo que inicialmente el primer elemento que se utiliza para comparar es el de la mitad del intervalo que estamos validando. Si el valor buscado es mayor, tomamos el intervalo que va desde la mitad del intervalo a la derecha, pero es es menor, usamos el intervalo que va de la mitad hacia la izquierda. Volvemos a realizar esta operación hasta encontrar el elemento buscado.

C++

```c++

struct Node * Search(int key){
    struct Node *t=root;

    while(t!=NULL){
        if(key == t->data){
            return t;
        } else if(key < t->data){
            t = t->lchild;
        } else{
            t = t->rchild;
        }
    }
    return NULL;
}

```

Java

```java
private static void searchNodeTree(int value, boolean delete) {
        int count = 0;
        BTree aux = root;
        BTree parent = null;
        while (aux != null) {
            if (value == aux.number) {
                break;
            }
            parent = aux;
            if (value < aux.number) {
                aux = aux.left;
            } else {
                aux = aux.right;
            }
            count++;
        }
        if (aux == null) {
            System.out.println("Value not found");
        } else {
            if (!delete) {
                System.out.println("Node found after " + count + " iterations");
            } else {
                if(parent != null){
                    if(parent.left.number == value){
                        parent.left = null;
                    }else{
                        parent.right = null;
                    }
                }
                System.out.println("Node with value "+value+" and its descendent nodes have been deleted");
            }
        }
    }
```

Java array example

```java
private static int binarySearch0(long[] a, int fromIndex, int toIndex,
                                     long key) {
        int low = fromIndex;
        int high = toIndex - 1;

        while (low <= high) {
            int mid = (low + high) >>> 1;
            long midVal = a[mid];

            if (midVal < key)
                low = mid + 1;
            else if (midVal > key)
                high = mid - 1;
            else
                return mid; // key found
        }
        return -(low + 1);  // key not found.
    }
```
