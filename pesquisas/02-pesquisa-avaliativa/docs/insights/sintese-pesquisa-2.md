# Síntese — Pesquisa 2 (Avaliativa)

> ⚠️ Síntese de achados simulados (`../usability-test/resultados-simulados.md` e `../tree-test/resultados-tree-test.md`), coerente com o protótipo real implementado.

## Ranking de problemas encontrados (por severidade)

| # | Problema | Severidade | Método que revelou | Recomendação |
|---|---|---|---|---|
| 1 | Fluxo de candidatura perde o participante ao sair para editar perfil | Alta (gerou abandono real na simulação) | Teste de Usabilidade (T4) | Editar perfil como etapa inline, sem sair do fluxo de candidatura |
| 2 | "Jovem Aprendiz" e "Estagiário/Aprendiz" competem semanticamente na árvore de IA | Média-alta (mascarada pelo protótipo visual, exposta pelo Tree Testing) | Tree Testing (TT3) | Renomear nó de senioridade para "Nível inicial" |
| 3 | Tarefas que exigem combinar duas facetas (área + modalidade) têm baixo sucesso na árvore em texto puro | Baixa como problema de produto / alta como limitação metodológica | Tree Testing (TT1) | Documentar como decisão consciente de design de filtros paralelos; ajustar desenho de testes futuros |

## Como isso valida (ou não) as hipóteses geracionais do portfólio
Diferente da Pesquisa 1, onde a diferença geracional era o próprio objeto de estudo, aqui o achado mais importante é o oposto: **os dois problemas mais sérios (achados 1 e 2) afetam os dois grupos de forma parecida** — não são um problema "de adolescente" ou "de Millennial", são problemas de arquitetura/fluxo que atingem qualquer usuário novo no produto. Isso é, em si, um resultado válido e maduro para constar no portfólio: nem toda pesquisa precisa confirmar diferença entre públicos para ser útil — às vezes o valor está em mostrar que um problema é universal, e portanto deve ser priorizado independentemente de segmento.

## Conexão com a Pesquisa 3
O achado 1 (perda de contexto ao sair do fluxo principal) tem o mesmo formato do problema de maior severidade encontrado na análise de avaliações do iFood (Pesquisa 3): friction em fluxos que interrompem a tarefa principal do usuário (candidatura / pedido) sem um caminho claro de retorno. Isso sugere um padrão transversal ao portfólio inteiro, que pode virar um argumento de fechamento no case final: **produtos que interrompem o fluxo principal do usuário sem preservar contexto de retorno geram abandono, independentemente do domínio (emprego ou delivery) ou da geração do usuário.**
