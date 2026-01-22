## ⌨️ Comandos e Permissões

O comando principal é `/bullet` (ou o alias `/bulletpika`). Todos os comandos possuem **Tab-Complete** para facilitar o uso.

### 👑 Comandos Administrativos
*Permissão: `bullet.admin`*

| Comando | Descrição |
| :--- | :--- |
| `/bullet adminstart` | Abre o seletor de kits para iniciar ou agendar uma partida administrativa. |
| `/bullet darsessao <player>` | Concede créditos de agendamento a um jogador específico. |
| `/bullet setkit <nome> <ícone>` | Salva o inventário atual como um kit (Ex: `/bullet setkit PvP DIAMOND_SWORD`). |
| `/bullet setspawn` | Define o ponto de nascimento (spawn) dentro da arena de combate. |
| `/bullet setlobby` | Define o local onde os jogadores aguardam o início da partida. |
| `/bullet border <dist> <tempo>` | Configura manualmente a distância e tempo de fechamento da borda. |
| `/bullet sessoes` | Cria ou move o holograma de sessões agendadas para sua posição. |
| `/bullet disband` | Encerra a partida em andamento imediatamente. |
| `/bullet reload` | Atualiza as configurações e arquivos de mensagens (`messages.yml`). |

### 👤 Comandos de Jogador
*Permissão: `bullet.player`*

| Comando | Descrição |
| :--- | :--- |
| `/bullet playerstart` | Abre o menu de agendamento (consome **1 sessão** do jogador). |
| `/bullet join` | Entra em uma partida que está no estado de "Aguardando". |
| `/bullet leave` | Sai da fila de espera ou da partida atual. |

> [!TIP]
> **Dica:** O sistema de ícones no `/bullet setkit` aceita qualquer Material válido do Spigot/Paper. Use o Tab-Complete para ver a lista disponível!

---

## 🛡️ Sistema de Licenciamento e Segurança

Para garantir a integridade do plugin, o **BulletPika** conta com:
* **Validação de Chave:** O plugin requer uma licença ativa via API externa para funcionar.
* **Feedback em Tempo Real:** Se a licença for inválida ou expirar, os jogadores e administradores serão notificados via **Action Bar** ao tentar executar qualquer comando.
* **Logs via Webhook:** Notificações instantâneas no Discord da Staff sobre o status de ativação do plugin.
