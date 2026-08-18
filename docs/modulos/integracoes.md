---
title: Integrações
parent: Módulos
nav_order: 9
role: [supervisor]
routes: [/wp-admin/admin.php?page=v3rhelp#/integrations]
screenshots: []
source_docs: [ARCHITECTURE.md#adr-017, "#82", "#84"]
last_verified: 2026-08-18
status: publicado
description: Conecte o V3RHelp a ferramentas externas de automação (como o n8n) por chave de API ou por webhook.
---

# Integrações
{: .no_toc }

<details open markdown="block">
  <summary>
    Índice
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

*(Captura pendente — esta funcionalidade é nova, v1.28/1.29, e as telas serão adicionadas
numa próxima passada. Veja o que precisa aparecer em cada print no relatório desta entrega.)*

## O que é a aba Integrações

Na tela **V3RHelp! > Integrações**, você conecta o V3RHelp a ferramentas externas de
automação — na prática, o caso mais comum é o **n8n**, que pode receber os avisos do V3RHelp
e, por exemplo, alimentar uma planilha do Google automaticamente. Existem duas formas de
conectar, e elas resolvem problemas diferentes:

- **Chaves de API** — a ferramenta externa **pergunta** ao V3RHelp (consulta chamados ou,
  com a chave certa, abre chamados novos).
- **Webhooks de saída** — o V3RHelp **avisa** a ferramenta externa quando algo acontece, sem
  ela precisar ficar perguntando.

{: .importante }
> **Por que isso é importante:** antes, ligar o V3RHelp a uma automação exigia alguém mexendo
> direto no banco de dados ou reconstruindo em outro sistema o que já existia aqui. Com chave
> de API e webhook, a conexão é feita pela própria tela do painel, sem tocar em código — e o
> administrador decide exatamente o que cada conexão pode ver ou fazer.

Esta aba só aparece para o **supervisor**. Operadores e quem apenas abre chamados não a veem.

## Chaves de API

Uma chave de API é um código secreto que você gera para que um sistema externo se identifique
junto ao V3RHelp e converse com ele — sem usar login nem senha de ninguém.

### Como gerar uma chave

1. Acesse **V3RHelp! > Integrações**.
2. No bloco **Chaves de API**, clique em **Nova chave**.
3. Preencha o **Nome** — algo que identifique quem vai usar a chave, como "n8n — planilha de
   chamados".
4. Escolha o **Escopo**:
   - **Leitura** — o sistema externo só consulta chamados; não abre, não responde, não altera
     nada.
   - **Escrita (abertura de chamados)** — o sistema externo pode **abrir chamados** no
     V3RHelp. É o caso de um formulário que já existe no site: o formulário continua sendo o
     formulário, e o chamado nasce no V3RHelp automaticamente, sem ninguém copiar e colar.
5. Marque a confirmação de dados (veja abaixo) e clique em **Gerar chave**.
6. Copie o valor mostrado **na hora** — é a única vez que ele aparece.

{: .importante }
> **Desde a v1.30.0**, um chamado aberto por uma chave de **Escrita** em nome de alguém sem
> conta no site recebe o mesmo **e-mail de confirmação com o link de acompanhamento** que
> recebe quem abre pela Central. Faz sentido: para quem não tem conta, esse e-mail é a
> **única porta de entrada** para acompanhar o próprio chamado — sem ele, a pessoa não tem
> como saber que o pedido foi recebido nem como voltar a ele depois. Isso não depende da opção
> de notificações de abertura (veja [Configurações](configuracoes)), que só vale para quem
> tem conta.

{: .atencao }
> **A chave é exibida uma única vez, na criação.** Depois disso o painel só mostra o prefixo
> (os primeiros caracteres), para você reconhecer a chave na lista, nunca o valor completo. Se
> perder o valor, não tem como recuperar: **gere uma outra chave** e atualize a ferramenta
> externa com o novo valor.

### A confirmação de dados

Ao gerar qualquer chave, o painel exige marcar uma confirmação de que os dados dos chamados —
**inclusive nome, e-mail e mensagens dos solicitantes** — ficarão disponíveis para a
ferramenta externa que usar aquela chave. Isso não é burocracia: é uma decisão consciente
sobre dado pessoal de terceiros, e cabe a quem administra a instalação avaliar se aquela
ferramenta externa é confiável antes de marcar a caixa.

### Revogar uma chave

Na lista de chaves, clique em **Revogar**. A revogação **vale na hora**: qualquer sistema que
esteja usando aquela chave para de funcionar imediatamente, sem aviso prévio ao sistema
externo. Use quando uma integração deixa de ser necessária ou quando desconfiar que a chave
vazou.

### Encontrar chave esquecida

A lista de chaves mostra a coluna **Último uso**. Uma chave com "Nunca usada" ou com uma data
muito antiga é candidata a ser revogada — sinal de uma integração que foi testada e
abandonada, ou de uma automação que já não existe mais do outro lado.

{: .dica }
> Revise a lista de chaves de vez em quando, do mesmo jeito que revisaria quem tem acesso a
> um sistema. Chave esquecida e ativa é uma porta aberta que ninguém está de olho.

{: .exemplo }
> Sua organização quer que os chamados abertos por um formulário de intranet (fora do
> WordPress) apareçam automaticamente no V3RHelp. Você gera uma chave com escopo **Escrita**,
> chamada "Intranet — abertura automática", entrega o valor para quem mantém o formulário, e
> a partir daí cada envio do formulário vira um chamado novo no V3RHelp — sem ninguém da
> equipe digitar nada.

## Webhooks de saída

Em vez de a ferramenta externa perguntar de tempos em tempos, o V3RHelp **avisa** — envia um
aviso automático assim que algo acontece: um chamado é aberto, respondido, muda de status,
é designado, entre outros eventos.

### Como cadastrar um webhook

1. No bloco **Webhooks de saída**, clique em **Novo webhook**.
2. Informe a **URL de destino** — o endereço da ferramenta externa que vai receber os avisos.
3. Marque os **Eventos** que devem disparar um aviso (chamado aberto, respondido, status
   alterado, designado, e os demais disponíveis).
4. Marque a confirmação de dados e clique em **Cadastrar**.
5. Copie o **segredo** mostrado na hora do cadastro.

{: .importante }
> **Por que isso é importante:** o segredo serve para a ferramenta do outro lado **conferir
> que o aviso veio mesmo do V3RHelp**, e não de alguém se passando por ele. Sem o segredo, um
> sistema mal-intencionado poderia forjar avisos falsos de "chamado aberto" ou "chamado
> resolvido" para o seu destino.

### Repetição e identificador de entrega

Se a rede falhar no meio do caminho, **o mesmo aviso pode chegar mais de uma vez** — por isso
cada aviso tem um **identificador próprio**. A ferramenta do outro lado usa esse identificador
para reconhecer que já processou aquele aviso antes e ignorar a repetição, em vez de, por
exemplo, duplicar a linha na planilha.

Se o destino estiver fora do ar no momento do envio, o V3RHelp **tenta de novo**, espaçando as
tentativas — não desiste na primeira falha, mas também não insiste para sempre.

{: .dica }
> Ao configurar o destino (por exemplo, um fluxo no n8n), guarde os identificadores de entrega
> já processados por um tempo, e descarte qualquer aviso repetido. É o que torna a integração
> segura mesmo com falha de rede.

### Gerar novo segredo e remover

Use **Gerar novo segredo** quando desconfiar que o segredo vazou — o webhook continua ativo,
só passa a assinar com um valor novo (atualize a ferramenta externa também). Use **Remover**
para desligar de vez a integração; o histórico de entregas daquele webhook é apagado junto.

{: .atencao }
> Depois de gerar um novo segredo, **a ferramenta externa precisa ser atualizada com o valor
> novo**, senão ela passa a rejeitar os avisos por assinatura inválida (veja "Quando dá
> errado", abaixo).

{: .exemplo }
> Você cadastra um webhook apontando para um fluxo do n8n, com os eventos "chamado aberto" e
> "chamado resolvido" marcados. A cada chamado aberto ou resolvido, o n8n recebe o aviso e
> adiciona ou atualiza uma linha numa planilha do Google — sem ninguém da equipe entrar na
> planilha manualmente.

## Quando dá errado

- **"Confirme o aviso de dados antes de gerar a chave" / "...antes de cadastrar o webhook"** —
  a caixa de confirmação de dados pessoais não foi marcada. Marque-a e tente de novo.
- **A ferramenta externa diz que a chave é inválida ou que o acesso foi negado** — a chave foi
  revogada, digitada errada, ou o escopo dela não cobre a ação que a ferramenta está tentando
  (por exemplo, uma chave de leitura sendo usada para tentar abrir chamado). Confira o escopo
  na lista de chaves; se for o caso, gere uma chave nova com o escopo certo.
- **O destino do webhook diz que a assinatura é inválida** — o segredo configurado do lado de
  fora não é mais o mesmo do V3RHelp, geralmente porque alguém gerou um novo segredo e
  esqueceu de atualizar a ferramenta externa. Copie o segredo atual na lista de webhooks e
  atualize a ferramenta.
- **Os avisos pararam de chegar** — confira se o webhook está **Ativo** na lista; ele pode ter
  sido desativado. Se estiver ativo e mesmo assim nada chega, confirme se a URL de destino
  ainda está correta e no ar.

## Próximos passos

- [Chamados](chamados.html) — os eventos que os webhooks avisam (aberto, respondido, status
  alterado, designado) são os mesmos que acontecem nesta tela.
- [Configurações](configuracoes.html) — outras opções administrativas da instalação.
- [Política de Privacidade](/legal/privacidade/) — o que muda no tratamento de dados quando
  você liga uma integração externa.
