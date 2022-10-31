# Truco

Jogo de truco programado em C++ como trabalho final da matéria de Programação 3 da Universidade Federal de Santa Catarina desenvolvido pelo aluno Gabriel Maçaneiro do Curso de Engenharia Mecatrônica de Joinville.

## Pré-requisitos

O compilador utilizado foi o GNU Compiler Collection na versão c++17. As bibliotecas externas utilizadas foram iostream, string, vector, random, algorithm, chrono e stdexcept. O código foi programado no codeblocks, no Windows para ser utilizado no Linux.

## Guia de Instalação

Para rodar a aplicação, é necessário apenas extrair o arquivo .zip em uma pasta, abrir o terminal do Linux nessa pasta e digitar o comando 'make'.

## O Código

O código foi programado em C++ orientado a objetos, todas as classes estão separadas em definição(arquivos .h) e implementação(arquivos .cpp). A interface do código será o próprio terminal do Linux. **Atenção: A execução do programa possui breves pausas de 3s ou 5s que são os tempos para o jogador poder analisar as cartas jogadas ou outras informações alertadas pelo código!**

## Sobre o Truco

###### Gírias importantes
Antes de apresentar os conceitos básicos e as regras do jogo é importante definir algumas gírias que serão utilizadas para explicação do jogo
- Partida: É um jogo que vale 12 pontos, conseguidos através das "mãos".
- Mão: Fração da partida onde cada jogador possui três cartas, começa valendo 1 ponto e pode ter seu valor aumentado para 3, 6, 9 ou 12.
- Rodada: Fração da "mão", em cada rodada os jogadores mostram uma carta.

###### Conceitos básicos
- Este truco foi programado para ser jogado entre uma pessoa e o próprio computador(Bot). 
- Possui um baralho de quarenta cartas.
- Antes de cada "mão" o baralho é embaralhado.
- No início de cada "mão", são distribuídas três cartas para cada jogador alternadamente e uma última carta representando o "vira".
- O vira determinará quem serão as manilhas daquela "mão".
- A carta com maior valor ganha a rodada.
- As manilhas são sempre as cartas subsequentes ao vira, são as cartas com maior valor da mão, entre elas não há empate e o valor do naipe determina qual carta tem maior valor.
- Segue abaixo tabelas com a sequência de valores das cartas e dos naipes.

Cartas | Valor
-------|------
4 | 0
5 | 1
6 | 2
7 | 3
Q | 4
J | 5
K | 6
A | 7
2 | 8
3 | 9

Naipes | Valor
-------|------
ouro | 0
espadas | 1
copas | 2
paus | 3

 - Um jogador pode levantar o valor da "mão". Assim, o outro jogador tem a opção de aceitar ou recusar, caso recuse, perde automaticamente aquela mão e o jogador que pediu para levantar o valor ganha o número de pontos que a "mão" estava valendo, caso aceite, a "mão" têm o valor aumentado para seu subsequente (se está valendo 1 passa a valer 3, se está valendo 3 passa a valer 6). **Um jogador não pode pedir para levantar o valor da mão duas vezes seguidas nem pedir para levantar se a "mão" já estiver valendo 12 pontos.**
 - O primeiro jogador a completar 12 pontos ou mais ganha a partida.
 - Por fim, segue tabela com todas as possíveis jogadas que uma "mão" pode ter e quem será o ganhador em cada caso

Rodada 1 | Rodada 2 | Rodada 3 | Ganhador
---------|----------|----------|---------
Pessoa Ganha | Pessoa Ganha | | Pessoa
Bot Ganha | Bot Ganha | | Bot
Pessoa Ganha | Empate | | Pessoa
Bot Ganha | Empate | | Bot
Empate | Pessoa Ganha | | Pessoa
Empate | Bot Ganha | | Bot
Pessoa Ganha | Bot Ganha | Pessoa Ganha | Pessoa
Pessoa Ganha | Bot Ganha | Bot Ganha | Bot
Bot Ganha | Pessoa Ganha | Bot Ganha | Bot
Bot Ganha | Pessoa Ganha | Pessoa Ganha | Pessoa
Pessoa Ganha | Bot Ganha | Empate | Pessoa
Bot Ganha | Pessoa Ganha | Empate | Bot
Empate | Empate | Pessoa Ganha | Pessoa
Empate | Empate | Bot Ganha | Bot
Empate | Empate | Empate | Ninguém

## Créditos

Desenvolvido por Gabriel Maçaneiro.
Contato: gabriel.macaneiro@hotmail.com
