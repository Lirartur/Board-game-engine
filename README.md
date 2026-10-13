# Jogo da Velha — Board Game Engine (Checkpoint 1)

Trabalho da disciplina de **Linguagem de Programação Orientada a Objetos (LPOO)** na POLI/UPE[cite: 2]. O projeto é uma implementação do jogo da velha, desenvolvido em Java, dividindo as responsabilidades em classes e aplicando conceitos de lógica de programação e orientação a objetos[cite: 8, 10].

---

## 🏗️ Estrutura do Código

O código está estruturado por meio de três arquivos principais[cite: 1]:

- **`Jogodavelha` (`Main`)**: Classe principal do programa. Contém o método `main`, que atua como ponto de partida da aplicação, sendo responsável por instanciar a classe `Jogo` e chamar o método para iniciá-lo[cite: 22].
- **`Jogo`**: Atua como o controlador da partida, gerenciando o loop principal do jogo, alternância de turnos, validação e leitura de dados do usuário via terminal.
- **`Tabuleiro`**: Responsável por gerenciar os dados e a exibição do estado da grade. A grade é uma matriz 3x3 inicializada com espaços vazios.

---

## 📐 Diagrama de Classes

Abaixo está o diagrama de classes da solução desenvolvida para o Checkpoint 1[cite: 10]:

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
