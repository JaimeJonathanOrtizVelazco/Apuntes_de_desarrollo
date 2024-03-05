# Pila / Stack

Es una estructura de datos linear que sigue una particularidad en las operaciones que realizar. Esta es que el orden de entrada y salida es de tipo LIFO(Last In First Out) o FILO ( First In Last Out). Principalmente operaciones en el stack:

- Push : Agrega un elemento a la colección
- Pop : Remueve un elemento de la colección.
- Peek or Top: Regresa el elemento en lo mas alto de la pila
- IsEmpty: Regresa si la lista esta vacio o no
- IsFull: Nos dice si ya no hay espacio en la lista

```java
import java.util.ArrayDeque;
import java.util.Deque;

public class Example {
public static void main(String[] args) {
Deque<Integer> stack = new ArrayDeque<>();

        // Adding elements (push)
        stack.push(10);
        stack.push(20);
        stack.push(30);

        // Accessing the top element
        int topElement = stack.peek();
        System.out.println("Top element: " + topElement);

        // Removing elements (pop)
        stack.pop();
        topElement = stack.peek();
        System.out.println("Top element after pop: " + topElement);
    }

}
```
