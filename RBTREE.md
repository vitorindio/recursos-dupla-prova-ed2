### Pontos importantes sobre RBT 

#### 1- qual é o calculo para encontrar a menor e maior quantidade de nos em uma arvore rubro-negra ? 
- A menor quantidade de nós em uma árvore Rubro-Negra de altura h é dada por 2^h - 1. A razão para isso é que cada nível da árvore precisa ter pelo menos dois nós, exceto o nível mais baixo, que pode ter um nó. Portanto, o número total de nós é dado por:
    2^0 + 2^1 + ... + 2^(h-1) = 2^h - 1

    A maior quantidade de nós em uma árvore Rubro-Negra de altura h é dada por (2^(h+1)) - 1. A razão para isso é que, em cada nível da árvore, todos os nós podem ter dois filhos. Portanto, o número total de nós é dado por:
    2^0 + 2^1 + ... + 2^h = (2^(h+1)) - 1

    Portanto, a menor quantidade de nós em uma árvore Rubro-Negra de altura 8 é 2^8 - 1 = 255 e a maior quantidade de nós é (2^9) - 1 = 511.  
    
    
#### 2- Propriedades + conceitos arvore rubro negra
- Todos os nós são coloridos ou Rubro ou Preto.
    A raiz é Preta.
    Todos os filhos de um nó Rubro são Pretos.
    Para todo nó, a quantidade de nós Pretos na subárvore esquerda é igual à quantidade de nós Pretos na subárvore direita.
    Todas as folhas (nós NIL) são Pretas.
    Se estas propriedades estiverem sendo satisfeitas, a árvore Rubro-Negra está balanceada.

    altura de uma árvore Rubro-Negra pode ser determinada percorrendo a árvore e encontrando o caminho mais longo até a folha. A altura da árvore é o comprimento desse caminho. Em uma árvore Rubro-Negra balanceada, a altura da árvore é garantida para ser logarítmica em relação ao número de nós na árvore.
      
