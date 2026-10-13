# Jogo da Velha — Board Game Engine (Checkpoint 1)

Trabalho da disciplina de **Linguagem de Programação Orientada a Objetos (LPOO)**. O projeto é uma implementação do jogo da velha, desenvolvido em Java. O projeto foi desenvolvido dividindo as responsabilidades em classes, aplicando conceitos de lógica de programação e orientação a objetos[cite: 8, 10].

---

## 🏗️ Estrutura do Código

O código está estruturado em três arquivos principais[cite: 1]:

- **`Jogodavelha` (`Main`)**: É a classe principal do programa. Ela contém o método `main`, que atua como ponto de partida da aplicação, sendo responsável apenas por instanciar a classe `Jogo` e chamar o método para iniciá-lo[cite: 1, 10].
- **`Jogo`**: Atua como o controlador da partida, gerenciando o loop principal do jogo, a alternância de turnos, a leitura de dados do usuário e o fluxo geral da partida[cite: 1, 10].
- **`Tabuleiro`**: Responsável por gerenciar os dados e a exibição do estado da grade. A grade representada é uma matriz 3x3, iniciando todas as posições com um espaço vazio de partida[cite: 1, 4].

---

## 📐 Diagrama de Classes

Abaixo está o diagrama de classes da solução desenvolvida para o Checkpoint 1:

```mermaid
classDiagram
    class Jogodavelha {
        +main(args: String[])$ void
    }

    class Jogo {
        +tabuleiro: Tabuleiro
        +scanner: Scanner
        +iniciar(): void
    }

    class Tabuleiro {
        +celulas: char[][]
        +Tabuleiro()
        +inicializar(): void
        +posicaoOcupada(linha: int, coluna: int): boolean
        +marcar(linha: int, coluna: int, jogador: char): void
        +exibirEsquemaPosicoes()$ void
        +exibir(): void
        +verificarVitoria(jogador: char): boolean
    }

    Jogodavelha ..> Jogo : instancia
    Jogo "1" *-- "1" Tabuleiro : composição
