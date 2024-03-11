# Arboles AVL / AVL Trees

Es un tipo de árbol binario que es auto balanceado, lo que significa la diferencia de los pesos de los dos subarboles hijos de cualquier nodo debe ser a lo mucho 1. Si la diferencia de los pesos es mayor a 1, se debe realizar el rebalanced.

Los arboles AVL se balancean a si mismo al rotar los subarboles in diferentes maneras llamados:

- LL Left-Left rotation
- RR Right-Right rotation
- LR Left-Right rotation
- RL Right-Left rotation

Las interiores direcciones de rotación se determinan con forme a la dirección de inserción del ultimo elemento que ocasionó que el el árbol se desvalanciara.
