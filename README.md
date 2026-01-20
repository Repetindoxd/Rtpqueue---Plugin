
# 🌀 RTPQueue

> **Sistema Avançado de Matchmaking e Teletransporte Aleatório (RTP)**

O **RTPQueue** é um plugin de alta performance para servidores competitivos (Minecraft 1.21+). Ele combina um sistema de filas inteligente com teletransporte estratégico, ideal para servidores de PvP que buscam organizar duelos de forma justa e automatizada.

---

## ✨ Funcionalidades Principais

### ⚖️ Filas Inteligentes

* **Fila Sem Crystal:** Focada em combate clássico. O plugin monitora o inventário em tempo real para impedir o uso ou posse de End Crystals.
* **Fila Com Crystal:** Combate livre, sem restrições de itens.

### ⚔️ Matchmaking Dinâmico

* **Countdown Visual:** Ao encontrar um oponente, um título centralizado é exibido com um subtítulo de contagem regressiva (5 segundos).
* **Segurança de Conexão:** O processo é cancelado instantaneamente se um dos jogadores desconectar antes do teletransporte.
* **Action Bar Persistente:** Mostra o status da fila: `Jogadores na fila [1/2] - Tempo: MM:SS`.

### 🗺️ Teletransporte Estratégico (RTP)

* **Posicionamento Preciso:** Os oponentes são teleportados para uma área aleatória, mas surgem a exatamente **9 blocos de distância** um do outro.
* **Efeito de Glowing (Brilho):** Ambos recebem o efeito de brilho ao iniciar. A cor é totalmente customizável via `config.yml` através do sistema de *Teams* do Minecraft.

### 🛡️ Segurança e Restrições

* **Anti-Cheat Manual (Crystal):** Se um jogador da "Fila Sem Crystal" obtiver o item (drop ou pick-up), ambos são teleportados para locais diferentes e uma penalidade é aplicada.
* **Requisito de Equipamento:** É possível exigir que o jogador esteja vestindo armaduras específicas (ex: Netherite) para acessar o menu de filas.

---

## 🛠️ Comandos e Permissões

| Comando | Descrição | Atalhos | Permissão |
| --- | --- | --- | --- |
| `/rtpqueue` | Abre o menu GUI de seleção de fila | `/fila`, `/q` | *Livre* |
| `/fila sair` | Remove o jogador da fila atual | - | *Livre* |
| `/fila reload` | Recarrega as configurações do plugin | - | `rtpqueue.admin` |

---

## ⚙️ Configuração (`config.yml`)

O plugin suporta cores clássicas (`&`) e **Hexadecimal** (`&#FFFFFF`).

### Placeholders Disponíveis:

* `%queue%`: Nome da fila selecionada.
* `%size%`: Quantidade de jogadores na fila.
* `%time%`: Cronômetro de espera formatado.

### Exemplo de Estrutura RTP:

```yaml
rtp:
  radius: 1000          # Raio máximo do teletransporte
  world: "world_pvp"    # Mundo do combate
  glowing-duration: 15  # Segundos de brilho
  glowing-color: "RED"  # Cor do Team (RED, AQUA, GOLD, etc)

```

---

## 🚀 Instalação

1. Baixe o arquivo `.jar` na aba Releases.
2. Coloque-o na pasta `plugins` do seu servidor.
3. Reinicie o servidor ou utilize um gerenciador de plugins.
4. Configure as mensagens e mundos no `config.yml`.

---

*Desenvolvido para servidores competitivos de alta performance.*

---
