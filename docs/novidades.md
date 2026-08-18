---
title: Novidades
nav_order: 8
description: O que mudou no V3RHelp em cada versão, em linguagem simples.
---

# Novidades
{: .no_toc }

O que chegou de novo no V3RHelp, da versão mais recente para a mais antiga. Sem jargão — só o
que muda para você.

{: .dica }
> Você confere a versão instalada no seu sistema em **V3RHelp! > Shortcodes e Documentação**,
> no rodapé da página ("V3RHelp X.Y.Z").

---

<div class="timeline" markdown="1">

## 1.30.0 · agosto / 2026
{: .text-green-200 }

- **Confirmação garantida para quem abre chamado sem conta:** quem não tem conta no site
  agora recebe o e-mail de confirmação com o link de acompanhamento **sempre** — inclusive
  quando o chamado nasce por uma [integração externa](modulos/integracoes) (por exemplo, um
  formulário fora do WordPress ligado por chave de API), e não só pela Central de Atendimento.
  Antes, um chamado de visitante aberto por integração podia deixar a pessoa sem nenhuma forma
  de acompanhar. Veja em [Configurações](modulos/configuracoes).

## 1.29.2 · agosto / 2026
{: .text-green-200 }

- **Limpeza interna, sem efeito na tela:** uma regra que existia duplicada em dois pontos do
  código passou a existir num só. Não muda nada no que você vê ou faz no V3RHelp.

## 1.29.0 · agosto / 2026
{: .text-green-200 }

- **Abertura de chamados por sistema externo:** a nova aba [Integrações](modulos/integracoes)
  ganhou o escopo **Escrita** para chaves de API — dá para um sistema externo (por exemplo, um
  formulário que já existe no seu site, fora do WordPress) abrir chamados no V3RHelp
  automaticamente, sem ninguém copiar e colar nada.

## 1.28.1 · agosto / 2026
{: .text-green-200 }

- **Correção em Integrações:** ao criar uma chave de API ou um webhook sem marcar a
  confirmação sobre envio de dados, o aviso pedindo para marcá-la ficava escondido atrás da
  janela — parecia que nada tinha acontecido ao clicar em "Gerar chave" ou "Cadastrar". Agora
  o aviso aparece dentro da própria janela.

## 1.28.0 · agosto / 2026
{: .text-green-200 }

- **Nova aba Integrações:** conecte o V3RHelp a ferramentas externas de automação, como o
  **n8n** — por exemplo, para alimentar uma planilha do Google automaticamente. Duas formas de
  conectar: **chaves de API**, para a ferramenta externa consultar chamados, e **webhooks de
  saída**, para o V3RHelp avisar sozinho quando algo acontece (chamado aberto, respondido,
  status alterado, entre outros). Visível só para o supervisor. Veja em
  [Módulos > Integrações](modulos/integracoes).

## 1.27.1 · agosto / 2026
{: .text-green-200 }

- **Ajuste visual:** correção pontual para o painel manter a própria aparência em temas de
  site que ainda insistiam em sobrescrever a cor de fundo de alguns campos.

## 1.27.0 · agosto / 2026
{: .text-green-200 }

- **O painel mantém a própria aparência dentro do site:** quando o painel do V3RHelp é
  colocado numa página do seu site (em vez do wp-admin), ele agora resiste melhor ao CSS do
  tema e não fica mais "espremido" nem com a aparência quebrada por regras de estilo do site.

## 1.26.3 · agosto / 2026
{: .text-green-200 }

- **Correção no seletor de membros da Equipe:** ao trocar de busca depois de já ter marcado
  alguém, o nome dessa pessoa podia sumir da etiqueta e aparecer como um código cru. Agora o
  nome fica guardado e continua aparecendo certinho, não importa quantas buscas você fizer.

## 1.26.2 · agosto / 2026
{: .text-green-200 }

