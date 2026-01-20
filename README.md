# 🛡️ Bullet Plugin

O **Bullet** é um sistema avançado de eventos PvP automáticos e agendados, inspirado no conceito de partidas "bullet" (rápidas). Focado em combate intenso, o sistema apresenta uma arena dinâmica com bordas que encolhem, proporcionando uma experiência competitiva premium para servidores de Minecraft.

---

## 🚀 Funcionalidades Principais

### 📋 Sistema de Agendamento Profissional
* **GUI Intuitiva:** Interface completa para seleção de kits e horários diretamente no jogo.
* **Seletores de Tempo Precisos:** Ajuste de Data, Hora e Minuto com botões de navegação e ajuste cumulativo.
* **Validação Inteligente:** Sistema nativo que impede agendamentos em datas passadas e garante um intervalo mínimo de 1 hora entre eventos para evitar sobreposição.

### 💰 Economia de Sessões
* **Sessões como Moeda:** Jogadores utilizam "Sessões" (créditos) para iniciar seus próprios eventos.
* **Persistência de Dados:** Suporte robusto para banco de dados **H2** (local) e **MySQL** (remoto).
* **Estatísticas:** Rastreamento de Vitórias e Kills Totais por jogador.

### ⚔️ Game Loop e Combate
* **WorldBorder Dinâmico:** Borda configurável que encolhe gradualmente até o centro, forçando o confronto final.
* **Kits Automáticos:** Distribuição instantânea de equipamentos ao entrar na arena.
* **Proteção Pré-Jogo:** Imortalidade e restrição de movimento durante a contagem regressiva.
* **Modo Espectador:** Transição suave para espectador após a eliminação.

### 📢 Integração e Customização
* **Webhooks para Discord:** Notificações automáticas e customizáveis para eventos agendados e iniciados.
* **Suporte PlaceholderAPI:** Use `%bullet_sessions%` e `%bullet_total_kills%` em seus menus e scoreboards.

---

## 🛠️ Comandos, Permissões e Placeholders

| Comando | Descrição | Permissão |
| :--- | :--- | :--- |
| `/bullet adminstart` | Abre o menu de agendamento sem custo. | `bullet.admin` |
| `/bullet playerstart` | Inicia o evento consumindo 1 sessão. | `bullet.player` |
| `/bullet darsessao {player} {qtd}` | Adiciona sessões a um jogador. | `bullet.admin` |

| Placeholder | Descrição |
| :--- | :--- |
| `%bullet_wins%` | Exibe o total de vitórias globais do jogador (armazenado no banco de dados). |
| `%bullet_total_kills%` | Exibe o total de abates (kills) acumulados pelo jogador em todas as partidas. |
| `%bullet_sessions%` | Exibe a quantidade de sessões (créditos) que o jogador possui para agendar eventos. |
| `%bullet_kills_bullet%` | Exibe a quantidade de abates que o jogador fez **apenas no Bullet atual**. |
| `%bullet_border_status%` | Exibe o status da borda em tempo real: tempo para encolher ou tamanho atual. |

---

## ⚙️ Instalação

1. Certifique-se de ter o **PlaceholderAPI** instalado para melhor aproveitamento.
2. Arraste o arquivo `.jar` para a pasta `plugins` do seu servidor.
3. Reinicie o servidor para gerar os arquivos de configuração.
4. Configure sua conexão MySQL (opcional) e o Webhook do Discord no arquivo `config.yml`.

---

## 📊 Requisitos
* **Versão do Minecraft:** [Disponivel apenas para versões PURPUR LEAF E PAPER 1.21.8]
* **Dependências:** PlaceholderAPI (Opcional, mas recomendado).
* **Java:** [Java 21].

---
