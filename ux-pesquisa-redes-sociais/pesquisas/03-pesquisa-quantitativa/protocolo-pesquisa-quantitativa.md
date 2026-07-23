# Protocolo de Pesquisa Quantitativa e Análise de Dados
## Análise de Avaliações de Loja de Aplicativos + System Usability Scale (SUS)

> Documento de trabalho para o Projeto 3 do portfólio de UX Research.
> Tema mapeado na varredura do repositório `public-apis/public-apis`: categoria **Food & Drink**.
> Métodos: Análise de Avaliações de App Store + SUS.

---

## 1. Contexto e objetivo de pesquisa

**Diferença metodológica importante em relação aos Projetos 1 e 2**: este projeto é o único dos três que pode se ancorar em **dados reais publicamente disponíveis** (avaliações de app store são conteúdo público), em vez de ser inteiramente simulado. Isso muda o padrão de rigor esperado — aqui, "simulado" deve ficar restrito estritamente à etapa de SUS (que exige recrutamento de respondentes, fora do escopo definido para este portfólio), enquanto a análise de avaliações deve, na medida do possível, usar avaliações e reclamações reais e citáveis.

**Produto avaliado**: proponho **iFood**, por ser o aplicativo de delivery dominante no Brasil e se encaixar diretamente no exemplo já citado no briefing original do portfólio ("apps de banco ou delivery"). Alternativa caso você prefira: Rappi (segundo maior player). Vou seguir com iFood como padrão, mas isso é facilmente ajustável.

**Perguntas de pesquisa**:
1. Quais são os pontos de dor de usabilidade mais recorrentes relatados por usuários reais em avaliações negativas do app?
2. Como esses pontos de dor se comparariam, em uma medição padronizada (SUS), à percepção de usuários dos dois perfis geracionais já estabelecidos no portfólio (Millennial e "Geração Alpha"/jovem)?

---

## 2. Análise de Avaliações de Loja de Aplicativos

### 2.1 Fonte de dados
- Avaliações públicas do app na Google Play Store e/ou Apple App Store — texto e nota (1 a 5 estrelas).
- Fonte complementar: **Reclame Aqui**, plataforma brasileira de reclamações de consumidores, costuma ter reclamações mais detalhadas e categorizadas do que reviews de loja de app, e é citável como fonte pública.
- Fonte complementar: reportagens/matérias jornalísticas brasileiras que já tenham sintetizado padrões de reclamação sobre o app (uma forma de triangular sem precisar coletar centenas de reviews manualmente).

### 2.2 Método de coleta e amostragem
- Foco em avaliações de **1 e 2 estrelas** (avaliações negativas), conforme o escopo original do projeto — dezenas de avaliações, não uma amostra probabilística.
- Período de coleta: avaliações recentes (últimos 3-6 meses a partir de julho de 2026), para refletir a versão atual do app, não reclamações antigas já corrigidas.
- **Nota sobre citação**: ao reportar trechos de avaliações reais no relatório final, seguir boas práticas de citação — paráfrase do conteúdo, sem reproduzir textos extensos literalmente, e sem incluir nomes de usuário ou informação que identifique o autor da avaliação.

### 2.3 Codificação/categorização
Cada avaliação negativa deve ser classificada em pelo menos uma categoria de problema, usando um esquema fechado para permitir contagem (não é análise qualitativa aberta — aqui o objetivo é quantificar frequência):

| Categoria | Descrição |
|---|---|
| Atraso na entrega | Tempo de entrega muito maior que o estimado no app |
| Erro no pedido | Item errado, faltando, ou pedido cancelado sem aviso |
| Cobrança/taxa | Taxa de entrega considerada abusiva, cobrança duplicada, problema de reembolso |
| Suporte ao cliente | Dificuldade de contato, resposta automática sem solução, demora no atendimento |
| Bugs/instabilidade do app | Erro técnico, app trava, pagamento não processa |
| Problema com entregador | Comportamento do entregador, localização incorreta |
| Outro | Não se encaixa nas categorias acima |

### 2.4 Saída esperada
- Tabela de frequência: % de avaliações negativas por categoria.
- Ranking dos 3 problemas mais citados.
- Trechos ilustrativos parafraseados (não citações literais extensas) por categoria.

