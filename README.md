# 🎳 Tutorial Completo - Plugin Bullet
Este é o guia definitivo para configurar e utilizar todas as funções do seu plugin de evento **Bullet**.
---
## 🛠️ 1. Configuração Inicial
Antes de começar, você precisa configurar os locais básicos e validar sua licença.
1.  **Chave de Licença:** No arquivo [config.yml](file:///c:/Users/repetecas/IdeaProjects/bulletpika%20-%20Com%20licensa/src/main/resources/config.yml), coloque sua chave em `license-key`.
2.  **Lobby:** Vá até o local onde os jogadores devem ir após o evento e use:
    *   `/bullet setlobby`
3.  **Spawn da Arena:** Vá até o centro do mapa onde o evento ocorrerá e use:
    *   `/bullet setspawn`
---
## 📦 2. Gerenciamento de Kits
Kits são os itens que os jogadores receberão automaticamente ao entrar no evento.
1.  **Criar um Kit:**
    *   Equipe os itens e a armadura exatamente como deseja no seu inventário.
    *   Use: `/bullet setkit <nome> <ícone_material>`
    *   *Exemplo:* `/bullet setkit Gladiador DIAMOND_SWORD`
---
## 🏗️ 3. Sistema de Arena (Restauração de Blocos)
O plugin possui um sistema de restauração automática para que as construções dos jogadores sejam limpas após o fim do evento.
1.  **Definir a Área:**
    *   Vá até um canto da arena e use: `/bullet pos1`
    *   Vá até o canto oposto e use: `/bullet pos2`
2.  **Salvar a Arena:**
    *   Use: `/bullet setararena <nome>`
3.  **Deletar uma Arena:**
    *   Use: `/bullet deletearena <nome>`
> [!TIP]
> O plugin restaurará automaticamente todos os blocos dentro desse cubo quando o jogo terminar!
---
## 🎮 4. Iniciando e Participando
Existem duas formas de iniciar um evento:
### Como Admin (Início Imediato)
1.  Use `/bullet adminstart`.
2.  Um menu abrirá para você escolher o kit.
3.  O evento começará instantaneamente.
### Como Jogador (Início Agendado)
O jogador precisa de "sessões" para iniciar um evento.
1.  **Dar Sessão a um Jogador:** `/bullet darsessao <player>`
2.  **Agendar Jogo:** O jogador usa `/bullet playerstart`.
3.  Um menu abrirá permitindo escolher:
    *   **Kit:** Qual kit será usado.
    *   **Data e Hora:** Quando o jogo começará.
    *   **Comando de Prêmio:** (Apenas Admin) Qual comando será executado para o vencedor.
---
## 🏆 5. Holograma de Sessões (Leaderboard)
Se você tiver o plugin **DecentHolograms** instalado, pode exibir as próximas sessões agendadas.
1.  **Criar/Atualizar Holograma:**
    *   Vá até o local desejado e use: `/bullet sessoes`
2.  O holograma mostrará as próximas 10 sessões agendadas automaticamente.
---
## 📊 6. Outros Comandos e Funções
*   **`/bullet info`:** Veja suas estatísticas de Kills e Vitórias.
*   **`/bullet join`:** Entra em um evento que está na fase de espera.
*   **`/bullet leave`:** Sai de um evento ativo.
*   **`/bullet disband`:** Finaliza forçadamente um evento em andamento.
*   **`/bullet border <tamanho> <tempo>`:** Ajusta manualmente a barreira do mundo.
*   **`/bullet reload`:** Recarrega as configurações e traduções.
---
## ⚙️ Destaques da Configuração (`config.yml`)
*   **`reset_arena_command`:** Comando executado no console quando o jogo acaba (ex: limpar lag).
*   **`border`:** Configure o tamanho inicial, final, tempo de fechamento e atraso.
*   **`spectator.block_teleport`:** Impede que espectadores se teleportem e atrapalhem o jogo.
*   **`webhook`:** Envie anúncios automáticos para o seu Discord quando um jogo começar ou for agendado.
---
> [!NOTE]
> Suporte técnico: Este plugin foi desenvolvido para ser performático e fácil de usar. Se precisar de ajustes nas cores, verifique o `pt_BR.yml`.バランスバランス
