### Pontos importantes sobre BST

#### Busca
Árvore eficiente para a busca. Todos os filhos da esquerda são menores que o nó raíz e vice versa.
Se não for balanceada, pode perder a propriedade de eficiência da busca.
    
Uma árvore binária de busca é uma estrutura de dados de árvore que é usada para armazenar e recuperar elementos. Ela funciona baseada em uma propriedade de ordenação: para cada nó da árvore, todos os elementos na subárvore esquerda são menores que o elemento do nó e todos os elementos na subárvore direita são maiores. Isso permite realizar buscas eficientes, pois o algoritmo pode descartar metade dos elementos em cada iteração.
1.1. A propriedade de ordenação que uma árvore binária de busca deve obedecer é que para cada nó da árvore, todos os elementos na subárvore esquerda são menores que o elemento do nó e todos os elementos na subárvore direita são maiores.

1.2. A árvore binária de busca é usada para implementar uma estrutura de dados de árvore porque sua propriedade de ordenação permite realizar buscas eficientes. Além disso, a árvore binária de busca é fácil de implementar e usar.

1.3. A inserção de um elemento em uma árvore binária de busca envolve a busca pela posição correta para o elemento e a inserção dele na subárvore apropriada. A busca de um elemento na árvore envolve comparar o elemento buscado com o elemento de cada nó e descartar metade dos elementos em cada iteração, conforme o elemento é encontrado ou não.

1.4. A complexidade de tempo de inserção, busca e exclusão na árvore binária de busca é O(log n), onde n é o número de elementos na árvore.
