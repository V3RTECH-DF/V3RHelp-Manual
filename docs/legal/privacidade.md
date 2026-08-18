---
title: Política de Privacidade
parent: Jurídico
nav_order: 1
description: Como o V3RHelp! trata dados pessoais, à luz da LGPD.
---

# Política de Privacidade
{: .no_toc }

Esta política explica como o **V3RHelp!** trata dados pessoais. O V3RHelp é um plugin de
WordPress **auto-hospedado**: ele roda no site da sua organização, e é a sua organização —
não a V3RTECH — quem controla os dados dos chamados.

<details open markdown="block">
  <summary>Nesta página</summary>
- TOC
{:toc}
</details>

{: .atencao }
> Este texto é um modelo. Ele **não substitui a orientação de um advogado**. Ajuste-o à
> realidade da sua organização e à legislação aplicável (no Brasil, a LGPD).

---

## Parte A — O papel da V3RTECH

### A.1 A V3RTECH não hospeda os dados dos chamados
A V3RTECH é a **fornecedora do software**. O V3RHelp é instalado no seu WordPress e grava tudo
no **seu próprio banco de dados**. A V3RTECH **não hospeda, não acessa e não recebe** os dados
dos chamados. Não há envio automático de dados para servidores da V3RTECH.

### A.2 Dados que você fornece diretamente à V3RTECH
Se você entrar em contato com a V3RTECH (suporte, compra), os dados dessa interação são usados
apenas para aquela finalidade, conforme a LGPD.

### A.3 Encarregado de Dados (DPO)
Dúvidas sobre privacidade do software podem ser enviadas ao Encarregado de Proteção de Dados
da V3RTECH: **dpo@v3rtech.com.br**.

---

## Parte B — Dados tratados pelo plugin (sob controle da sua organização)

### B.1 O que o V3RHelp armazena
No banco de dados do WordPress da sua organização, o plugin mantém:

- **Dados do chamado:** assunto, descrição, categoria, status, histórico de mensagens e notas.
- **Dados do solicitante:** nome e e-mail (informados por quem abre o chamado) e, para
  usuários logados, a associação à conta do WordPress.
- **Anexos:** arquivos enviados nos chamados, guardados na biblioteca de mídia do WordPress.
- **Ambiente técnico da abertura:** navegador, sistema operacional, tipo de dispositivo,
  tamanho de tela, idioma, fuso horário e as versões do V3RHelp/WordPress/PHP.

{: .importante }
> **O V3RHelp não coleta o endereço IP** de quem abre o chamado, nem outros dados pessoais além
> dos que a própria pessoa informa. O "ambiente técnico" guarda apenas características do
> dispositivo/navegador, para ajudar a equipe a diagnosticar o problema — nunca para
> identificar a pessoa.

### B.2 Finalidades e base legal
Os dados são tratados para **prestar o atendimento** solicitado (registrar, responder e
resolver o chamado) e para **comunicar o solicitante** sobre o andamento. A base legal usual é
a **execução de procedimentos a pedido do titular** e o **legítimo interesse** em prestar
suporte. Cabe à sua organização confirmar a base adequada e informar os titulares.

### B.3 Comunicações por e-mail
O V3RHelp envia e-mails transacionais (confirmação de abertura, respostas, resolução,
lembretes) usando o servidor de e-mail configurado no seu WordPress. O conteúdo desses e-mails
inclui informações do chamado.

### B.4 Compartilhamento com terceiros
O plugin **não compartilha** dados com terceiros por conta própria. Serviços externos só
recebem dados se a sua organização os configurar (por exemplo, um serviço de envio de e-mail).

### B.5 Integrações externas (chaves de API e webhooks)
O administrador da sua instalação pode gerar **chaves de API** e cadastrar **webhooks** para
que ferramentas de automação externas (por exemplo, o n8n) leiam ou recebam dados dos
chamados — incluindo nome, e-mail, descrição e mensagens do solicitante. Essa integração é uma
decisão do **administrador da instalação**, não da V3RTECH: a base legal e o destino desses
dados são responsabilidade de quem configura a chave ou o webhook. Ao criar cada credencial, o
painel exige uma confirmação explícita desse envio antes de liberar. Veja como funciona em
[Módulo de Integrações](/modulos/integracoes/).

### B.6 Direitos do titular
Conforme a LGPD, o titular pode solicitar **confirmação, acesso, correção, portabilidade e
exclusão** de seus dados. A equipe da organização pode localizar e gerenciar esses dados pelas
telas de Chamados do painel.

### B.7 Retenção e eliminação
A sua organização define por **quanto tempo** os chamados são mantidos, conforme a necessidade
e a legislação. A exclusão de um chamado remove seus dados da base.

### B.8 Segurança
Recomenda-se manter o site em **HTTPS**, o WordPress e os plugins **atualizados**, e restringir
o **acesso administrativo** apenas a quem precisa.

---

## Alterações desta política
Esta política pode ser atualizada. A versão vigente fica em
`docs.v3rhelp.v3rtech.com.br/legal/privacidade/`.

**Contato:** dpo@v3rtech.com.br · suporte@v3rtech.com.br

_Versão deste documento: 1.1 (agosto de 2026) — adicionada a seção B.5, sobre integrações
externas (chaves de API e webhooks)._
