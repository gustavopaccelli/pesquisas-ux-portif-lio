# Análise de Avaliações — iFood
### Dados reais, coletados via busca em julho de 2026

> **Nota metodológica importante**: não tenho acesso direto a um scraper/API que extraia sistematicamente centenas de avaliações da Google Play Store ou Apple App Store — o levantamento abaixo é uma **amostra intencional (purposiva)** de ~12 reclamações documentadas, encontradas via busca (Reclame Aqui, Google Play, reportagens), mais 2 estatísticas oficiais agregadas da própria plataforma Reclame Aqui. Isso é suficiente para ilustrar o método de codificação e gerar um ranking direcional de problemas, mas **não é uma amostra estatisticamente representativa** do volume total de avaliações do app — essa limitação deve constar no relatório final. Se você quiser um levantamento exaustivo de verdade, o caminho seria abrir a Google Play Store/App Store manualmente e extrair um número maior de reviews, ou usar uma ferramenta de scraping dedicada.

## Métricas gerais do app (dados reais, verificados)
- **Google Play Store**: nota 4,7/5, ~13,4 milhões de avaliações, mais de 100 milhões de downloads (dado coletado diretamente da página do app em julho de 2026).
- **Reclame Aqui**: nota 7,1/10, 142.588 reclamações registradas no período de 01/01/2026 a 30/06/2026, 69% resolvidas, tempo médio de resposta de 3 dias e 17 horas.
- **Segundo o próprio Reclame Aqui** (resumo oficial da página da empresa, período 01/09/2025-28/02/2026): **a maioria das reclamações são sobre "Estorno do valor pago" e "Dificuldade de cadastro"** — este é o dado mais forte que temos, por vir agregado diretamente da plataforma, não de uma amostra nossa.
- **Reportagem do jornal A Tarde** (maio de 2025): iFood foi a empresa com mais reclamações do Brasil em um levantamento de 6 meses no Reclame Aqui, com 136.712 reclamações no período.

## Amostra codificada de reclamações documentadas

| # | Fonte | Resumo parafraseado (sem nome de usuário) | Categoria |
|---|---|---|---|
| 1 | Reclame Aqui (estatística oficial) | Estorno do valor pago é a categoria de reclamação mais comum, segundo a própria plataforma | Cobrança/taxa |
| 2 | Reclame Aqui (estatística oficial) | Dificuldade de cadastro é a segunda categoria mais comum, segundo a própria plataforma | Bugs/instabilidade do app |
| 3 | Google Play (review, jan/2026) | Entrega adiada duas vezes (20 min, depois mais 15 min); ao tentar cancelar, suporte parou de responder; compensação oferecida foi de apenas R$5 | Atraso na entrega + Suporte ao cliente |
| 4 | Google Play (review, abr/2026) | Impossível alterar e-mail, telefone ou endereço no cadastro; códigos de verificação não chegam por e-mail | Bugs/instabilidade do app |
| 5 | Google Play (review, abr/2026) | Sem suporte para número de telefone ou cartão internacional | Bugs/instabilidade do app |
| 6 | Reclame Aqui (reportagem A Tarde) | Cliente esperou entregador por mais de 15 minutos na calçada; pedido cancelado sem reembolso | Atraso na entrega + Cobrança/taxa |
| 7 | Reclame Aqui (reportagem A Tarde) | Pedido de mercado acima de R$400; maior parte dos itens não entregue; reembolso negado mesmo com nota fiscal e fotos como prova | Erro no pedido + Cobrança/taxa |
| 8 | Reclame Aqui (relato individual) | Prazo de entrega alterado três vezes; item final entregue estava incorreto | Atraso na entrega + Erro no pedido |
| 9 | Reclame Aqui (relato individual) | Erro de validação de acesso após desbloqueio de conta, sem atualização apesar de promessa de prazo | Bugs/instabilidade do app |
| 10 | Reclame Aqui (título de reclamação) | Demora excessiva na entrega combinada com impossibilidade de cancelar o pedido e ausência de suporte | Atraso na entrega + Suporte ao cliente |
| 11 | Google Play (review de outro usuário, citada em busca) | Entregador reportado por tentar cobrar valor extra do cliente alegando problema falso no pedido; suporte não tomou nenhuma ação | Problema com entregador + Suporte ao cliente |
| 12 | TechTudo (reportagem, fev/2026) | Usuários relatam, em posts virais e no Reclame Aqui, que o app mostra preços diferentes para o mesmo prato dependendo da conta — inclusive entre assinantes e não assinantes do clube de benefícios | Cobrança/taxa |

## Tabela de frequência por categoria (sobre os 12 casos documentados)

| Categoria | Ocorrências | % da amostra |
|---|---|---|
| Cobrança/taxa | 4 | 33% |
| Atraso na entrega | 5 | 42% |
| Bugs/instabilidade do app | 4 | 33% |
| Suporte ao cliente | 4 | 33% |
| Erro no pedido | 2 | 17% |
| Problema com entregador | 1 | 8% |

*(Alguns casos foram contados em mais de uma categoria, por combinarem múltiplos problemas na mesma reclamação — comportamento realista, já que reclamações reais raramente têm uma única causa.)*

## Ranking dos 3 problemas mais citados
1. **Atraso na entrega** (a categoria mais frequente na amostra, e frequentemente combinada com falta de suporte para resolver o problema)
2. **Cobrança/taxa** — inclui tanto reembolso negado quanto a controvérsia mais recente e específica de 2025-2026: **preços diferentes mostrados para o mesmo produto dependendo da conta do usuário**, o que é um achado particularmente interessante para o relatório final, por ser um problema de transparência de interface, não só de operação logística.
3. **Bugs/instabilidade do app e suporte ao cliente** (empatados) — cadastro/validação de conta, e um padrão recorrente de suporte que interrompe o atendimento ou oferece compensação desproporcional ao problema.

## Achado de destaque para o relatório final
A combinação do dado oficial do Reclame Aqui ("estorno" como categoria #1) com o achado da reportagem do TechTudo (preços diferentes por conta) sugere que **o principal ponto de dor do produto não é operacional (comida atrasada), mas de confiança na transparência financeira** — quanto o cliente paga, e se recebe de volta o que tem direito. Isso é um insight mais forte e mais acionável para um relatório de UX do que "app atrasa entrega", que é um problema mais genérico de qualquer serviço de delivery.
