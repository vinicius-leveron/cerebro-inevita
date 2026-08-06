---
tipo: catalogo
colecao: skills-disponiveis
curadoria: INEVITA
verificado: 2026-08-06
---
# Pacote INEVITA — 34 skills de fora

Skills públicas e gratuitas, de repositórios ativos, **curadas pela INEVITA e verificadas em 06/08/2026**.
Não são nossas, não são auditadas por nós, e não vêm instaladas: este é um **catálogo**, não um inventário.

**A regra que faz o pacote valer:** skill instalada é execução emprestada — ela sabe *como fazer*, não sabe *do teu negócio*.
Cada bloco abaixo declara o **arquivo de contexto** que precisa existir pra a skill sair do genérico.
Quem escreve esse arquivo a partir do teu cérebro é a **`/moldar`** — molde uma, veja o resultado, depois vá pra próxima.

> *"o ativo escasso é a empresa saber dar contexto para os modelos"* — [[dia1-cerebro-da-empresa-transcricao]] @ 00:05

## Como instalar (honesto)

O comando circula assim:

```
cp -r skills/<nome> ~/.claude/skills/      # global
cp -r skills/<nome> ./.claude/skills/      # só neste projeto
```

Ele pressupõe que **o repositório de origem já foi clonado** na tua máquina — o `cp` copia de uma pasta local,
não baixa nada. Então o caminho completo é: clonar o repositório da fonte → copiar a pasta da skill que interessa →
rodar `/moldar` pra ela ler o teu contexto. Copiar as 34 de uma vez é o erro clássico: instala catálogo, não capacidade.

---

## Bloco 0 · O vault (5)

`obsidian-cli` · `obsidian-markdown` · `obsidian-bases` · `json-canvas` · `defuddle`

**Fonte:** `kepano/obsidian-skills` — oficial; Kepano é CEO do Obsidian.
Ensinam o agente a ler e escrever no vault direto. É o bloco que fecha o circuito da aula: sem ele,
as outras 29 rodam contra uma pasta qualquer em vez de rodarem contra o teu cérebro.

- **Arquivo de contexto:** o próprio cofre, com a estrutura de pastas definida — ou seja, já existe aqui.
- **Alimenta de:** a estrutura que o `/comecar` montou.
- **Comece por aqui.** Este bloco é pré-requisito dos outros, não uma opção paralela.

## Bloco 1 · Design consistente (7)

`design` · `design-system` · `ui-styling` · `brand` · `taste-skill` · `frontend-design` · `theme-factory`

**Fontes:** `ui-ux-pro-max-skill` · `taste-skill` · `anthropics/skills`.

- **Arquivo de contexto:** `design/tokens.md` (paleta, escala tipográfica, espaçamento, raio) e
  `design/referencias.md` (3 que você aprova, 3 que rejeita — e por quê).
- **Alimenta de:** `meu-negocio/posicionamento.md`, `meu-negocio/entrega.md` (a régua de "bom").
- **O que carrega o bloco:** os 3 que você **rejeita**. Contra-exemplo molda mais que exemplo.

## Bloco 2 · Disciplina de código (10)

`brainstorming` · `writing-plans` · `executing-plans` · `systematic-debugging` · `test-driven-development` ·
`verification-before-completion` · `requesting-code-review` · `ponytail-review` · `code-review-and-quality` ·
`incremental-implementation`

**Fontes:** `obra/superpowers` · `DietrichGebert/ponytail` · `addyosmani/agent-skills`.
Atacam degradação em base grande, *code bloat* e o "pronto" declarado sem verificação.

- **Arquivo de contexto:** `eng/decisoes.md` (arquitetura e **o que já foi descartado**) e `eng/definition-of-done.md`.
- **Alimenta de:** `meu-negocio/decisoes/` — decisão descartada com o motivo é exatamente o que o cérebro já guarda.

## Bloco 3 · Segurança (2)

`security-best-practices` · `security-threat-model`

**Fonte:** `openai/skills`.

- **Arquivo de contexto:** `eng/stack.md` (linguagens, frameworks, versões) e
  `eng/dados-sensiveis.md` (o que guarda, onde ficam os segredos, quem acessa).
- **Cuidado:** `eng/dados-sensiveis.md` descreve **onde** o segredo mora — nunca o segredo. Valor real vai pra `privado/`.

## Bloco 4 · Token e contexto (3)

`caveman-compress` · `learn-codebase` · `mem-search`

**Fontes:** `caveman` · `claude-mem`.

- **Arquivo de contexto:** nenhum obrigatório — **e é justamente por isso que este bloco vale menos que os outros**.
  Skill sem encaixe de contexto é skill que não aprende com o teu negócio.

## Bloco 5 · Distribuição e dinheiro (5)

`product-marketing` · `offers` · `pricing` · `avatar-extraction` · `generic-language-killer`

**Fontes:** `coreyhaines31/marketingskills` · `realkimbarrett/advertising-skills`.
`product-marketing` gera `.agents/product-marketing.md`, lido por todas as outras do mesmo repositório —
um autor externo chegando na tese do cérebro sozinho: **uma fonte de contexto, várias execuções em cima**.

- **Arquivo de contexto:** `negocio/icp.md`, `negocio/oferta.md`, `marca/voz.md`.
- **Alimenta de:** `meu-negocio/icp.md`, `meu-negocio/oferta.md`, `meu-negocio/posicionamento.md` — já existem aqui.
  A `/moldar` projeta pro caminho que a skill procura; a verdade continua em `meu-negocio/`.
- **É o bloco mais rápido de provar valor** se a frente do `/prototipar` foi **venda**.

## Bloco 6 · Criar as próprias (2)

`skill-creator` · `writing-skills`

**Fontes:** `anthropics/skills` · `obra/superpowers`.
Transformam o membro em produtor de skill em vez de consumidor de catálogo — é o bloco que sustenta a renovação no ano 2.

- **Arquivo de contexto:** o cérebro inteiro. Uma skill boa nasce de um trabalho que você já repetiu três vezes,
  não de uma ideia — o `/reindex` é quem revela a terceira vez.

---

## Três avisos antes de usar

1. **`caveman-compress` precisa de teste seu.** Corta tokens instruindo o agente a falar em estilo telegráfico.
   Viralizou pela graça. Em tarefa de precisão, a compressão cobra qualidade — teste num caso real antes de adotar.
2. **`learn-codebase` e `mem-search` competem com o pitch do cérebro.** São memória automática de sessão.
   Alguém vai perguntar por que construir cofre se isso já existe. A resposta: **elas guardam o que o agente fez;
   o cérebro guarda o que você decidiu** — e só a segunda coisa sobrevive à troca de ferramenta.
3. **Quatro repositórios do pacote passaram de 90k estrelas tendo nascido em julho.** Pode ser viralização real ou
   inflação. **Nenhuma skill aqui foi auditada por ninguém** — incluindo por nós. Leia o `SKILL.md` antes de instalar,
   e não instale skill que escreve fora do escopo que você espera.

## O caminho curto

1. `/prototipar` — descobre a frente (decisão · venda · entrega) e o primeiro trabalho.
2. Escolha **uma** skill do bloco que serve àquela frente.
3. `/moldar` — escreve o arquivo de contexto dela a partir do teu cérebro e valida numa rodada real.
4. Rodou com a tua cara? Aí sim a próxima.

Skill sem contexto devolve a média da internet. A média é o que a IA já entrega de graça.
