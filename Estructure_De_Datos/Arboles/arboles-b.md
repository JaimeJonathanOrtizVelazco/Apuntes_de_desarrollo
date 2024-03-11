# B-Tree

Es una estructura de arboles autobalanceados que mantiene la información ordenada y permite eficientes operaciones de inserción, eliminación y búsqueda.

La principal característica de estos arboles es que las hojas se mantiene al mismo nivel y que los nodos internos pueden almacenar mas de una llave.

Cada nodo dentro del B-tree contiene cierto numero de llaves y punteros para navegar en el árbol.
Las llaves actúan como valores individuales que dividen al árbol.

Por ejemplo, un nodo que contenga los valores 10, 20 y 30. Este entra 4 nodos hijos. El primero: que tenga valores menores a 10. El segundo, que tenga valores entre 10 y 20. El tercero: Que tenga valores entre 20 y 30. Y el cuarto: Que tenga valores mayores a 30.
