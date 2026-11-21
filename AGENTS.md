# AGENTS.md — Regras de Colaboração (`ember-beacons`)

Este projeto é desenvolvido com apoio de múltiplas IAs sob direção humana. Respeite os limites de cada agente para evitar retrabalho e conflitos de arquivos.

## 1. Papéis e Escopo de Pastas
* **Gemini (Narrativa, Design e Dados):** Responsável por `docs/` (`GDD_MASTER.md`, `LORE_BIBLE.md`, `ART_PROMPTS.md`) e `data/` (`.json` de personagens, itens, upgrades, missões e diálogos).
* **ChatGPT (Direção de Arte e Assets):** Responsável por gerar artes/sprites/retratos/cenários alinhados a `docs/ART_PROMPTS.md` para organização em `assets/`.
* **Claude Code (Engenharia Godot 4.x):** Responsável por `godot/` (cenas `.tscn`, scripts `.gd`, singletons, transições e sistemas jogáveis) e organização técnica no repositório.
* **Diretor / QA (Usuário):** Define prioridades, aprova entregas e testa o jogo na prática.

## 2. Regras de Ouro (Anti-Retrabalho)
1. **IDs são sagrados:** Não altere IDs definidos em `data/*.json` sem manter compatibilidade com cenas, diálogos e scripts existentes.
2. **Sem expansão de escopo sem aprovação:** Não adicione mecânicas fora do GDD (como construção de base) nem reescreva sistemas inteiros quando um ajuste pontual resolve.
3. **Progressão e ações unificadas:** Armas, armaduras, relíquias, recursos e comandos base do jogador permanecem consistentes; o que muda entre áreas/encontros é a câmera, a apresentação e as regras do modo (Isométrico, 2.5D Lateral, Tático por Turnos, Stealth/Puzzles e Chefes).
4. **Respeite o estado da Fatia Vertical:** Priorize fazer o ciclo jogável funcionar ponta a ponta antes de expandir o mundo ou adicionar conteúdo secundário excessivo.

## 3. Boas Práticas Entre Agentes
* Ao criar ou atualizar dados em `data/`, mantenha JSON válido e campos consistentes com os scripts da Godot.
* Ao criar ou ajustar cenas/scripts em `godot/`, evite quebrar referências e caminhos existentes.
* Em caso de dúvida sobre história, tom, reviravoltas ou intenção de gameplay, consulte/atualize `docs/GDD_MASTER.md` e `docs/LORE_BIBLE.md`.