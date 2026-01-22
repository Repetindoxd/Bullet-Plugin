## 🎮 Mecânica do Evento

O fluxo de jogo é projetado para ser fluido e automatizado, dividido em fases claras:

* **Fases do Jogo:** Ciclo completo entre **Espera** (Join), **Início** (Countdown), **Em Jogo** (Running) e **Finalização**.
* **Teleporte Automático:** Jogadores são levados à arena 60 segundos antes do início oficial.
* **Sistema de Borda (WorldBorder):** Borda dinâmica que diminui progressivamente. 
    * *Configuráveis:* Tamanho inicial/final, tempo de fechamento e atraso (delay).
* **Eliminação:** Detecção precisa de mortes com avisos globais no chat (Vítima vs. Assassino).
* **Vencedor:** O último sobrevivente é anunciado globalmente e recebe o bônus de vitória em suas estatísticas.

---

## 🎒 Gerenciamento de Kits

Sistema flexível para facilitar a troca de modalidades (Ex: Kit PvP, Full Iron, Pots, etc):

* **Criação Dinâmica:** Administradores criam kits salvando o inventário atual com `/bullet setkit`.
* **Seleção Visual:** Escolha do kit via GUI antes de confirmar o agendamento.
* **Aplicação Automática:** Limpeza de inventário e aplicação do kit instantânea ao entrar na arena.

---

## 🕒 Agendamento e Persistência

* **Agendamento por GUI:** Menu intuitivo para seleção de data, hora e minuto.
* **Sessões de Jogador:** Sistema de créditos que permite que players iniciem eventos.
* **Intervalo de Segurança:** Trava nativa de **1 hora** entre eventos para evitar sobreposição.
* **Banco de Dados:** Suporte a **SQL** para armazenamento persistente de vitórias, abates e sessões.

---

## 🛠️ Comandos e Administração

### Comandos Administrativos
| Comando | Descrição |
| :--- | :--- |
| `/bullet adminstart` | Abre o menu de início imediato ou agendado. |
| `/bullet disband` | Encerra o evento atual à força e limpa tarefas. |
| `/bullet setspawn` | Define o local de combate na arena. |
| `/bullet setlobby` | Define o local de saída/lobby do evento. |
| `/bullet reload` | Recarrega as configurações e traduções (`pt_BR.yml`). |
| `/bullet darsessao <player>` | Adiciona créditos de sessão a um jogador. |

### Comandos de Jogador
| Comando | Descrição |
| :--- | :--- |
| `/bullet join` | Entra em um evento ativo. |
| `/bullet leave` | Sai do evento antes do início ou durante a morte. |
| `/bullet playerstart` | Inicia/Agenda um evento (consome 1 sessão). |

## 🧩 Integração com PlaceholderAPI

O **Bullet** oferece suporte total ao PlaceholderAPI, permitindo que você exiba estatísticas e informações do evento em qualquer lugar do seu servidor.

### 🏆 Estatísticas Globais
*Dados persistentes armazenados no banco de dados (H2/MySQL).*

| Placeholder | Descrição |
| :--- | :--- |
| `%bullet_wins%` | Retorna a quantidade total de **vitórias** do jogador. |
| `%bullet_total_kills%` | Retorna a quantidade total de **abates** acumulados. |
| `%bullet_sessions%` | Retorna o saldo de **sessões (créditos)** do jogador. |

### ⚔️ Partida em Andamento
*Informações dinâmicas sobre o evento atual.*

| Placeholder | Descrição |
| :--- | :--- |
| `%bullet_kills_bullet%` | Quantidade de abates do jogador na **partida atual**. |
| `%bullet_border_status%` | Exibe o status dinâmico da borda (veja os estados abaixo). |

#### 📡 Estados do `%bullet_border_status%`
Este placeholder adapta a mensagem automaticamente de acordo com a fase do jogo:
* **Sem evento:** Exibe uma mensagem de "Sem jogo".
* **Aguardando:** `"A Borda irá diminuir em Xm Xs"`
* **Em movimento:** `"Diminuindo..."`
* **Finalizado:** `"A Borda está em X blocos."`

---
---

## ⚙️ Detalhes Técnicos e Performance

* **Localização Completa:** 100% das mensagens e menus são traduzíveis via `pt_BR.yml`.
* **Anti-Flood de Tasks:** Sistema robusto de gerenciamento de tarefas (BukkitRunnables) que evita execuções duplicadas ou mensagens repetidas.
* **Operações Assíncronas:** Acesso ao banco de dados e envio de Webhooks realizados fora da thread principal para evitar lag no servidor.
* **Webhooks:** Integração com Discord para log de agendamentos e início de partidas.
