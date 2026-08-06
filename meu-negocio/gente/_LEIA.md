# gente/ — o eixo PESSOA do teu cérebro
Uma página por pessoa ou empresa que importa: cliente-chave, parceiro, concorrente, fornecedor.
Formato: quem é (2 linhas) · estado atual · histórico (links pros átomos/dailies onde aparece).
Quem alimenta: `/call` e `/daily` perguntam "isso atualiza a página de alguém?".
Regra: pessoa PRIVADA usa papel ("o cliente grande de SC"), nunca nome+dados — PII é regra 5.

## Quem presta serviço: o cliente vira pasta, não página

Quando o mesmo cliente gera entrega recorrente, uma página não segura. Ele vira pasta:

```
gente/<apelido-do-cliente>/
  contexto.md      quem é, o que comprou, o que a gente prometeu
  entregas/        o que já foi feito (um arquivo por entrega, ou ponteiro pro original)
  julgamentos.md   o que ele aprovou, o que rejeitou e POR QUÊ
```

**`<apelido-do-cliente>` é papel, nunca nome real** — `cliente-saas-sc`, `industria-do-parana`. O nome, o
contato e o contrato vivem em `privado/`. Trinta pastas com nome de cliente é o jeito mais rápido de
transformar o cofre em coisa que não pode ser versionada nem mostrada.

**`julgamentos.md` é o arquivo pelo qual a pasta inteira existe.** Contexto envelhece, entrega é
histórico — mas aprovado/rejeitado **com o motivo** é a única coisa ali que fica mais valiosa a cada
mês e que nenhum concorrente consegue copiar. Uma linha por julgamento:

```
- 2026-08-06 · rejeitou <o quê> · motivo: "<as palavras dele, literais>" · virou régua? sim/não
```

> *"esse julgamento não está sendo acumulado. E por conta disso, vocês não conseguem olhar para
> coisas novas"* — [[dia1-cerebro-da-empresa-transcricao]] @ 00:20

Julgamento que aparece em **2+ clientes** sobe pra `meu-negocio/repete.md`. Na **3ª vez**, deixa de ser
padrão de cliente e vira régua da casa (`entrega.md`) ou sistema. Quem faz essa promoção é o `/reindex`.
