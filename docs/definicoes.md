---
title: Definições
nav_order: 2
description: Glossário dos termos do mundo dos chamados, em ordem alfabética e em linguagem simples.
---

# Definições
{: .no_toc }

Os termos abaixo aparecem ao longo do manual e dentro do V3RHelp!. Estão em ordem
alfabética e explicados em linguagem simples. Se bater dúvida em qualquer página, volte aqui.

{: .dica }
> Não precisa decorar nada. Leia por cima agora e use esta página como consulta quando
> topar com uma palavra nova.

---

## Anexo
Um arquivo enviado junto com o chamado ou com uma resposta — uma foto, um print da tela,
um documento. Anexos ajudam a equipe a **entender o problema mais rápido**.

## Categoria
O "assunto" do chamado (por exemplo: *Financeiro*, *Acesso*, *Manutenção*). Serve para
**direcionar** o chamado para a pessoa ou o time certo e para organizar os relatórios.

## Chamado
O registro de um pedido de ajuda. Tem um **código único** (como `A1B2-C3D4`), um assunto,
uma descrição, um status e um histórico de mensagens.

## Chave de API
Um código secreto que você gera em [Integrações](/modulos/integracoes/) para que um sistema
externo (como uma automação no n8n) converse com o V3RHelp sem precisar de login. Cada chave
tem um **escopo** (leitura ou escrita) e pode ser **revogada** a qualquer momento.

## Escopo
O que uma chave de API tem permissão de fazer. **Leitura** só consulta chamados; **escrita**
também pode abrir chamados novos. Uma chave nunca faz mais do que o escopo escolhido na
criação permite.

## Idempotência
A garantia de que reenviar o mesmo aviso duas vezes não duplica nada do outro lado. No
V3RHelp isso aparece nos [webhooks](#webhook): cada aviso leva um identificador de entrega
próprio, para a ferramenta externa reconhecer um reenvio (por exemplo, depois de uma falha de
rede) e ignorá-lo, em vez de processar a mesma coisa duas vezes.

## Magic link
Um link especial enviado por e-mail que permite a quem **não tem conta** acompanhar e
responder ao próprio chamado, com segurança, **sem precisar fazer login**.

## Operador
A pessoa da equipe de suporte que **atende** os chamados: lê, responde, resolve. Cada
operador costuma atender determinadas categorias.

## Prioridade
Uma indicação de **urgência** do chamado. Ajuda a equipe a decidir o que atacar primeiro.

## Reabertura
Quando um chamado que estava **resolvido** volta a ficar ativo — porque o problema não foi
totalmente resolvido ou voltou a acontecer.

## Resposta
Cada mensagem trocada dentro do chamado, do solicitante para a equipe ou da equipe para o
solicitante. O conjunto de respostas forma o **histórico**.

## SLA (prazo de atendimento)
Sigla de *Service Level Agreement* — o **compromisso de prazo**. É o tempo combinado para
dar a primeira resposta e para resolver o chamado. O V3RHelp mostra um "semáforo" de SLA:
no prazo, em atenção ou vencido.

{: .exemplo }
> Um SLA pode dizer: "primeira resposta em até 2 horas e solução em até 1 dia útil".
> Se o tempo está acabando, o sistema avisa a equipe.

## Solicitante
Quem **abre** o chamado e pede a ajuda — cliente, assinante, autor, colaborador etc.

## Status
O **momento** em que o chamado está. Os principais são:

| Status | O que significa |
|---|---|
| **Aberto** | Recém-criado, ainda não começou a ser atendido. |
| **Em andamento** | A equipe já está cuidando. |
| **Aguardando** | Parado esperando algo (uma informação do solicitante, por exemplo). |
| **Resolvido** | O pedido foi atendido. |
| **Reaberto** | Estava resolvido e voltou a ficar ativo. |
| **Cancelado** | Encerrado sem solução (duplicado, engano etc.). |

## Supervisor
A pessoa que **coordena** a equipe de suporte: acompanha os indicadores, distribui o
trabalho, cuida das categorias, dos prazos (SLA) e da equipe de operadores.

## Webhook
Um aviso automático que o V3RHelp envia para um endereço externo assim que algo acontece — um
chamado é aberto, respondido, muda de status. Em vez de a ferramenta externa perguntar de
tempos em tempos, o V3RHelp avisa na hora. Configura-se em
[Integrações](/modulos/integracoes/).
