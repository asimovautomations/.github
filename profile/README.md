<div align="center">

# 🤖 Asimov Academy Automations

### Documentação, versionamento e gestão das automações internas da Asimov Academy

[![n8n](https://img.shields.io/badge/n8n-workflows-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](#)
[![Status](https://img.shields.io/badge/status-em%20evolução-2ea44f?style=for-the-badge)](#)
[![Manutenção](https://img.shields.io/badge/mantido%20por-Asimov%20Academy-blueviolet?style=for-the-badge)](#)

</div>

---

## 📌 Sobre esta organização

> Esta organização existe para **documentar, versionar e gerenciar** as automações internas da Asimov Academy — incluindo fluxos **n8n**, agentes de IA e integrações operacionais.

Não é apenas um lugar para guardar código ou workflows. É o lugar onde cada automação ganha **contexto, histórico, regras de negócio e instruções claras de uso**, para que ninguém dependa de conhecimento informal, prints ou conversas soltas para entender como as coisas funcionam.

<br>

## 🧭 Índice

- [Por que essa organização existe](#-por-que-essa-organização-existe)
- [O que você vai encontrar aqui](#-o-que-você-vai-encontrar-aqui)
- [Como usamos os repositórios](#-como-usamos-os-repositórios)
- [n8n-agent](#-n8n-agent)
- [Como pessoas não técnicas participam](#-como-pessoas-não-técnicas-participam)
- [Como abrir uma issue](#-como-abrir-uma-issue)
- [Como organizar melhorias](#-como-organizar-melhorias)
- [Boas práticas de documentação](#-boas-práticas-para-documentar-automações)
- [Segurança](#-segurança)
- [Primeiros passos](#-para-quem-está-chegando-agora)

<br>

## 🎯 Por que essa organização existe

Boa parte das nossas automações nasce em ferramentas visuais, como o **n8n**. Elas são ótimas para criar fluxos, integrar APIs e colocar processos para rodar — mas não são o melhor lugar para documentar tudo o que uma automação precisa ter.

<table>
<tr><td width="50%" valign="top">

**O que uma ferramenta visual não guarda bem:**
- O que a automação faz
- Quem usa e quem mantém
- Regras de negócio
- Como configurar e testar
- Credenciais e variáveis necessárias

</td><td width="50%" valign="top">

**O que o GitHub resolve:**
- Histórico de decisões
- Documentação viva (README)
- Rastreio de erros conhecidos
- Melhorias planejadas
- Comunicação entre áreas via issues

</td></tr>
</table>

Por isso, usamos o GitHub como **camada de documentação, organização e gestão** das automações. Cada automação importante tem seu próprio repositório, com README, issues, documentação técnica e histórico de evolução.

<br>

## 📂 O que você vai encontrar aqui

| Categoria | Exemplos |
|---|---|
| 🔁 Workflows | Fluxos do **n8n** |
| 🧠 Agentes de IA | Automações orientadas por LLMs |
| 🔌 Integrações | Conexões entre APIs e ferramentas internas |
| 🛠️ Ferramentas de apoio | Utilitários e CLIs do time |
| 📖 Documentação | Regras de negócio e decisões registradas |
| 🐞 Issues | Bugs, melhorias e solicitações |

A ideia é que qualquer pessoa autorizada consiga entender o básico de uma automação **sem depender apenas de conversas soltas, prints ou conhecimento informal.**

<br>

## 🗂️ Como usamos os repositórios

Cada repositório representa uma automação, um conjunto de automações ou uma ferramenta interna. Dentro dele, esperamos encontrar:

- **Visão geral** — o que a automação faz
- **Área responsável** — qual time usa ou mantém
- **Como usar** — instruções para quem opera a automação
- **Como configurar** — variáveis, credenciais e dependências
- **Regras de negócio** — decisões e condições que a automação respeita
- **Fluxos envolvidos** — workflows, agentes, scripts ou integrações relacionados
- **Problemas conhecidos** — limitações e pontos de atenção
- **Histórico de melhorias** — o que já foi feito e o que falta fazer

> 💡 O README de cada repositório deve ser direto, simples e útil. A documentação não precisa ser perfeita desde o primeiro dia — mas precisa existir e evoluir junto com a automação.

<br>

## ⚙️ n8n-agent

Para facilitar o trabalho com automações do n8n, usamos uma ferramenta open-source chamada **`n8n-agent`**.

Essa CLI foi criada para permitir que agentes de IA locais trabalhem melhor com workflows do n8n, sincronizando informações entre a nuvem e o ambiente local.

<details>
<summary><strong>O que o n8n-agent permite fazer</strong> (clique para expandir)</summary>
<br>

- Trazer workflows da nuvem para o ambiente local
- Atualizar workflows locais e enviar mudanças de volta para a nuvem
- Ler partes específicas dos JSONs dos workflows
- Reduzir o tamanho do contexto enviado para modelos de IA
- Transformar estruturas grandes em formatos mais econômicos, como `.toon`
- Editar, adicionar ou remover nodes
- Facilitar análise, manutenção e documentação dos fluxos

</details>

Na prática, o `n8n-agent` conecta três pontas:

```
    ┌────────────────────┐        ┌────────────────────────┐        ┌────────────────────────┐
    │   Workflow no n8n  │  <──>  │  Documentação (GitHub) │  <──>  │  Trabalho local + IA   │
    └────────────────────┘        └────────────────────────┘        └────────────────────────┘
```

Isso permite que agentes de IA ajudem de verdade na manutenção das automações, sem depender de copiar e colar JSONs enormes manualmente.

<br>

## 👥 Como pessoas não técnicas participam

Nem todo mundo que usa uma automação precisa saber programar ou editar workflows. Os repositórios também servem como espaço organizado para que outras áreas participem da melhoria das ferramentas.

Pessoas de áreas como **Customer Success**, **Vendas**, **Produto** e outras podem usar issues padronizadas para:

- 🐞 Reportar problemas
- ✨ Pedir melhorias
- 📋 Explicar casos de uso
- ⚠️ Informar comportamentos inesperados
- 💬 Sugerir ajustes em mensagens, regras ou processos
- 👀 Acompanhar o andamento das solicitações

Sempre que possível, problemas e melhorias devem virar **issues no repositório da automação correspondente**, evitando que pedidos importantes se percam em mensagens soltas.

<br>

## 🐛 Como abrir uma issue

Ao encontrar um problema ou sugerir uma melhoria, procure o repositório da automação relacionada e abra uma issue usando o modelo disponível, respondendo sempre que possível:

- [ ] O que aconteceu?
- [ ] O que deveria ter acontecido?
- [ ] Em qual automação isso ocorreu?
- [ ] Quando o problema aconteceu?
- [ ] Existe algum print, link, mensagem ou exemplo?
- [ ] Isso impede o uso da automação ou é apenas uma melhoria?

> Quanto mais contexto a issue tiver, mais fácil será entender, priorizar e resolver.

<br>

## 📈 Como organizar melhorias

As melhorias das automações são acompanhadas dentro dos próprios repositórios. Isso ajuda o time a entender:

- O que já foi feito
- O que está em andamento
- O que ainda precisa ser analisado
- Quais problemas são recorrentes
- Quais automações precisam de mais atenção

O GitHub funciona como o **histórico operacional** da automação — não é só um lugar para guardar arquivos, é onde a evolução fica registrada.

<br>

## ✅ Boas práticas para documentar automações

Ao criar ou atualizar um repositório, mantenha estas informações claras:

<table>
<tr><td>

- Nome da automação
- Objetivo principal
- Área que usa a automação
- Responsável técnico ou time responsável
- Como a automação é acionada

</td><td>

- Quais ferramentas ela usa
- Quais dados ela lê ou atualiza
- Quais regras de negócio são importantes
- Como testar se está funcionando
- O que fazer em caso de erro

</td></tr>
</table>

Evite documentações longas demais. O ideal é que qualquer pessoa consiga abrir o README e entender rapidamente:

> **o que é isso, para que serve e como usar.**

<br>

## 🔒 Segurança

> [!WARNING]
> Nunca coloque nos repositórios:
> - Tokens
> - Senhas
> - Chaves de API
> - Arquivos `.env`
> - Credenciais do n8n
> - Dados sensíveis de alunos, leads, clientes ou colaboradores
> - Exports de workflows com credenciais embutidas

Sempre que uma automação precisar de variáveis de ambiente, use um arquivo de exemplo:

```txt
.env.example
```

Esse arquivo deve mostrar **quais** variáveis são necessárias, mas nunca deve conter valores reais.

<br>

## 🚀 Para quem está chegando agora

1. **Entenda** quais repositórios você tem acesso
2. **Leia** o README do repositório da automação que você vai usar
3. **Veja** se existem issues abertas relacionadas à sua área
4. **Use** os modelos de issue para reportar problemas ou sugerir melhorias
5. **Em caso de dúvida**, mencione o time responsável dentro da própria issue

<br>

---

<div align="center">

## 📝 Em resumo

A **Asimov Academy Automations** existe para transformar automações internas em sistemas bem documentados, versionados e fáceis de manter.

**Aqui ficam:** contexto · regras · decisões · problemas · melhorias · documentação · evolução

<br>

**Menos conhecimento perdido. Mais clareza para quem usa. Mais controle para quem mantém.**

</div>

---

<div align="center">
<sub>Mantido pelo time da Asimov Academy 💜</sub>
</div>
