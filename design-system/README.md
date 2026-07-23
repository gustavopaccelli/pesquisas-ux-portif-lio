# Design System do Portfólio

> Base: [`DESIGN-clay-source.md`](DESIGN-clay-source.md), o design system que você anexou (originalmente uma análise do site da Clay.com). Os **tokens** (cores, tipografia, espaçamento, raio de borda, elevação) foram implementados fielmente em [`tokens.css`](tokens.css). O que mudou aqui é a **aplicação**: a fonte original descreve páginas de um SaaS de dados B2B (hero "Go to market with unique data", pricing tiers, página /experts, ilustrações de claymation) — nada disso se aplica a um portfólio de UX Research, então este documento traduz o vocabulário de componentes do Clay para as páginas que o nosso site realmente precisa.

## O que foi preservado exatamente como está na fonte
- Paleta de cores completa (base, superfícies, 7 cores de marca, semânticas).
- Escala tipográfica completa (display-xl a nav-link), com a mesma hierarquia de tamanho/peso/letter-spacing.
- Escala de espaçamento (base 4px) e de raio de borda.
- Princípio de elevação: sem sombras pesadas, profundidade vem do contraste entre canvas creme e cards saturados.
- Regra de tipografia: peso 500 no display, nunca mais bold — "reads as bombastic" conforme a fonte.

## O que foi adaptado

### Substituição de fonte (já prevista na própria fonte)
Plain Black não é uma fonte web pública. Seguindo a nota "Known Gaps" do documento original, uso **Inter 500 com letter-spacing negativo** como substituto nos tamanhos display — já implementado em `tokens.css`.

### Sem ilustrações de claymation
As montanhas/mascotes 3D são ativos comissionados específicos da marca Clay, fora do escopo deste portfólio. **O substituto de "brand voltage"** aqui são os próprios artefatos de pesquisa — prints/telas do protótipo VagaCerta, tabelas de dados reais, trechos dos journey maps — usados dentro dos cards saturados no lugar de ilustração 3D. Ou seja: onde o Clay mostra fragmento de UI do produto dele dentro do card colorido, nós mostramos fragmento real da nossa própria pesquisa.

### Mapeamento de cores de marca → pesquisas do portfólio
A fonte original diz para escolher a cor de card certa para cada feature, não usar arbitrariamente. Mapeamento proposto:

| Cor | Pesquisa | Por quê |
|---|---|---|
| `--color-brand-pink` | Pesquisa 1 — Generativa (redes sociais) | Cor mais "social"/expressiva do conjunto, coerente com o tema |
| `--color-brand-teal` | Pesquisa 2 — Avaliativa (VagaCerta) | Teal é a cor "featured" na fonte original (usada no pricing-tier-featured) — faz sentido para o projeto mais robusto metodologicamente (dois métodos) |
| `--color-brand-ochre` | Pesquisa 3 — Quantitativa (iFood) | Ochre remete a dado/relatório mais "sério"/executivo, coerente com o tom técnico deste projeto |
| `--color-brand-lavender` / `--color-brand-peach` | Reservadas | Para uso futuro (ex: uma quarta seção, ou destaque de citação/insight dentro de uma página de case) |

### Páginas do portfólio (substituindo o mapa de páginas do Clay)

| Página do Clay (fonte original) | Equivalente no nosso portfólio |
|---|---|
| Homepage (hero + feature cards + pricing) | **Home do portfólio**: hero com nome/proposta + 3 `feature-card` (um por pesquisa, cores da tabela acima) + seção "sobre a metodologia" |
| Product pages | **Página de case** (uma por pesquisa): hero-band com título do projeto, `product-mockup-card` mostrando prints do protótipo/dados reais, blocos de achados usando `card-cream` |
| /experts | **Não se aplica** — não usar |
| Pricing | **Não se aplica** — não usar |
| CTA band pré-footer | Mantido: `cta-band-illustrated` (sem ilustração 3D) linkando para o repositório no GitHub / contato |
| Footer | Mantido como especificado: **footer creme, não escuro** — é uma regra explícita do sistema original ("Don't use a dark footer") |

### Regras que continuam valendo sem alteração
- Canvas sempre creme (`--color-canvas`), nunca cinza frio.
- Nunca repetir a mesma cor de card saturado duas vezes seguidas.
- Botão primário sempre `--color-primary` (quase preto), nunca colorido.
- Raio generoso: 12px em botões/inputs, 16px em cards de conteúdo, 24px em cards saturados.
- Sem hover states elaborados além do que já está no sistema.

## Como isso se relaciona com o protótipo VagaCerta
O protótipo clicável em `pesquisas/02-pesquisa-avaliativa/docs/usability-test/prototype/index.html` **tem sua própria identidade visual** (navy + tangerina + teal, motivo de "encaixe"), diferente deste design system. Isso é intencional e deve continuar assim: o VagaCerta é um produto fictício sendo testado *dentro* de uma pesquisa, não é a marca do portfólio em si — da mesma forma que um app de banco testado em uma pesquisa de usabilidade não precisa ter a cara da consultoria que fez a pesquisa. O design system deste documento é exclusivamente para a camada de apresentação do portfólio (`src/`), que vai *falar sobre* os três projetos, incluindo o VagaCerta, sem se disfarçar de nenhum deles.

## Próximo passo
Este documento e o `tokens.css` são a base pronta para a Home e as páginas de case do portfólio. A construção das páginas em si (HTML/CSS usando esses tokens) ainda não foi feita — é a próxima etapa, quando você quiser seguir para lá (por aqui no chat, ou já delegando ao Claude Code).
