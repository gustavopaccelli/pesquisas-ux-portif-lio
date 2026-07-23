# Protocolo de Pesquisa Avaliativa
## Teste de Usabilidade Moderado + Tree Testing — Plataforma de Vagas de Emprego

> Documento de trabalho para o Projeto 2 do portfólio de UX Research.
> Tema mapeado na varredura do repositório `public-apis/public-apis`: categoria **Jobs**.
> Métodos: Teste de Usabilidade Moderado + Tree Testing.

---

## 1. Contexto e objetivo de pesquisa

**Por que este projeto vem depois do Projeto 1**: o IS5 da Pesquisa Generativa mostrou que a jornada de decisão difere estruturalmente entre gerações — o que reforça a necessidade de **validar hipóteses de design com usuários reais**, em vez de assumir que uma única arquitetura de informação serve igualmente bem a públicos diferentes. Este projeto testa exatamente isso, mas em outro domínio (emprego, não redes sociais), para não repetir o mesmo tema.

**Pergunta de pesquisa central**: um usuário consegue, de forma eficiente e sem erros, (a) executar tarefas-chave de busca e candidatura em uma plataforma de vagas, e (b) localizar categorias de vagas em uma arquitetura de informação baseada só em texto (sem visual/design)?

**Produto avaliado** (fictício, construído para este portfólio — não é um produto real de mercado):
- **Nome de trabalho**: "VagaCerta" (a definir/ajustar).
- **Escopo**: protótipo de média fidelidade (clicável, não funcional de verdade) de uma plataforma de busca de vagas, com filtros por área, senioridade, tipo de contrato (CLT, PJ, estágio, jovem aprendiz, freelance) e modalidade (remoto, híbrido, presencial).
- **Ferramenta de prototipagem**: ~~Figma~~ **decisão revisada**: o protótipo foi construído diretamente como HTML/CSS/JS clicável e funcional, em vez de Figma — arquivo único, autocontido, em [`prototype/index.html`](prototype/index.html). Motivo da troca: elimina dependência de link externo que pode expirar/perder acesso, e já nasce dentro do repositório versionado. É um protótipo de média fidelidade de verdade (não apenas telas estáticas) — filtros funcionam, fluxo de candidatura em 3 passos navega de fato, estado vazio aparece quando um filtro não retorna resultado.

---

## 2. Recorte e recrutamento

Para manter a continuidade narrativa do portfólio, a proposta é reaproveitar os dois perfis geracionais já estabelecidos no Projeto 1 — mas adaptados ao contexto de busca de emprego, não de redes sociais. Personas específicas para este projeto serão desenhadas na próxima etapa (com dados reais do mercado de trabalho brasileiro, seguindo o mesmo padrão de rastreabilidade do Projeto 1).

| Grupo | Perfil de uso no contexto "vagas de emprego" | Critério de recrutamento |
|---|---|---|
| A — Millennial (~30-44 anos) | Profissional já empregado buscando transição/nova oportunidade | Já usou pelo menos uma plataforma de vagas (LinkedIn, Catho, Indeed, Gupy) nos últimos 12 meses |
| B — "Geração Alpha"/adolescente (~16-17 anos) | Buscando primeira vaga formal (jovem aprendiz — modalidade permitida a partir de 14 anos pela CLT; vaga formal regular a partir de 16) | Nunca teve emprego formal, mas já pesquisou ou tem interesse em buscar uma vaga de jovem aprendiz/estágio |

**Nota**: diferente do Projeto 1 (onde excluímos deliberadamente a mediação parental), aqui *pode* ser relevante perguntar, no roteiro pós-tarefa do Grupo B, se o adolescente busca vagas sozinho ou com apoio de um adulto — isso é uma pergunta de pesquisa sobre o **produto** (a plataforma ajuda ou não o usuário jovem a ser autônomo?), não sobre mediação de uso de rede social. É uma distinção importante para não reintroduzir escopo que você já decidiu deixar de fora.

Amostra sugerida: 5 participantes por grupo para o teste de usabilidade (número padrão de mercado — a partir de 5 usuários já se identifica a maioria dos problemas de usabilidade recorrentes) e 15-20 participantes por grupo para o tree testing (testes de árvore são quantitativos-leves e precisam de mais respondentes para gerar taxa de sucesso confiável, mesmo que a amostra ainda seja pequena/não representativa estatisticamente).

---

## 3. Teste de Usabilidade Moderado

### 3.1 Estrutura da sessão (30-40 min, individual, remoto ou presencial)

**Abertura (5 min)**
- Consentimento de gravação de tela.
- Explicar o protocolo de "pensar em voz alta" (think-aloud): pedir que o participante narre o que está pensando/procurando enquanto navega.
- Deixar claro: "não estamos testando você, estamos testando o produto — se você não conseguir fazer algo, é um problema do produto, não seu."

**Tarefas (20-25 min)**
Lista de tarefas a executar no protótipo, em ordem crescente de complexidade:

| # | Tarefa | Métrica capturada |
|---|---|---|
| T1 | "Encontre uma vaga de [área X] na modalidade remoto." | Task success (sim/não), tempo, nº de erros/cliques errados |
| T2 | "Filtre as vagas para mostrar apenas as de tipo CLT." | Task success, tempo, nº de erros |
| T3 | "Abra os detalhes de uma vaga e identifique o salário e os benefícios oferecidos." | Task success, tempo |
| T4 | "Candidate-se a uma vaga." | Task success, tempo, nº de erros, pontos de abandono |
| T5 | "Volte e edite alguma informação do seu perfil de candidato." | Task success, tempo |
| T6 (só Grupo B) | "Encontre vagas específicas para jovem aprendiz." | Task success — testa se a categoria é discoverable para quem não sabe exatamente o termo certo |

