# Resultados simulados — Teste de Usabilidade Moderado
### Rodado no protótipo `../usability-test/prototype/index.html`

> ⚠️ **Simulado**, não é coleta real — escopo do portfólio é de dados secundários, sem recrutamento (protocolo, seção 2). As métricas abaixo foram construídas para refletir, de forma plausível, o comportamento real do protótipo tal como ele foi implementado — incluindo uma fricção genuína que existe no código (não um problema inventado): ao clicar em "editar perfil antes de continuar" durante a candidatura, o fluxo não retorna automaticamente ao passo 1, forçando o participante a navegar de volta manualmente. Isso está registrado como achado real de usabilidade abaixo.

## Amostra simulada
5 participantes por grupo (protocolo, seção 2) — Grupo A (Millennial) e Grupo B ("Geração Alpha"/adolescente candidato a jovem aprendiz).

## Resultados por tarefa

| Tarefa | Grupo A — Success Rate | Grupo A — Tempo médio | Grupo A — Erros médios | Grupo B — Success Rate | Grupo B — Tempo médio | Grupo B — Erros médios |
|---|---|---|---|---|---|---|
| T1 — Encontrar vaga remota em área X | 5/5 (100%) | 18s | 0,2 | 5/5 (100%) | 22s | 0,4 |
| T2 — Filtrar por CLT | 5/5 (100%) | 9s | 0 | 5/5 (100%) | 11s | 0,2 |
| T3 — Ver salário e benefícios | 5/5 (100%) | 7s | 0 | 5/5 (100%) | 8s | 0 |
| T4 — Candidatar-se (fluxo de 3 passos) | 5/5 (100%) | 71s | 0,8 | 4/5 (80%) | 96s | 1,6 |
| T5 — Editar perfil | 5/5 (100%) | 24s | 0,2 | 5/5 (100%) | 19s | 0 |
| T6 — Achar vaga p/ quem nunca trabalhou (só Grupo B) | — | — | — | 5/5 (100%) | **4s** | 0 |

## Achados

**Achado 1 — T6 validou a decisão de design mais importante do wireframe.**
Todos os 5 participantes do Grupo B encontraram a categoria "Jovem Aprendiz" quase instantaneamente (~4 segundos, 0 erros), porque o chip está visível diretamente na Home, sem precisar abrir nenhum menu. Essa era exatamente a decisão de design marcada como crítica na especificação de wireframes — a simulação sugere que ela funciona.

**Achado 2 — a T4 é o ponto de maior fricção do protótipo, e por um motivo real e específico.**
1 participante do Grupo B abandonou a tarefa (pediu para desistir, conforme regra do protocolo de só intervir mediante pedido explícito) depois de clicar em "editar perfil antes de continuar" a partir do passo 1 da candidatura, e não conseguir encontrar o caminho de volta — o protótipo leva para a tela de Perfil, mas não guarda o "de onde vim" para retornar automaticamente. Isso é uma fricção real do fluxo implementado, não uma suposição. Recomendação de redesenho: o botão "editar perfil" durante a candidatura deveria abrir a edição como um modal/etapa inline, sem sair do fluxo de candidatura.

**Achado 3 — Grupo B teve tempo maior e mais erros em quase todas as tarefas, mas a diferença é pequena, exceto na T4.**
Isso é coerente com a expectativa: usuários menos experientes em plataformas de vagas (Théo nunca usou uma) navegam um pouco mais devagar, mas a diferença só se torna grande exatamente na tarefa mais complexa (T4) — sugerindo que o design geral do protótipo é acessível para um primeiro uso, e o problema está concentrado em um ponto específico e corrigível, não espalhado pelo produto inteiro.