- **Ajuste visual nos campos de busca:** nos campos de busca do painel (Chamados e Equipe), o
  ícone da lupa não fica mais em cima do texto digitado, e o espaçamento dos campos foi
  corrigido.

## 1.26.1 · agosto / 2026
{: .text-green-200 }

- **Logo pela biblioteca de mídia:** em [Configurações](modulos/configuracoes), além de enviar
  um arquivo novo, agora dá para clicar em **Escolher da biblioteca** e reaproveitar uma imagem
  de logo já enviada ao site.

## 1.26.0 · agosto / 2026
{: .text-green-200 }

- **Quem enxerga quais chamados:** nova opção em
  [Configurações](modulos/configuracoes#quem-enxerga-quais-chamados) para marcar, papel do
  WordPress por papel, quem enxerga **todos** os chamados na Central de Atendimento em vez de
  só os próprios — útil para coordenadores e gestores que acompanham tudo sem entrar na equipe
  de suporte. Por padrão, ninguém ganha essa visão ampliada: o comportamento de sempre continua
  valendo até você marcar um papel.

## 1.25.1 · agosto / 2026
{: .text-green-200 }

- **Ajuste visual:** o cursor agora vira uma mãozinha ao passar sobre abas e botões do painel,
  deixando mais claro o que é clicável.

## 1.25.0 · agosto / 2026
{: .text-green-200 }

- **Ações em lote nos chamados:** na lista de [Chamados](modulos/chamados#chamados-em-lote), marque
  vários chamados (ou todos os visíveis) e aplique de uma vez: **mudar status**, **designar a um
  operador ou grupo**, **exportar** ou **excluir**. A exclusão em lote é **definitiva** e só o
  **supervisor** pode fazer, com uma confirmação mostrando quantos e quais chamados serão
  apagados antes de você confirmar.

## 1.24.3 · agosto / 2026
{: .text-green-200 }

- **Busca ao adicionar membros da Equipe:** o seletor de "Adicionar membro" agora tem um campo
  de **busca** por nome ou e-mail e permite **marcar várias pessoas** para adicionar de uma vez,
  todas com o mesmo papel e as mesmas categorias. Antes, a lista mostrava só uma fatia fixa dos
  usuários do site e cada pessoa precisava ser adicionada separadamente.

## 1.24.0 · julho / 2026
{: .text-green-200 }

- **Escolha de membros do grupo com busca:** ao montar um [grupo](modulos/grupos), agora você encontra
  os operadores por um campo de **busca**, vê os escolhidos como etiquetas com um contador, e pode
  **selecionar todos os filtrados** de uma vez — bem mais prático que a lista de marcações anterior,
  principalmente para equipes grandes.

## 1.23.0 · julho / 2026
{: .text-green-200 }

- **Grupos de operadores:** agora dá para designar um chamado a um **grupo** de atendentes, não só a
  uma pessoa. O time trabalha junto no mesmo chamado ou um dos membros clica em **Assumir** para
  cuidar dele — e pode **Devolver ao grupo** depois. Você monta os grupos na nova tela **Grupos** e
  pode fazer cada **categoria** (ou tipo de solicitação) mandar os chamados novos direto para um grupo.
  Veja em [Módulos > Grupos](modulos/grupos).

## 1.22.0 · julho / 2026
{: .text-green-200 }

- **Exportação mais organizada:** a exportação agora separa **Configuração** (configurações, SLA e
  categorias — para replicar num site novo) de **Dados** (chamados + operadores). Assim você leva a
  "receita" do seu suporte para outra instalação sem arrastar junto os chamados e as pessoas.

## 1.21.0 · julho / 2026
{: .text-green-200 }

- **Conjuntos de campos condicionais:** um formulário pode mostrar **grupos de campos diferentes**
  conforme a escolha do solicitante. Ex.: um select "Tipo de pedido" (licença, isenção, mudança…)
  revela só os campos daquele pedido. Ótimo para atender vários tipos de solicitação num formulário
  só.

## 1.20.0 · julho / 2026
{: .text-green-200 }

- **Painel de atendimento no seu site:** um novo shortcode `[v3rhelp_admin]` coloca o **painel
  completo** (Dashboard e todas as opções) numa página do próprio site, só para a equipe logada —
  útil para atender sem entrar no painel do WordPress.

## 1.18.0 · julho / 2026
{: .text-green-200 }

- **Campos que aparecem só quando precisam:** agora um campo do formulário pode ser **condicional**
  — ele só aparece quando outro campo tem um certo valor (por exemplo, mostrar "CNPJ" apenas se o
  tipo de pessoa for "Jurídica"). Menos formulário na tela, mais foco no que importa. Também
  chegou a **máscara de CEP**.

## 1.17.0 · julho / 2026
{: .text-green-200 }

- **Entrega de documento pelo operador:** ao responder um chamado, a equipe pode marcar a
  resposta como **"documento entregue"**. O solicitante recebe um **e-mail avisando que há um
  documento disponível** e vê a mensagem destacada com o selo **"Documento disponível"**. Fecha
  o fluxo de quem usa o V3RHelp como **protocolo** (pedir e entregar documentos).

## 1.16.0 · julho / 2026
{: .text-green-200 }

- **Consentimento LGPD nos formulários:** já vem um conjunto de campos pronto de **Consentimento
  LGPD** para você usar nos seus formulários. Quando o solicitante aceita, o chamado guarda **o
  texto do aceite e a data e hora** — bom para conformidade e transparência.

## 1.15.0 · julho / 2026
{: .text-green-200 }

- **Formulários personalizados de chamados:** agora você monta **tipos de solicitação** com os
  **campos que quiser** (texto, número, data, listas, caixas de seleção, anexo…), com campos
  **obrigatórios** e validação (CPF, CNPJ, telefone). Os campos ficam em **conjuntos
  reutilizáveis** que você aproveita em vários tipos. Na hora de abrir o chamado, quem pede
  escolhe o tipo e preenche só o que importa — e a equipe vê tudo organizado no bloco **"Dados do
  formulário"**. Configure em **V3RHelp! > Tipos de solicitação** e **Conjuntos de campos**.

## 1.12.0 · julho / 2026
{: .text-green-200 }

- **Menos spam nos chamados públicos:** o formulário de abertura por **visitantes** ganhou uma
  proteção anti-spam **invisível** — sem captcha e sem atrapalhar quem é gente de verdade. Vem
  ligada e pode ser ajustada em **Configurações > Público**.

## 1.11.0 · julho / 2026
{: .text-green-200 }

- **Atenda pela Central, sem abrir o painel:** supervisores e operadores agora podem **ver e
  cuidar de chamados direto pela página pública** da Central de Atendimento. O supervisor
  enxerga **todos** os chamados; o operador, os que estão **com ele**. Dá para **responder,
  mudar o status e designar** por ali mesmo.

## 1.10.0 · julho / 2026
{: .text-green-200 }

- **Status que anda sozinho:** quando a equipe **responde** um chamado, ele já passa para
  **Em andamento** — sem precisar mudar na mão.
- **Resolveu e o problema voltou? Basta responder:** se o seu chamado foi marcado como
  resolvido mas persiste, é só **responder** que ele **reabre automaticamente**. Se já houve
  muitas reaberturas, o sistema abre um **chamado novo ligado ao antigo**, sem perder nada.

## 1.9.0 · julho / 2026
{: .text-green-200 }

- **Cada chamado com um dono:** dá para escolher se os chamados novos já saem **com um
  operador** (por rodízio) ou ficam para a equipe distribuir à mão.
- **Supervisão no radar:** os **supervisores** passam a receber uma **cópia** de cada chamado
  aberto, para acompanhar o movimento sem depender de ninguém avisar.
- **Transferência sem surpresa:** ao passar um chamado para outro operador, os **dois** — o
  novo e o anterior — são avisados por e-mail.

## 1.8.0 · julho / 2026
{: .text-green-200 }

- **Enviar feedback ficou mais completo:** o formulário de **feedback sobre o V3RHelp** (para a
  equipe da V3RTECH) ganhou **tipos** (Sugestão, Dúvida, Bug, Depoimento, Outros), campos de
  **depoimento** com autorização de publicação, **e-mail para resposta** e uma **cópia de
  confirmação** para você.

## 1.7.1 · julho / 2026
{: .text-green-200 }

- **E-mails de feedback mais úteis:** passam a incluir a **logo** no topo e um resumo do
  **ambiente**, dando contexto para a equipe entender o cenário mais rápido.

## 1.7.0 · julho / 2026
{: .text-green-200 }

- **Anexos no feedback:** ao mandar um feedback sobre o V3RHelp, agora dá para **anexar
  arquivos** (prints, documentos) junto da mensagem.

## 1.6.0 · julho / 2026
{: .text-green-200 }

- **Quem abriu, sempre à vista:** a lista de chamados agora mostra a coluna **Solicitante**
  (nome e e-mail), e o detalhe também — sem precisar entrar em cada chamado para saber de quem é.
- **Anexos repensados:** cada arquivo aparece **junto da mensagem** em que foi enviado; a equipe
  pode anexar **vários arquivos de uma vez** numa resposta e **remover** anexos quando preciso.
  Arquivos de nota interna continuam **só para a equipe**.
- **Para quem abre chamados:** ao enviar, você vê uma **mensagem clara de confirmação** e já cai
  na tela de acompanhamento; e agora dá para **anexar arquivos também nas respostas**, não só na
  abertura. O link **"Meus chamados"** leva sempre ao chamado certo.
- **Sua página, do seu jeito:** dá para **ligar ou desligar a logo** da organização nas telas
  públicas de atendimento.

## 1.5.0 · julho / 2026
{: .text-green-200 }

- **Notas internas:** a equipe pode registrar observações **visíveis só para o suporte**, sem
  que o solicitante veja — o histórico técnico fica separado da conversa com o cliente.
- **Anexos na abertura pública:** quem abre um chamado pela página do site pode **anexar
  arquivos** já no formulário.

## 1.4.0 · julho / 2026
{: .text-green-200 }

- A aba de ajuda do painel virou **"Shortcodes e Documentação"**, com visual renovado e um
  atalho direto para este manual.

## 1.3.0 · julho / 2026
{: .text-green-200 }

- **Lembretes inteligentes:** dá para ligar ou desligar cada tipo de aviso por e-mail e, de
  quebra, receber um lembrete quando um chamado fica **parado** por muitos dias.

## 1.2.0 · julho / 2026
{: .text-green-200 }

- **E-mails com a sua cara:** as mensagens automáticas passaram a ter cabeçalho com a logo da
  organização, um resumo do chamado, um **botão** para acompanhar e um rodapé com os links
  importantes.

## 1.1.0 · julho / 2026
{: .text-green-200 }

- **Diagnóstico mais rápido:** ao abrir um chamado, o sistema registra automaticamente o
  ambiente de quem pediu ajuda (navegador, sistema, tela) — sem coletar dados pessoais. A
  equipe passa a resolver sem precisar ficar perguntando "qual navegador você usa?".

## 1.0.0 · julho / 2026
{: .text-green-200 }

- **Primeira versão estável do V3RHelp!** 🎉 Com tudo o que um bom atendimento precisa:
  - abertura e acompanhamento de chamados, com status e histórico;
  - prazos de atendimento (SLA) com semáforo em tempo real;
  - painel com indicadores e gráficos;
  - página pública para abrir chamados (inclusive por quem não tem conta);
  - importação e exportação de dados;
  - interface disponível em **português** e **inglês**.

</div>
