# SUS Simulado — iFood
### Painel fictício de 6 respondentes, calibrado com os achados reais de `avaliacoes-codificadas.md`

> ⚠️ **Simulado**, não é coleta real — o escopo deste portfólio é de dados secundários, sem recrutamento (ver protocolo, seção 3.3). As respostas abaixo foram construídas para refletir, de forma plausível e internamente coerente, os padrões de reclamação real encontrados na etapa anterior: os itens do SUS relacionados a **confiança** e **inconsistência** foram calibrados para pontuar pior, porque é exatamente isso que os dados reais mostraram (estorno, preços diferentes por conta, dificuldade de cadastro) — a usabilidade "básica" do app (fácil de usar, rápido de aprender) foi calibrada para pontuar bem, coerente com a nota real de 4,7/5 no Google Play.

## Composição do painel
- **R1, R2, R3** — perfil Millennial (ancorado na Camila): usuário experiente do app, já usa há anos.
- **R4, R5, R6** — perfil "Geração Alpha"/jovem (ancorado no Théo): usuário recente/pouco experiente, poucos meses de uso.

## Respostas simuladas (escala 1-5: 1 = discordo totalmente, 5 = concordo totalmente)

| Item | R1 | R2 | R3 | R4 | R5 | R6 | Média |
|---|---|---|---|---|---|---|---|
| 1. Gostaria de usar com frequência | 5 | 4 | 5 | 5 | 4 | 5 | 4,67 |
| 2. Desnecessariamente complexo | 2 | 2 | 1 | 3 | 2 | 2 | 2,00 |
| 3. Fácil de usar | 5 | 4 | 5 | 4 | 4 | 5 | 4,50 |
| 4. Precisaria de apoio técnico | 1 | 2 | 1 | 3 | 2 | 1 | 1,67 |
| 5. Funções bem integradas | 4 | 3 | 4 | 3 | 3 | 4 | 3,50 |
| 6. Muita inconsistência | 3 | 4 | 2 | 3 | 2 | 2 | 2,67 |
| 7. Maioria aprenderia rápido | 5 | 4 | 5 | 4 | 4 | 5 | 4,50 |
| 8. Muito complicado | 1 | 2 | 1 | 2 | 2 | 1 | 1,50 |
| 9. Me senti confiante usando | 3 | 3 | 4 | 2 | 3 | 3 | **3,00** |
| 10. Precisei aprender muitas coisas novas | 2 | 2 | 1 | 3 | 2 | 1 | 1,83 |

## Cálculo do score SUS (fórmula oficial — ver protocolo, seção 3.2)

| Respondente | Soma (itens ímpares −1) | Soma (5 − itens pares) | Total (0-40) | Score SUS (×2,5) |
|---|---|---|---|---|
| R1 (Millennial) | 17 | 16 | 33 | 82,5 |
| R2 (Millennial) | 13 | 13 | 26 | 65,0 |
| R3 (Millennial) | 18 | 19 | 37 | 92,5 |
| R4 (Alpha) | 13 | 11 | 24 | 60,0 |
| R5 (Alpha) | 13 | 15 | 28 | 70,0 |
| R6 (Alpha) | 17 | 18 | 35 | 87,5 |

**Score SUS médio — Millennials**: (82,5 + 65,0 + 92,5) / 3 = **80,0**
**Score SUS médio — Geração Alpha/jovem**: (60,0 + 70,0 + 87,5) / 3 = **72,5**
**Score SUS médio geral**: (80,0 + 72,5) / 2 = **76,25**

## Interpretação
O benchmark de mercado mais citado para o SUS (Bangor, Kortum & Miller, 2008) é uma média de ~68 pontos — nosso score simulado geral (76,25) fica **acima** dessa referência nos dois grupos, mesmo com os problemas reais documentados na análise de avaliações. Existe também uma escala adjetiva associada a faixas de score SUS, mas não vou citar os cortes exatos de memória sem verificar a fonte original — se for usar isso no relatório final, vale confirmar os números antes de publicar.

**O achado mais interessante desta simulação, e coerente com os dados reais**: o item 9 ("me senti confiante usando o app") teve a **pior média entre os itens positivos (3,0)**, destoando de itens como "fácil de usar" (4,5) e "aprenderia rápido" (4,5). Isso é internamente consistente com o achado real da Pesquisa 3 — o problema do iFood não é a usabilidade básica de pedir comida (isso funciona bem, e a nota real de 4,7/5 na Play Store reflete isso), é a **confiança** na parte financeira/transparência (estorno, preços diferentes por conta). Essa é uma demonstração de um ponto metodológico importante: **SUS mede usabilidade percebida da interface, não necessariamente confiabilidade ou transparência do serviço** — os dois podem divergir, como divergiram aqui.

Diferença entre grupos: Alpha/jovem pontuou ~7,5 pontos abaixo de Millennial, principalmente pelos itens 4 e 10 (necessidade de apoio/aprendizado) — coerente com a hipótese de que usuários novos levam mais tempo para se sentir fluentes no produto, mesmo em um app popular e geralmente bem avaliado.
