# 🛡️ BulletPika — Sistema Avançado de Partidas Agendadas

O **BulletPika** é um sistema de elite para gerenciamento de eventos e partidas competitivas de ritmo acelerado. Inspirado no conceito de partidas "bullet" (rápidas), o plugin foca em automação total, oferecendo uma experiência premium com arenas dinâmicas, bordas que encolhem e um sistema de agendamento profissional.

---

## 🚀 Funcionalidades Principais

### 📅 Agendamento Inteligente
* **Interface GUI:** Menu intuitivo para seleção de kits, data e hora exata do evento.
* **Sessões como Moeda:** Jogadores podem usar "Sessões" (créditos) para agendar seus próprios eventos.
* **Intervalo de Segurança:** O plugin impede automaticamente agendamentos com menos de 1 hora de diferença para evitar sobreposições.

### 🎒 Gerenciamento de Kits (Persistência Base64)
* **Criação Dinâmica:** Salve seu inventário atual (itens e armaduras) como um kit usando `/bullet setkit`.
* **Aplicação Automática:** Limpeza de inventário e entrega de itens instantânea ao entrar na arena.
* **Armazenamento Seguro:** Dados salvos em Base64 no banco de dados para total fidelidade aos itens.

### 📊 Hologramas de Sessões
* **Integração DecentHolograms:** Exibe um ranking dinâmico com as **próximas 10 sessões agendadas** no servidor.
* **Atualização em Tempo Real:** Mantenha os jogadores informados sobre os próximos eventos sem comandos extras.

### ⚔️ Game Loop e Mecânicas
* **WorldBorder Dinâmica:** Borda que encolhe gradualmente até um ponto central, forçando o combate.
* **Fases do Jogo:** Estados claros de Espera, Contagem Regressiva, Em Jogo e Finalização.
* **Modo Espectador:** Transição suave para acompanhar o final da batalha após ser eliminado.

---

## 🧩 Integração com PlaceholderAPI

| Placeholder | Descrição |
| :--- | :--- |
| `%bullet_wins%` | Vitórias globais do jogador. |
| `%bullet_total_kills%` | Total de abates acumulados. |
| `%bullet_sessions%` | Saldo de créditos/sessões do jogador. |
| `%bullet_kills_bullet%` | Abates na partida atual. |
| `%bullet_border_status%` | Status da borda (Tempo para encolher ou tamanho atual). |

---

## 🛠️ Comandos e Permissões

### 👑 Administração (`bullet.admin`)
* `/bullet adminstart` — Abre o seletor de kits para agendar uma partida administrativa.
* `/bullet darsessao <player>` — Concede créditos de agendamento a um jogador.
* `/bullet setkit <nome> <ícone>` — Cria um kit com o seu inventário atual.
* `/bullet setspawn` / `/bullet setlobby` — Define os locais de jogo e saída.
* `/bullet sessoes` — Posiciona o holograma de agendamentos.
* `/bullet border <dist> <tempo>` — Configura a borda manualmente.
* `/bullet disband` — Encerra a partida atual à força.
* `/bullet reload` — Recarrega as configurações e mensagens.

### 👤 Jogador (`bullet.player`)
* `/bullet playerstart` — Agenda uma partida (consome 1 sessão).
* `/bullet join` / `/bullet leave` — Entrar ou sair de um evento ativo.

---

## ⚙️ Detalhes Técnicos
* **Versão Base:** Paper API 1.21.x
* **Banco de Dados:** Suporte a **SQLite/H2** (local) ou **MariaDB/MySQL** (alta performance) via HikariCP.
* **Customização:** 100% das mensagens e menus configuráveis via `messages.yml`.
* **Segurança:** Sistema de licenciamento via API externa com notificações de status na Action Bar e Webhook no Discord.

---

## 📡 Dependências
* [DecentHolograms](https://www.spigotmc.org/resources/decentholograms.96927/) (Obrigatório para hologramas)
* [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) (Recomendado)
