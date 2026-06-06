# PROJETO-DUNGEON-CRAWLER

## 📝 Visão Geral e História
O jogo do gênero *dungeon crawler* com perspectiva *top-down*, desenvolvido inteiramente na linguagem C e executado diretamente no console utilizando caracteres ASCII para a representação visual.

### A História
> *"["A cidade de Belém foi tomada pelo Senhor das Trevas, e você é a última esperança de salvá-la!"]"*

---

## 👥 Desenvolvedores
* **[Lucas Quaresma Sadala]**

---

## 🎮 Como Jogar e Controles

### Objetivo
O jogador começa sua jornada em uma Vila pacífica onde deve escolher sua arma. Em seguida, deve adentrar uma masmorra composta por 3 andares progressivamente mais desafiadores, coletando chaves, abrindo portas, superando armadilhas e derrotando monstros até vencer o Boss Final.

### Sistema de Vidas
* O jogador inicia a partida com **3 vidas**.
* Colidir com espinhos (`#`) ou ser tocado por um monstro (`X` ou `Y` ou 'Z') faz o jogador perder **1 vida** e reinicia o andar atual a partir do ponto inicial.
* Perder todas as 3 vidas resulta em **Game Over** e o jogador retorna ao menu principal.

### Controles no Teclado
A movimentação e o combate ocorrem de forma ortogonal (sem movimentos diagonais):

| Tecla | Ação |
| :---: | --- |
| **W** | Move o jogador para **cima** (muda o visual para `^`) |
| **A** | Move o jogador para a **esquerda** (muda o visual para `<`) |
| **S** | Move o jogador para **baixo** (muda o visual para `v`) |
| **D** | Move o jogador para a **direita** (muda o visual para `>`) |
| **E** | Interage com o objeto/NPC diretamente à frente |
| **O** | Realiza um ataque na célula/área à frente (baseado na arma escolhida) |

---

## 🗺️ Elementos do Mapa (Símbolos ASCII)

### Personagens e Monstros
* `^`, `<`, `>`, `v` : O **Jogador** (indicando a direção para onde está olhando).
* `X` : **Monstro Tipo 1** (Movimentação completamente aleatória a cada turno).
* `Y` : **Monstro Tipo 2** (Perseguição simples, move-se na direção que reduz a distância até o jogador).
* `Z` : **Boss Final** (Perseguição e muitas vidas).

### Cenário e Objetos
* `*` : **Parede** (Obstáculo intransponível).
* `#` : **Espinho** (Causa dano/perda de vida e reinicia a fase).
* `k` : **Caixa** (Bloqueia o caminho, mas pode ser destruída com um ataque).
* `O` : **Botão** (Executa uma ação ou gatilho no mapa ao ser pressionado).
* `D` : **Porta Fechada** (Bloqueia a passagem até que uma chave seja usada).
* `=` : **Porta Aberta** (Passagem livre).
* `@` : **Chave** (Item coletável necessário para abrir as portas).
* `L` : **Escada** (Leva o jogador para o próximo andar; liberada após resolver os desafios).

---

## ⚔️ Arsenal (Armas Disponíveis)
No NPC da Vila, você deve escolher uma das três armas abaixo. O padrão de ataque é espelhado de acordo com a direção que o jogador está olhando:

* **Espada:** Ataca uma área de $3 \times 2$ diretamente à frente.
* **Arco e Flecha:** Ataca em linha reta, atingindo as 4 células consecutivas à frente.
* **Cajado:** Ataca simultaneamente as 8 células adjacentes ao redor do jogador (independe da direção).

---
