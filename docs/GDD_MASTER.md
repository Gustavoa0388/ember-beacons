# GDD MASTER — Ember Beacons

## 1. High Concept
* **Título do Repositório:** `ember-beacons`
* **Gênero:** Aventura, exploração em mundo semiaberto, puzzles e ação tática/técnica com transição dinâmica de câmera e ritmo, sem construção de base.
* **Engine Alvo:** Godot 4.x.
* **Público-Alvo:** Jogadores de títulos indie focados em mistério narrativo, exploração recompensadora, variedade de situações e combate ágil sem exigências de produção AAA.

## 2. Pilares de Design
1. **Narrativa de Investigação e Virada:** A história avança por descobertas ambientais, diálogos e evidências sobre os Faróis, a névoa e quem manipula o medo do povo.
2. **Exploração Semiaberta Guiada:** Liberdade para explorar regiões, vilas e missões secundárias opcionais, com bloqueios naturais/narrativos que conduzem a progressão principal sem mundo aberto vazio.
3. **Base Unificada, Ritmos Variados:** O personagem mantém os mesmos atributos, armas, armaduras, relíquias e upgrades; o que muda conforme o local ou situação é o ângulo da câmera, a leitura espacial e o estilo de combate.
4. **Escopo Enxuto e Iterativo:** Construção em fatias verticais testáveis, evitando retrabalho de arte e código.

## 3. Progressão e Ciclo de Tempo (Sem Construção de Base)
* **Recursos Coletados:** Minérios, Âmbar Bruto, Reagentes da Névoa, Moedas e Fragmentos Raros.
* **Destino dos Recursos:** Melhorias diretas de **Arma**, **Armadura/Mobilidade**, **Relíquias/Poderes** e **Itens Especiais** (como lamparina/antídoto). Não há base para construir ou gerenciar.
* **Ciclo Dia / Noite (Maré da Névoa):**
  * **Dia (Maré Baixa):** Maior visibilidade, rotina ativa em vilas/castelos, inimigos com comportamento padrão, foco em exploração, missões e puzzles externos.
  * **Noite (Maré Alta):** A névoa avança, altera iluminação global, torna criaturas mais agressivas/mutadas e aumenta o risco — mas libera recursos raros de upgrade.

## 4. Modos de Jogo e Transições
* **Mundo Semiaberto (Isométrico):** Exploração livre dentro das áreas liberadas, vilas/cidades, NPCs, missões principais e secundárias, combate rápido com pegada *hack and slash* sem virar botão-mash cego (com pressão/risco de *roguelike* em incursões).
* **Ruínas, Cavernas e Torres (2.5D Lateral):** Câmera lateral com avanço horizontal/vertical, plataformas e puzzles.
* **Missões com Aliados (RPG Tático por Turnos):** Quando 1 ou 2 aliados acompanham o protagonista em missões específicas, o combate ocorre em turnos táticos coordenando o grupo.
* **Zonas de Infiltração (Stealth & Puzzles):** Áreas vigiladas ou de baixa luz onde furtividade, luz/sombra e enigmas destravam o avanço.
* **Chefes de Ruína / Farol (Roguelike + Soulslike):** Encontros de maior exigência técnica, leitura de padrões, janela de esquiva/ataque e punição real.
* **Transições:** Curtas (1–2s) e integradas ao mundo: poeira/névoa + *fade* rápido, portões abrindo, escurecimento ao entrar em caverna com acender de lamparina e nova iluminação/câmera, ou encerramento de diálogo já posicionando o grupo no modo tático.

## 5. Fatia Vertical do Protótipo (MVP Jogável)
1. **Vila de Cinza-Clara (Isométrico):** Conversa inicial com `npc_aldric` + 1 missão secundária simples de coleta.
2. **Bosque da Fronteira (Isométrico + Dia/Noite):** Combate rápido e coleta de recursos para 1 upgrade.
3. **Estrada dos Apagadores (RPG Tático por Turnos):** 1 aliado entra no grupo para enfrentar uma emboscada após diálogo.
4. **Catacumba do Farol Caído (2.5D Lateral + Stealth/Puzzle):** Entrada com lamparina acendendo, 1 puzzle e 1 trecho de furtividade.
5. **Altar do Farol (Chefe Soulslike/Roguelike):** Derrotar o guardião corrompido e reacender o primeiro Farol.