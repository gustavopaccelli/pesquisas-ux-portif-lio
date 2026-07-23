# Portfólio de UX Research — Gustavo Paccelli

Três projetos de pesquisa, um para cada tipo de método em UX Research, construídos com dados reais de pesquisas de mercado e literatura acadêmica brasileira como base para cases simulados.

| # | Projeto | Tipo | Status |
|---|---|---|---|
| 1 | [Comportamento em Redes Sociais: Millennials vs. "Geração Alpha"](pesquisas/01-pesquisa-generativa/) | Pesquisa Generativa (Discovery) — Diary Study + Journey Mapping | 🟢 Pesquisa concluída — falta página no site |
| 2 | [Teste de Usabilidade + Tree Testing — Plataforma de Vagas "VagaCerta"](pesquisas/02-pesquisa-avaliativa/) | Pesquisa Avaliativa (Validação) | 🟢 Pesquisa concluída — falta página no site |
| 3 | [Análise de Avaliações + SUS — App de Delivery (iFood)](pesquisas/03-pesquisa-quantitativa/) | Pesquisa Quantitativa | 🟢 Pesquisa concluída — falta página no site |

## Estrutura do repositório

```
.
├── README.md                          # este arquivo
├── pesquisas/
│   ├── 01-pesquisa-generativa/        # protocolo, personas, dados secundários
│   ├── 02-pesquisa-avaliativa/        # placeholder
│   └── 03-pesquisa-quantitativa/      # placeholder
├── src/                                # SPA de apresentação do portfólio (a construir)
│   └── assets/
└── .github/workflows/deploy.yml        # deploy automático para GitHub Pages
```

**Lógica da separação `pesquisas/` vs. `src/`**: `pesquisas/` guarda o *trabalho de pesquisa em si* (protocolos, dados, personas, journey maps — o material que sustenta cada case) em Markdown, versionável e legível direto no GitHub. `src/` vai conter a SPA que *apresenta* esse trabalho como página pública — landing page do portfólio com um card por pesquisa, cada card levando a uma página-case daquele projeto.

## Metodologia geral
Cada pesquisa segue seu próprio protocolo, documentado dentro de sua respectiva pasta em `pesquisas/`. O ponto em comum entre as três: sempre que um dado de mercado ou acadêmico é citado, a fonte é registrada em um arquivo `data/fontes-secundarias.md` dentro da pasta do projeto, para rastreabilidade.

## Aviso metodológico
Este é um portfólio de estudo/demonstração. Personas, diários e journey maps usados nos cases são **composições fictícias e ilustrativas**, construídas a partir de padrões documentados em pesquisas reais e citadas — não são retratos de pessoas reais nem dados coletados em campo, exceto quando explicitamente indicado o contrário em algum projeto específico.
