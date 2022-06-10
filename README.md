# Projeto Jogo da Velha
Faça um "jogo da velha" criando uma matriz em duas dimensões (Você deve criar um array com 3 arrays de 3 elementos cada dentro). O programa deve pedir as coordenadas (linha e coluna) alternadamente para 2 jogares e marcar `X` ou `O` em cada caso. Caso um jogador vença, ele deve perguntar se desejam jogar mais uma vez, e registrar quem venceu aquela rodada, se os jogadores desejarem parar, o programa deve mostrar quem ganhou mais rodadas e quem é o grande vencedor.

### Funções do Projeto

* `iniciaMatriz(matriz)`: Recebe uma Array vazia e cria a matriz 3x3 responsável pelo controle do jogo, preenchendo com seus valores iniciais.
* `imprimeMatriz(matriz, placar)`: Recebe as variáveis, `matriz` e `placar`, imprimindo-as no terminal após a jogada de cada **jogador**.
* `versusAI`: Pergunta através do `prompt` se a partida será realizada contra outro **Jogador** ou contra o **Computador**. Retorna valor `booleano`:`true` ou `false`.
* `lerJogada(matriz)`: Lê a posição que o **Jogador** deseja efetuar a jogada, tratando a entrada e verificando se é uma posição livre. Retorna um *número* que representa posição no campo de jogo que a jogada será realizada.
* `computadorJoga(matriz)`: Semelhante a função `lerJogada`, porém define a posição que o **Computador** jogará. A variável *\_jogada* recebe um valor da função `checaAI` caso satisfaça alguma condição, caso contrário jogará em uma *posição aleatória*.
* `escreveJogada(num, matriz, marca)` Onde `num`é o número da posição da `matriz` que receberá a `marca` correspondende ao **Jogador** desta rodada. Invoca `lerPosicao()` para converter `num` em coordenadas _**(i, j)**_. Escreve `marca` em `matriz[i][j]`.
* `lerPosicao(num)`: Converte um número `num` em uma coordenada _**(i, j)**_ de uma matriz 3x3.
* `darPosicao(i, j)`: Converte uma coordenada _**(i, j)**_ em um número que representa uma casa do jogo.
* `validaPosicao(num, matriz)`: Invoca `lerPosicao()` para converter `num` em coordadenas **_(i, j)_**, em seguida checa se a posição correspondente na matriz(i,j) esta vazia. Retorna valor `booleano`: *`true`* ou `false`.    
* `checaAI(matriz)`: Executa testes para definir se o computador fará alguma jogada específica, na seguinte ordem: 
  1. Checa se há uma jogada que garanta sua vitória;
  2. Checa se há uma jogada que evita sua derrota iminente;
  3. Caso contrário retorna `null`.
* `checaVencedor(matriz)`: Varre a `matriz` checando se algum dos jogadores venceu a partida. Se não há vencedores retorna `false`. 
* `matrizCheia(matriz)`: Checa se não há mais jogadas possíveis retornando o `boolean`:`true` no caso de cheia, se econtrar uma casa vazia retorna `false`. 
* `anunciaVencedor(vencedor, matriz, placar)`: Imprime quem foi o `vencedor`, a `matriz` do jogo e o `placar`.
* `jogarNovamente()`: Pergunta se o **jogador** deseja continuar jogando através do `prompt`. **Não** é *CaseSensitive* e aceita `s, sim, n, nao` como resposta. Retorna valor `booleano`: *`true`* ou `false`.
* `novaRodada(matriz, placar)`: Reinicia a `matriz` para iniciar nova rodada, invoca `imprimeMatriz()`.
* `anunciaCampeao(placar)`: Recebe `placar`, define o campeão e define o grande vencedor ao final de todas as rodadas.          

### Variáveis de Controle
* `matriz`: Acumula os valores relacionaos ao campo do jogo da velha. É uma matriz de duas dimensões.
* `placar`: Conta as rodadas vencidas pelo **Jogador 1** e pelo **Jogador 2**.
* `vsAI`: Controla se o jogo será realizado contra o **Computador** ou contra outro **Jogador**.
* `vencedor`: Controla se há um vencedor nessa rodadas. Se diferente de `false` há um vencedor. 
* `indica_turno`: Controla se é o turno do **Jogador 1** ou do **Jogador 2**. 

**Autor.** [Flavio Alvarenga](https://github.com/alvalenda)

---

**Linguagem.** JavaScript                                                          
**Tecnologias.** Node.JS, JavaScript Vanilla

---
 
