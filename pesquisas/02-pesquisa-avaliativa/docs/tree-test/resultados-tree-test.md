# Resultados simulados — Tree Testing
### Árvore testada em formato texto puro (protocolo, seção 4.2), sem o apoio visual do protótipo

> ⚠️ **Simulado**, não é coleta real. Diferente do Teste de Usabilidade (que testa o produto visual completo), o Tree Testing avalia **apenas a estrutura de texto da árvore de IA**, sem nenhuma pista visual — é isso que torna os dois métodos complementares, e é isso que os resultados abaixo demonstram.

## Amostra simulada
16 respondentes por grupo (dentro da faixa de 15-20 sugerida no protocolo, seção 2) — resultados agregados por tarefa, não por respondente individual (formato padrão de relatório de tree testing).

## Resultados por tarefa

| Tarefa | Nó correto na árvore | Millennial — Success | Millennial — Directness | Alpha — Success | Alpha — Directness |
|---|---|---|---|---|---|
| TT1 — "Vaga de tecnologia remota" | Área/Setor > Tecnologia **e** Modalidade > Remoto (dois nós separados) | 56% | 44% | 50% | 38% |
| TT2 — "Vaga com plano de saúde" | Benefícios e Salário > Benefícios | 88% | 81% | 75% | 63% |
| TT3 — "Vaga pra quem nunca trabalhou antes" | Tipo de contrato > Jovem Aprendiz | 63% | 50% | 56% | 44% |
| TT4 — "Vaga de liderança" | Senioridade > Liderança/Gestão | 94% | 94% | 88% | 81% |

## Achados

**Achado 1 — o problema da TT1 não é de conteúdo, é estrutural: a árvore mistura facetas paralelas com uma navegação de caminho único.**
A árvore do protótipo tem 5 grupos de categoria paralelos (Área, Tipo de contrato, Modalidade, Senioridade, Benefícios) que, na interface visual, funcionam como filtros combináveis — mas o formato clássico de tree testing pede que o participante escolha **um único caminho** na hierarquia. Uma tarefa que depende de duas facetas ao mesmo tempo ("tecnologia" + "remoto") não tem uma resposta única na árvore, o que derruba a taxa de sucesso mesmo sem nenhum problema real de nomenclatura. **Isso é uma limitação metodológica a declarar no relatório**, não um defeito do produto — o tree testing tradicional pressupõe hierarquia estrita de caminho único, e nosso produto usa filtros paralelos combináveis (mais comum em plataformas reais de busca, mas mal servido pelo método clássico).

**Achado 2 — TT3 confirma uma ambiguidade real de nomenclatura que o teste de usabilidade não conseguiu enxergar.**
No teste de usabilidade (T6), 100% dos participantes do Grupo B encontraram "Jovem Aprendiz" quase instantaneamente — mas isso só aconteceu porque o chip estava **visível na tela**, sem exigir que o participante decidisse sozinho onde procurar. No Tree Testing, sem essa pista visual, o sucesso cai para 56-63%, porque a árvore tem dois nós que podem parecer certos para quem não conhece o termo técnico: **"Tipo de contrato > Jovem Aprendiz"** (correto) e **"Senioridade > Estagiário/Aprendiz"** (parece certo, mas é sobre nível de senioridade, não sobre modalidade de contrato). Esse é exatamente o tipo de achado que só o Tree Testing revela — o protótipo visual "esconde" o problema estrutural.

**Achado 3 — o Grupo Alpha teve desempenho ligeiramente pior que o Millennial em quase todas as tarefas, mas a diferença é pequena e consistente — não há uma tarefa onde a geração "erra sozinha".**
Isso sugere que os problemas encontrados (TT1 e TT3) são de **arquitetura de informação**, não de característica geracional — ambos os grupos tropeçam nos mesmos dois pontos, só que o grupo mais experiente (Millennial) tropeça um pouco menos. É um achado relevante para o portfólio: nem todo problema de UX é "diferença entre gerações" — às vezes é só um problema de design que afeta todo mundo de forma parecida.

## Recomendação de redesenho da árvore (a partir dos dois achados acima)
1. Renomear "Estagiário/Aprendiz" (dentro de Senioridade) para algo que não colida semanticamente com "Jovem Aprendiz" (dentro de Tipo de contrato) — sugestão: renomear o nó de senioridade para **"Nível inicial"**, reservando a palavra "Aprendiz" só para o tipo de contrato.
2. Se o produto real mantiver filtros paralelos (o que faz sentido para a interface visual), isso deve ficar documentado como decisão consciente — e testes futuros de árvore devem ser desenhados como **tarefas de faceta única** (uma pergunta por grupo de filtro), não tarefas que exigem combinar dois grupos ao mesmo tempo.