**Fechamento (5-10 min)**
- "Em geral, o que foi mais fácil e o que foi mais difícil aqui?"
- "Teve algum momento em que você não sabia o que fazer, ou esperava que algo funcionasse diferente?"
- "Numa escala de 0 a 10, quão confiante você ficaria em usar essa plataforma de verdade pra buscar emprego?"

### 3.2 Métricas a consolidar por participante e por grupo
- **Task Success Rate**: % de tarefas completadas sem ajuda do moderador.
- **Tempo médio por tarefa**.
- **Taxa de erro**: número de cliques/caminhos incorretos antes de completar (ou desistir de) cada tarefa.
- **Pontos de abandono**: em qual tarefa/etapa, se houver, o participante desistiu.

### 3.3 Roteiro de moderação — regras para não induzir respostas
- Nunca confirmar se um clique está "certo" ou "errado" durante a tarefa — só observar.
- Se o participante travar, esperar aproximadamente 30 segundos antes de perguntar "o que você está pensando agora?" — sem sugerir caminho.
- Só intervir ativamente (dar a resposta) se o participante pedir explicitamente para desistir da tarefa, para não gerar frustração excessiva na sessão.

---

## 4. Tree Testing

### 4.1 Objetivo específico
Avaliar se a arquitetura de informação (hierarquia de categorias) da plataforma é encontrável **usando apenas texto**, sem nenhum apoio visual — isolando o problema de "estrutura/nomenclatura" do problema de "design visual".

### 4.2 Estrutura da árvore a ser testada (rascunho inicial — refinar na próxima etapa)
```
Vagas
├── Área/Setor
│   ├── Tecnologia
│   ├── Administrativo
│   ├── Comercial/Vendas
│   ├── Saúde
│   ├── Educação
│   └── ...
├── Tipo de contrato
│   ├── CLT
│   ├── PJ
│   ├── Estágio
│   ├── Jovem Aprendiz
│   └── Freelance/Temporário
├── Modalidade
│   ├── Remoto
│   ├── Híbrido
│   └── Presencial
├── Senioridade
│   ├── Estagiário/Aprendiz
│   ├── Júnior
│   ├── Pleno
│   ├── Sênior
│   └── Liderança/Gestão
└── Benefícios e Salário
    ├── Faixa salarial
    └── Benefícios (VR, VT, plano de saúde etc.)
```

### 4.3 Tarefas de teste de árvore (exemplos — pedir ao participante "onde você procuraria...")
- "Onde você procuraria uma vaga de tecnologia no modelo remoto?"
- "Onde você procuraria para saber se uma vaga tem plano de saúde?"
- "Onde você procuraria vagas para quem nunca trabalhou antes?" (testa se "Jovem Aprendiz" é encontrável por quem não conhece o termo exato)
- "Onde você procuraria vagas de liderança?"

### 4.4 Métricas do Tree Testing
- **Success rate**: % de participantes que chegaram ao local correto da árvore.
- **Directness**: % que chegou direto, sem "voltar" ou explorar caminhos errados antes.
- **Tempo médio por tarefa**.
- Ferramenta sugerida (fora deste repositório, apenas para rodar o teste): Optimal Workshop (Treejack) é o padrão de mercado para isso — permite testar a árvore em texto puro remotamente. Alternativa gratuita/simplificada: simular manualmente em entrevista, pedindo para o participante "apontar" na árvore impressa/em texto onde ele iria.

---

## 5. Plano de análise
1. Consolidar Task Success Rate e tempo médio por tarefa, por grupo geracional — comparar se há diferença sistemática entre Millennial e Alpha/adolescente.
2. Para o Tree Testing, montar uma "pain point matrix": categoria x taxa de sucesso, identificando quais nós da árvore são mais confusos.
3. Cruzar os dois métodos: um problema encontrado no Teste de Usabilidade (ex: dificuldade em achar "Jovem Aprendiz") deve aparecer também como taxa de sucesso baixa no nó correspondente do Tree Testing — se não aparecer nos dois, investigar a causa da divergência antes de reportar como achado.
4. Saída esperada: lista priorizada de problemas de usabilidade (com severidade), uma árvore de IA revisada, e recomendações de redesenho — que alimentarão eventualmente o Projeto 3 como pano de fundo (ex: se os problemas encontrados aqui aparecem também nas avaliações públicas de apps reais do setor).

## 6. Limitações a declarar no relatório final
- O protótipo testado é fictício; problemas de usabilidade encontrados não podem ser generalizados para plataformas reais do mercado (Catho, Gupy, LinkedIn etc.), servem apenas como demonstração de método.
- Amostra pequena (5 por grupo no teste de usabilidade) é suficiente para identificar problemas qualitativos recorrentes, mas não para comparação estatística rigorosa entre gerações.
- Tree Testing com 15-20 respondentes por grupo ainda é uma amostra de conveniência, não probabilística.

---

## Próximos passos (a fazer nas próximas etapas da conversa)
1. Levantar dados secundários reais sobre mercado de trabalho brasileiro por geração (taxa de desemprego jovem, uso de plataformas de vagas, jovem aprendiz) para embasar as personas deste projeto.
2. Desenhar as personas específicas deste projeto (adaptação de Camila/Théo ou novas personas).
3. Definir a ferramenta/formato do protótipo clicável.
4. Simular os resultados do teste de usabilidade e do tree testing (mesma lógica de artefatos simulados e rastreáveis do Projeto 1).