---

## 3. System Usability Scale (SUS)

### 3.1 O instrumento
SUS é um questionário padronizado de 10 itens, escala Likert de 5 pontos (1 = discordo totalmente, 5 = concordo totalmente), desenvolvido por John Brooke (1986) e amplamente usado como referência de mercado em UX Research. Itens (tradução padrão usada em pesquisa brasileira):

1. Eu acho que gostaria de usar este aplicativo com frequência.
2. Eu achei o aplicativo desnecessariamente complexo.
3. Eu achei o aplicativo fácil de usar.
4. Eu acho que precisaria de apoio técnico para conseguir usar este aplicativo.
5. Eu achei que as várias funções deste aplicativo estavam bem integradas.
6. Eu achei que havia muita inconsistência neste aplicativo.
7. Eu imagino que a maioria das pessoas aprenderia a usar este aplicativo rapidamente.
8. Eu achei o aplicativo muito complicado de usar.
9. Eu me senti muito confiante usando o aplicativo.
10. Eu precisei aprender muitas coisas novas antes de conseguir usar este aplicativo.

### 3.2 Cálculo da pontuação (padrão, não inventado — fórmula oficial do SUS)
- Para itens ímpares (1,3,5,7,9): pontuação = (resposta dada) − 1
- Para itens pares (2,4,6,8,10): pontuação = 5 − (resposta dada)
- Somar as 10 pontuações resultantes (variam de 0 a 4 cada) → total de 0 a 40
- Multiplicar por 2,5 → score final de 0 a 100
- Referência de mercado (Bangor, Kortum & Miller, 2008 — benchmark amplamente citado, não específico deste projeto): score médio de mercado ≈ 68; acima de 68 é considerado acima da média, abaixo é considerado abaixo da média.

### 3.3 Aplicação neste projeto
Como o escopo definido para este portfólio é de dados secundários (sem recrutamento real), a aplicação do SUS aqui será **simulada**: vamos gerar respostas simuladas para um pequeno painel fictício de respondentes (ancorados nas personas Camila e Théo já estabelecidas), calibradas para refletir, de forma plausível, os padrões de reclamação encontrados na etapa 2 (análise de avaliações reais). Isso deve ficar marcado claramente como simulação no relatório final — o valor do SUS aqui é demonstrar o método corretamente aplicado (fórmula, benchmark, interpretação), não apresentar um score real de mercado.

---

## 4. Plano de análise
1. Consolidar a tabela de frequência de categorias de reclamação (dado real).
2. Calcular o score SUS simulado, com quebra por perfil geracional (Millennial vs. Alpha/jovem), e comparar contra o benchmark de mercado (~68).
3. Cruzar os dois: categorias de reclamação mais frequentes devem se refletir nos itens do SUS com pior pontuação simulada (ex: se "bugs/instabilidade" for a categoria mais citada, o item 6 do SUS — "muita inconsistência" — deve ter pontuação simulada baixa, para manter coerência interna entre os dois métodos).
4. Saída esperada: relatório técnico de pontos de dor (ranking de problemas + score SUS) — o entregável mais "executivo" dos três projetos do portfólio, no formato que uma empresa real usaria para priorizar backlog de produto.

## 5. Limitações a declarar no relatório final
- Avaliações de app store têm viés de seleção conhecido (usuários insatisfeitos tendem a avaliar mais do que satisfeitos) — isso é uma limitação do método em si, não deste projeto especificamente, e deve ser mencionada.
- O SUS aplicado é **simulado**, não coletado de respondentes reais — não deve ser reportado como medição real de satisfação do iFood.
- Amostra de avaliações analisadas (dezenas) não é estatisticamente representativa do total de usuários do app.

---

## Próximos passos (a fazer nas próximas etapas da conversa)
1. Levantar avaliações/reclamações reais do iFood (ou app escolhido) via busca — Reclame Aqui, reportagens, reviews públicas.
2. Codificar essas avaliações nas categorias definidas acima e montar a tabela de frequência.
3. Simular o painel de respondentes SUS, calibrado com os achados reais da etapa 1.
4. Montar o relatório técnico final do projeto.
