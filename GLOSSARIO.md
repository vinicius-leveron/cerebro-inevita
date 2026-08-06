# Glossário — os termos da casa

> Uma linha por termo. **Termo novo só entra no produto passando por aqui** — se uma skill, página ou aula usa uma palavra que não está nesta lista, ou a palavra entra aqui ou ela sai do texto. Entre colchetes, o termo do Vale que ancora o nosso.

| Termo | O que é |
|---|---|
| **Engenharia de Contexto** | O método: montar o contexto certo pra IA em vez de caçar o prompt perfeito. [context engineering — Karpathy] |
| **Contexto** | Tudo que a IA precisa saber do TEU negócio pra responder como sócio, não como estranho. O modelo é igual pra todo mundo; o contexto é a vantagem. |
| **Cérebro** | O cofre de notas + as skills que o operam. A tua IA equipada com o teu contexto. |
| **Átomo** | Nota de UMA ideia: afirmação + citação literal + por quê + elos. Sem citação não é átomo, é palpite. |
| **Bruto** | O material na íntegra (transcrição, print, texto colado), imutável, na bandeja `capturas/`. Guarda-se tudo; opera-se pouco. |
| **Destilar** | Extrair do bruto só o que tem sinal e virar átomo. [“curate before you compute” — Deasy] |
| **Nível de refino** | Até onde uma fonte foi tratada: 0 ponteiro · 1 legível · 2 indexado · 3 destilado · 4 operacional. Para-se no nível que o trabalho exige (`FONTES.md`). [rate of change — "the only axis that drives this is rate of change"] |
| **Ponteiro** | Nível 0: o cérebro registra ONDE a fonte está, sem copiar nem converter. A maioria das fontes vive (bem) aqui. |
| **Motor vs contexto** | Motor = skills e gabaritos (nossos, atualizam via `/atualizar`). Contexto = tuas notas (nunca tocadas por atualização). [harness — o termo do Vale: "fix your harness, don't reprompt"] |
| **Skill** | Know-how executável: um comando que sabe fazer UMA coisa, com as regras embutidas. [skills — workshop AIEWF] |
| **Arquivo de contexto** | O arquivo que uma skill lê pra saber do TEU negócio (ex.: `design/tokens.md`). É projeção de `meu-negocio/`, nunca segunda fonte. Skill sem ele devolve a média da internet. |
| **Protótipo** | O desenho em rascunho de como o dinheiro entra (comercial) e como o trabalho sai (entrega), montado com as palavras do dono e com as lacunas marcadas. É a planta que os sistemas automatizam — nunca o palpite da IA. |
| **Frente** | Uma das três portas onde a primeira fonte encosta: **decisão · venda · entrega**. Escolhe-se a que paga tempo ou dinheiro mais rápido — uma só. |
| **Sistema** | Pacote de um resultado completo: manifest + pipeline + rotinas + skill + eval + feedback + versão. |
| **Pipeline** | Estados pelos quais uma entrada vira uma saída verificável. |
| **Rotina** | Gatilho por evento ou cadência que inicia ou revisa um pipeline. |
| **Conexão** | Interface fina para uma fonte ou ferramenta; não contém o processo inteiro. [MCP/CLI] |
| **Eval** | Régua que compara a saída real com o resultado esperado; existe por execução e no cérebro inteiro. |
| **Feedback** | Correção humana ligada a uma execução e versão, usada para mudar a próxima tentativa. |
| **Self Improvement** | Loop versionado de feedback → mudança pequena → teste → gate humano → nova medição; nunca autoedição cega. |
| **Primeira vitória (A2)** | Artefato de fonte real, aprovado, que o dono confirma ajudar a decidir ou agir. Instalação é A0; começo é A1. |
| **Contribuição** | Payload anonimizado que o dono prepara, aprova e decide enviar à comunidade em passos separados. |
| **Fios** | Os assuntos quentes em andamento (`fios/`) — o horizonte AGORA do negócio. |
| **Gente** | O eixo pessoa (`gente/`): uma página por cliente/parceiro/concorrente-chave. Cliente com entrega recorrente vira pasta. |
| **Julgamento** | O aprovado/rejeitado **com o motivo literal** (`julgamentos.md`). É o discernimento que hoje mora só na cabeça do dono; acumulado, é o que a concorrência não copia. |
| **Repete** | A escada entre atender e produtizar (`repete.md`): 1× é caso · 2× é padrão candidato · 3× vira régua, oferta ou sistema. |
| **Mapa** | O negócio numa página (`mapa.md`) + a métrica principal. Toda resposta estratégica ancora aqui. |
| **Relógios** | As cadências do método: `/daily` (dia), `/reindex` (semana), `/revisar` + `/teste` (mês). |
| **Perguntas-canário** | As 5 perguntas fixas do TEU negócio que medem se o cérebro está aprendendo (`teste-do-cerebro.md`). [evals / golden patterns — os termos do Vale; "canário" é metáfora nossa] |
| **Régua** | A escala do `/teste`: **em branco → estagiário → sócio**. |
| **Frescor** | A validade da nota: `confirmado:` (data da última validação) e `status: superado` (morreu — nada se deleta). É o antídoto do [context rot — "your context rots"]. |
| **Diagnóstico cruzado** | Um resultado possível: o teu negócio × o que o campo já provou, com citação dos dois lados. |
