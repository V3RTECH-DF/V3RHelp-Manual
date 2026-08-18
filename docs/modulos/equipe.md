---
title: Equipe
parent: Módulos
nav_order: 4
role: [supervisor]
screenshots: [mod-equipe-01, mod-equipe-02-busca-multipla]
last_verified: 2026-08-18
status: publicado
description: Quem atende os chamados — operadores e supervisores — e quais categorias cada um cobre.
---

# Equipe
{: .no_toc }

<details open markdown="block">
  <summary>
    Índice
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

Na tela **V3RHelp! > Equipe** você organiza quem atende os chamados: quem são os operadores, quem são os supervisores e quais categorias cada operador cobre.

![Gestão da equipe](../assets/mod-equipe-01.png)

## O que é a Equipe

Todo membro da equipe de suporte é, antes de tudo, um usuário do WordPress. Ao adicioná-lo na tela Equipe, ele é promovido a um dos dois papéis do V3RHelp:

- **Operador** — atende chamados. Pode ser designado automaticamente pelo rodízio ou receber chamados manualmente.
- **Supervisor** — além de atender chamados, coordena a equipe: acompanha o andamento geral, redistribui chamados e gerencia a própria tela de Equipe.

## Adicionar um membro

1. Clique em **Adicionar membro**.
2. Digite no campo de **busca** para encontrar as pessoas pelo **nome ou e-mail** — a busca
   olha o site inteiro, não só uma primeira lista. Quem já está na equipe não aparece: a lista
   mostra só quem ainda pode entrar.
3. Marque **uma ou várias pessoas**; cada uma vira uma etiqueta na área de selecionados, com um
   contador do total marcado.
4. Defina o papel: Operador ou Supervisor. O papel escolhido vale para **todo o grupo marcado**.
5. Se for Operador, escolha as **Categorias** que o grupo atende — use o campo de busca para
   achá-las pelo nome; as escolhidas viram etiquetas com um contador.
6. Salve. Todas as pessoas marcadas entram na equipe de uma vez, com o mesmo papel e as mesmas
   categorias.

![Busca com várias pessoas selecionadas](../assets/mod-equipe-02-busca-multipla.png)

{: .importante }
> Antes, a lista de candidatos mostrava só uma fatia dos usuários do site, sem busca, e cada
> pessoa precisava ser adicionada em uma operação separada. Em site com muitos usuários, isso
> tornava inviável achar quem você queria — e adicionar um time inteiro era clique repetido. A
> busca por nome/e-mail e a seleção múltipla resolvem os dois problemas de uma vez.

{: .dica }
> Monte a equipe de um setor inteiro numa passada só: busque pelo nome do setor ou digite parte
> do e-mail corporativo comum a todos, marque quem apareceu e salve — todos entram com o mesmo
> papel e as mesmas categorias em uma única ação.

{: .atencao }
> Se a sua busca trouxer **mais resultados do que cabe na lista**, o sistema avisa para
> **refinar a busca** em vez de cortar candidatos em silêncio. Se alguém que você esperava ver
> não apareceu, não é bug — é sinal de que a busca ainda está ampla demais. Digite mais
> caracteres do nome ou do e-mail até a pessoa aparecer.

## Editar um membro

Abra o membro na lista para trocar o papel (Operador ↔ Supervisor) ou ajustar as categorias que ele atende. As mudanças valem a partir do próximo chamado a ser designado — chamados já atribuídos não são movidos automaticamente.

## Remover um membro

Remover tira a pessoa da equipe de atendimento: ela deixa de aparecer no rodízio e de poder ser designada para novos chamados.

{: .atencao }
Remover um membro **revoga o papel do V3RHelp**, não exclui o usuário do WordPress. A pessoa continua existindo normalmente como usuário — ela só deixa de fazer parte da equipe de suporte.

## Categorias e o rodízio

Cada operador pode ter uma ou mais categorias marcadas. Isso alimenta o **rodízio** (round-robin): quando um chamado é aberto numa categoria, o sistema designa automaticamente o próximo operador elegível daquela categoria, alternando entre eles a cada novo chamado.

Se um operador não tem nenhuma categoria marcada, ele entra no rodízio de **todas** as categorias.

{: .importante }
Distribuir os operadores por categoria coloca cada chamado com quem realmente entende do assunto e equilibra a carga de trabalho — assim ninguém fica sobrecarregado enquanto outros ficam ociosos.

{: .importante }
A designação automática pelo rodízio evita chamados "sem dono": todo chamado novo já nasce com um responsável definido, sem depender de alguém escolher manualmente.

{: .dica }
O rodízio pode ser **ligado ou desligado** em **Configurações > Chamados** ("Designar operador automaticamente por rodízio ao abrir o chamado"). Desligado, os chamados abrem **sem operador**, para um supervisor fazer a triagem e distribuir à mão.

{: .exemplo }
João atende as categorias "Financeiro" e "Acesso"; Maria atende "Manutenção". Ao abrir um chamado na categoria Financeiro, o rodízio designa automaticamente João — porque é o operador elegível para aquela categoria.

## Próximos passos

- [Grupos](grupos.html) — reúna operadores em times para atenderem chamados em conjunto.
- [Categorias](categorias.html) — como criar e organizar as categorias usadas na Equipe.
- [Chamados](chamados.html) — como um chamado é designado e pode ser redistribuído.
