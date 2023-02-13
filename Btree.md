### Propriedades da Árvore B:
Todas as folhas estão no mesmo nível.
A Árvore B é definida pelo termo grau mínimo "t". O valor de "t" depende do tamanho do bloco de disco.
Todos os nós, exceto a raiz, devem conter pelo menos t-1 chaves. A raiz pode conter pelo menos 1 chave.
Todos os nós (incluindo a raiz) podem conter no máximo (2 * t - 1) chaves.
O número de filhos de um nó é igual ao número de chaves nele mais 1.
Todas as chaves de um nó estão ordenadas em ordem crescente. O filho entre duas chaves k1 e k2 contém todas as chaves no intervalo de k1 e k2.
A Árvore B cresce e diminui a partir da raiz, o que é diferente da Árvore de Busca Binária. As Árvores de Busca Binárias crescem para baixo e também encolhem para baixo.
Assim como outras Árvores de Busca Binárias balanceadas, o tempo de complexidade para pesquisar, inserir e excluir é O (log n).
A inserção de um Nó na Árvore B ocorre apenas em Nó Folha.

Busca
Operação de Busca na Árvore B: A busca é similar à busca na Árvore de Busca Binária. Considere a chave a ser procurada como k.

Comece a partir da raiz e percorra recursivamente para baixo. Para cada nó não folha visitado, se o nó tiver a chave, retornamos simplesmente o nó. Caso contrário, recorremos para o filho adequado (o filho que é imediatamente antes da primeira chave maior) do nó. Se chegarmos a um nó folha e não encontrarmos k no nó folha, retornamos NULL. Procurar uma Árvore B é similar a procurar uma árvore binária. O algoritmo é semelhante e usa recursão. Em cada nível, a busca é otimizada, pois se o valor da chave não estiver presente no intervalo do pai, a chave estará presente em outra ramificação. As these values limit the search they are also known as limiting values or separation values. If we reach a leaf node and don’t find the desired key then it will display NULL.


### Insertion 
Inicialize x como a raiz da árvore B.
Enquanto x não é uma folha, faça o seguinte:
2.1. Encontre o filho de x que será percorrido em seguida. Deixe o filho ser y.
2.2. Se y não estiver cheio, altere x para apontar para y.
Se y estiver cheio, insira k (a chave que desejamos inserir) em y. Se a inserção causar a superação da capacidade de y, então divida y e altere x para apontar para uma das duas partes de y. Se k for menor que a chave do meio em y, altere x para a primeira parte de y, caso contrário altere x para a segunda parte de y. Quando dividimos y, movemos uma chave de y para seu pai x.
O loop no passo 2 para quando x é uma folha.
Observe que essa abordagem é chamada de inserção "reativa" porque divide um nó apenas quando é necessário inserir uma nova chave, ao invés de dividi-lo antes de percorrê-lo. Isso pode levar a uma travessia repetida dos nós da árvore em casos onde todos os nós a partir da raiz até a folha estão cheios. Entretanto, a vantagem é que se evita realizar divisões desnecessárias.
