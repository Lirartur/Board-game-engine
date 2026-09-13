# Board-game-engine
Trabalho da disciplina de Linguagem de Programação orientada a Objetos
O projeto é uma implementação do jogo da velha, desenvolvido em Java. O projeto foi desenvolvido dividindo em classes, aplicando conceitos de lógica de programação e orientação a objetos.

O código está estruturado em três arquivos principais:
  Jogodavelha (main): É a classe principal do programa. Ela contém o método main, que atua como ponto de partida da aplicação, sendo responsável apenas por instanciar a classe Jogo e chamar o método para iniciá-lo
  Jogo: atua como o controlador da partida, gerenciando o loop principal do jogo, alternância de turno, leitura de dados, etc.
  Tabuleiro: Responsável por gerenciar os dados e a exibição do estado da grade. A grade representada é uma matriz 3x3, iniciando todas as posições com um espaço vazio de partida.

Como jogar:
  A grade é enumerada da esquerda para direita, de cima pra baixo; a primeira linha é representada por: 1,2,3 e a segunda: 4,5,6 e a terceira linha: 7,8,9.
  A partida começa com o jogador "X" e quando for sua vez, será necessário digitar o número da posição desejada e será informado caso a localização seja inválida ou esteja em uso. O jogo será terminado caso um jogador complete uma trinca ou após um total de 9 jogadas sem que ninguém vença (empate).
