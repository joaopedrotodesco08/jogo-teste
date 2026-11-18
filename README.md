# 🚀 Cosmic Escape: Star Maze

Um jogo arcade de labirinto espacial desenvolvido em HTML5 Canvas, JavaScript puro e Tailwind CSS.

---

## 🎯 Objetivo do Jogo
Pilote a **Nave Branca** pelos corredores do labirinto estelar, desvie dos **3 foguetes perseguidores** e colete todas as **169 estrelas** espalhadas para alcançar a pontuação máxima e vencer o jogo!

---

## 🎮 Controles

| Ação | Teclado | Tela / Mouse |
|---|---|---|
| **Mover a Nave** | `W`, `A`, `S`, `D` ou `Setas Direcionais` | Botões do D-Pad virtual |
| **Iniciar / Reiniciar** | `Espaço` ou `Enter` | Botões na tela |
| **Pausar / Retomar** | `P` | Botão de pausa (topo) |
| **Ativar / Desativar Som** | `M` | Botão de áudio (topo) |

---

## 🛸 Elementos e Mecânicas

### 1. Nave Branca (Jogador)
- **3 Vidas:** Indicadas pelos ícones de naves no painel superior.
- **Escudo Protetor (Invulnerabilidade):** Ao ser atingida ou ao iniciar uma rodada, a nave recebe um campo de força ciano por alguns segundos, permitindo manobras de fuga sem sofrer dano consecutivo imediato.
- **Movimentação Suave:** Sistema de pré-buffer de comandos em encruzilhadas do labirinto, garantindo curvas responsivas e precisas.

### 2. Os 3 Foguetes Inimigos
Cada foguete possui uma cor, rastro característico e comportamento de inteligência artificial próprio:
- **Ares (Vermelho):** Perseguidor direto. Utiliza algoritmo BFS para caçar a nave branca pelo caminho mais curto.
- **Nova (Laranja):** Interceptador tático. Calcula o trajeto projetando 3 posições à frente da direção atual da sua nave para fechar sua passagem.
- **Comet (Roxo):** Patrulheiro errante. Percorre os quadrantes do labirinto e parte para perseguição ativa quando detecta a nave por perto.

### 3. As Estrelas e Pontuação
- **Estrelas Comuns (165 unidades):** Valem **+10 pontos** cada.
- **Super Estrelas / Pulsares (4 cantos do mapa):** Valem **+50 pontos** cada e ativam o modo de sobrecarga por 6 segundos! Durante a sobrecarga:
  - Os foguetes ficam lentos e vulneráveis (cor azul gélido).
  - Colidir com um foguete nesse estado elimina-o temporariamente (volta para a base) e concede **+200 pontos bônus**!
- **Vitória Estelar:** Ao zerar o contador de estrelas restantes, você vence o jogo com bônus extra por vidas remanescentes (**+500 pontos** por vida intacta).

### 4. Portais de Dobra (Warp Tunnels)
- Localizados nas extremidades esquerda e direita do labirinto central (marcador `◀` e `▶`). Ao atravessar um lado, sua nave se teletransporta instantaneamente para o outro extremo, ideal para despistar perseguições!

### 5. Áudio Sintetizado Nativo
- Efeitos sonoros espaciais gerados em tempo real pela **Web Audio API** do navegador (sem necessidade de arquivos de áudio externos).

---

## 📂 Como Executar

Abra o arquivo `index.html` em qualquer navegador web moderno:
```bash
open /Users/joaopedro/.gemini/antigravity/scratch/space-maze/index.html
```
Ou jogue diretamente pelo visualizador de artefatos interativos do Antigravity!
