# Simulação de Herança de Tipos Sanguíneos
## Descrição:

Este programa simula a herança de tipos sanguíneos ao longo de gerações em uma família. O tipo sanguíneo de uma criança é determinado pelas alelos herdados de seus pais. Os três possíveis alelos são 'A', 'B' e 'O'. Cada pessoa na família possui dois alelos, que são herdados de seus pais. O programa atribui alelos aleatórios à geração mais antiga e os propaga para as gerações mais jovens, simulando o processo de herança.
## Utilização:

Para executar a simulação, compile o arquivo inheritance.c e execute o programa.

    gcc inheritance.c -o inheritance
    ./inheritance

O programa solicitará que você insira o número de gerações para a família. Digite um número inteiro positivo maior ou igual a 1.

A simulação criará uma árvore genealógica com o número especificado de gerações. Cada pessoa terá seus alelos de tipo sanguíneo atribuídos aleatoriamente, e seus pais serão vinculados de acordo.

O programa imprimirá a árvore genealógica e exibirá os tipos sanguíneos de cada membro da família.

Para limpar e liberar a memória alocada para a árvore genealógica, pressione Ctrl + C no terminal para encerrar o programa.
## Detalhes da Implementação:

O programa utiliza uma abordagem recursiva para criar a árvore genealógica e atribuir os alelos de tipo sanguíneo.

  * A função create_family recebe um inteiro generations como entrada e cria uma árvore genealógica com o número especificado de gerações. Ela retorna um ponteiro para a pessoa mais jovem na família. A geração mais antiga tem alelos atribuídos aleatoriamente, enquanto as gerações mais jovens herdam um alelo de cada pai.

  * A função free_family recebe um ponteiro para uma pessoa e libera recursivamente a memória para a pessoa e todos os seus ancestrais na árvore genealógica. Ela lida com o caso base em que o ponteiro de entrada é NULL, indicando que não há nada para liberar.

## Escolhas de Projeto:

  * O programa utiliza uma estrutura person para representar cada indivíduo na árvore genealógica. Cada pessoa possui dois alelos e um array de ponteiros para seus pais.

  * Os alelos de tipo sanguíneo são atribuídos aleatoriamente usando a função random_allele.

  * O programa utiliza um gerador de números aleatórios para simular a herança aleatória de alelos dos pais para os filhos.
