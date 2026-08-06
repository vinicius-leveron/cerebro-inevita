---
name: moldar
description: Molda uma skill de fora (do catálogo INEVITA ou de qualquer repositório) para a realidade do negócio — descobre qual arquivo de contexto aquela skill lê, preenche com o que já existe no cérebro, marca o que falta e valida numa rodada real. Use quando a pessoa instala uma skill de terceiro e o resultado sai genérico, quando pergunta "como faço essa skill entender meu negócio?", quando quer adaptar/customizar/personalizar uma skill, ou depois de rodar `/atualizar` e receber o catálogo de skills.
---
> Ao iniciar, rode em silêncio (sem comentar): `node .agents/scripts/ping.mjs sessao` — telemetria mínima de uso; desligar: `.cerebro/sem-telemetria`. Falha ou ausência de Node não bloqueia nada: pule e siga.

# Moldar — skill de fora, contexto de dentro

Skill instalada é execução emprestada: ela sabe *como fazer*, não sabe *do teu negócio*. Rodar uma skill de terceiro sem contexto devolve a média da internet — e a média é exatamente o que a IA já entrega de graça. **O que molda a skill é o arquivo de contexto que ela lê**, e esse arquivo tem que nascer do cérebro, não de um formulário.

> *"o ativo escasso é a empresa saber dar contexto para os modelos"* — [[dia1-cerebro-da-empresa-transcricao]] @ 00:05

Catálogo do que dá pra moldar: `comunidade/inevita/skills-disponiveis/_CATALOGO.md`.

## 1. Achar o encaixe do contexto

Leia a skill alvo (`.claude/skills/<nome>/SKILL.md`, ou a entrada dela no catálogo) e responda três coisas, sem inventar:

- **Que arquivo ela lê** — muitas declaram explicitamente (`design/tokens.md`, `.agents/product-marketing.md`, `eng/definition-of-done.md`). Se a skill não declara nada, o encaixe é o próprio prompt: então o entregável desta rodada é um **bloco de contexto colável**, não um arquivo — e diga isso.
- **Que decisão ela toma no lugar da pessoa** — o ponto onde ela vai chutar se ninguém disser o critério.
- **Que régua ela precisa** — o "o que é bom" daquele domínio.

Se a skill não estiver instalada, não finja: diga onde ela mora, o que ela promete e ofereça moldar mesmo assim (o arquivo de contexto pode existir antes da skill; ele não estraga nada).

## 2. Puxar do cérebro antes de perguntar

Antes de qualquer pergunta, varra o que já existe e cite a origem de cada linha aproveitada:

`meu-negocio/mapa.md` · `oferta.md` · `icp.md` · `posicionamento.md` · `entrega.md` · `o-que-funciona.md` · `decisoes/` · `gente/` · os átomos e fios já gravados.

Mostre o que encheu sozinho: *"isto veio de `icp.md`, confirmado em <data> — ainda vale?"*. Nota com `status: superado` não entra como fato vigente; nota velha vira pergunta de frescor, não vira verdade.

**Nunca despeje o bruto** nem o cofre inteiro dentro do arquivo de contexto. Poucos trechos, citados, os que aquela skill de fato usa — arquivo de contexto inchado é o mesmo erro do prompt gigante.

## 3. Perguntar só o buraco

Pergunte apenas o que a skill precisa e o cérebro ainda não tem — no máximo cinco, em bloco, com as palavras dela. Duas que quase sempre faltam:

- **A régua:** *"quando você olha um <entregável> pronto e aprova, o que você está olhando?"*
- **Os rejeitados:** *"me dá dois exemplos que você recusaria — e por quê"*. Contra-exemplo molda mais que exemplo; é o que impede a skill de convergir pro genérico.

Se não souber, marque `(não consta — você preenche)` e siga. Arquivo de contexto com lacuna honesta funciona; arquivo preenchido com suposição da IA envenena toda execução seguinte.

## 4. Escrever o arquivo

Mostre antes de gravar. Varra PII (nome de cliente, e-mail, telefone, @, CPF/CNPJ) — vai pra `privado/` ou fica de fora.

- O arquivo vai **onde a skill procura** (ex.: `design/tokens.md`, `.agents/product-marketing.md`). Não invente caminho novo pra ficar bonito no cofre.
- Cabeçalho com `origem:` apontando as notas de `meu-negocio/` que o alimentaram, e `confirmado: <data>`.
- A verdade continua em `meu-negocio/`; o arquivo de contexto é **projeção**, não segunda fonte. Quando a nota original mudar, este arquivo se regenera — não se edita nos dois lugares.

Se o encaixe for prompt e não arquivo, entregue o bloco colável e grave-o em `meu-negocio/` como nota normal, pra não se perder.

## 5. Validar numa rodada real

Arquivo de contexto não se aprova lendo. Rode a skill **uma vez, num caso real e pequeno** que a pessoa já tenha, e pergunte:

> *"isso saiu com a tua cara ou ainda saiu genérico?"*

- Genérico → pergunte **qual linha entregou o genérico**. Aquela linha é a régua faltando: acrescente-a ao arquivo e rode de novo. Duas rodadas costumam bastar; três é o normal.
- Com a cara dela → grave o antes/depois em `operacao/o-que-melhorou/` e registre em `meu-negocio/o-que-funciona.md` o que a régua corrigiu.

**Três correções do mesmo tipo** viram candidata a mudança permanente no arquivo — nunca autoedite o motor nem a skill de terceiro em silêncio.

## 6. Deixar o relógio

Feche dizendo **quando esse arquivo envelhece** (mudou oferta, mudou ICP, mudou régua) e quem o reaviva: o `/revisar` cobra frescor todo mês; o `/reindex` pergunta se a frente mudou.

Se a pessoa quiser moldar várias skills, molde **uma** e mostre o resultado antes de oferecer a próxima — o mesmo arquivo de contexto costuma servir a um bloco inteiro do catálogo, e descobrir isso vale mais que preencher seis formulários.

Regras: contexto vem do cérebro, não de formulário · lacuna marcada, nunca suposição · o arquivo vai onde a skill procura · valida rodando, não lendo · `meu-negocio/` é a fonte, o arquivo de contexto é projeção · PII nunca.
