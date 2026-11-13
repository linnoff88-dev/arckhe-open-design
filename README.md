# Open Design

> **A alternativa open-source ao [Claude Design][cd].** Local-first, implantÃ¡vel na web, BYOK em todas as camadas â€” **11 CLIs de agentes de codificaÃ§Ã£o** detectados automaticamente no seu `PATH` (Claude Code, Codex, Cursor Agent, Gemini CLI, OpenCode, Qwen, GitHub Copilot CLI, Hermes, Kimi, Pi, Kiro) tornam-se o motor de design, conduzidos por **31 Skills componÃ­veis** e **72 Design Systems de qualidade de marca**. Sem CLI? Um proxy BYOK compatÃ­vel com OpenAI executa o mesmo loop, dispensando o spawn.

<p align="center">
  <img src="assets/img/opendesign.png" alt="Open Design â€” capa editorial: design com o agente no seu laptop" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/nexu-io/open-design/stargazers"><img alt="Stars" src="https://img.shields.io/github/stars/nexu-io/open-design?style=for-the-badge&labelColor=0d1117&color=ffd700&logo=github&logoColor=white" /></a>
  <a href="https://github.com/nexu-io/open-design/network/members"><img alt="Forks" src="https://img.shields.io/github/forks/nexu-io/open-design?style=for-the-badge&labelColor=0d1117&color=2ecc71&logo=github&logoColor=white" /></a>
  <a href="https://github.com/nexu-io/open-design/issues"><img alt="Issues" src="https://img.shields.io/github/issues/nexu-io/open-design?style=for-the-badge&labelColor=0d1117&color=ff6b6b&logo=github&logoColor=white" /></a>
  <a href="https://github.com/nexu-io/open-design/pulls"><img alt="Pull Requests" src="https://img.shields.io/github/issues-pr/nexu-io/open-design?style=for-the-badge&labelColor=0d1117&color=9b59b6&logo=github&logoColor=white" /></a>
  <a href="https://github.com/nexu-io/open-design/graphs/contributors"><img alt="Contributors" src="https://img.shields.io/github/contributors/nexu-io/open-design?style=for-the-badge&labelColor=0d1117&color=3498db&logo=github&logoColor=white" /></a>
  <a href="https://github.com/nexu-io/open-design/commits/main"><img alt="Commit activity" src="https://img.shields.io/github/commit-activity/m/nexu-io/open-design?style=for-the-badge&labelColor=0d1117&color=e67e22&logo=git&logoColor=white" /></a>
  <a href="https://github.com/nexu-io/open-design/commits/main"><img alt="Last commit" src="https://img.shields.io/github/last-commit/nexu-io/open-design?style=for-the-badge&labelColor=0d1117&color=8e44ad&logo=git&logoColor=white" /></a>
</p>

<p align="center">
  <a href="https://github.com/nexu-io/open-design/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/nexu-io/open-design?style=flat-square&color=blueviolet&label=release&include_prereleases" /></a>
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/badge/license-Apache%202.0-blue.svg?style=flat-square" /></a>
  <a href="#agentes-de-codificacao-suportados"><img alt="Agents" src="https://img.shields.io/badge/agents-10%20CLIs%20%2B%20BYOK%20proxy-black?style=flat-square" /></a>
  <a href="#design-systems"><img alt="Design systems" src="https://img.shields.io/badge/design%20systems-72-orange?style=flat-square" /></a>
  <a href="#skills"><img alt="Skills" src="https://img.shields.io/badge/skills-31-teal?style=flat-square" /></a>
  <a href="QUICKSTART.md"><img alt="Quickstart" src="https://img.shields.io/badge/quickstart-3%20commands-green?style=flat-square" /></a>
</p>

<p align="center"><a href="README.en.md">English</a> Â· <a href="README.de.md">Deutsch</a> Â· <a href="README.zh-CN.md">ç®€ä½“ä¸­æ–‡</a> Â· <a href="README.zh-TW.md">ç¹é«”ä¸­æ–‡</a> Â· <a href="README.ko.md">í•œêµ­ì–´</a> Â· <a href="README.ja-JP.md">æ—¥æœ¬èªž</a> Â· <b>PortuguÃªs (BR)</b></p>

---

## Por que isto existe

O [Claude Design][cd] da Anthropic (lanÃ§ado em 2026-04-17, Opus 4.7) mostrou o que acontece quando um LLM para de escrever prosa e comeÃ§a a entregar artefatos de design. Viralizou â€” e permaneceu de cÃ³digo fechado, pago, apenas na nuvem, preso ao modelo da Anthropic e Ã s skills da Anthropic. NÃ£o hÃ¡ checkout, nÃ£o hÃ¡ self-host, nÃ£o hÃ¡ deploy na Vercel, nÃ£o hÃ¡ troca por seu prÃ³prio agente.

**Open Design (OD) Ã© a alternativa open-source.** Mesmo loop, mesmo modelo mental artifact-first, nada do lock-in. NÃ£o enviamos um agente â€” os agentes de codificaÃ§Ã£o mais fortes jÃ¡ vivem no seu laptop. NÃ³s os conectamos a um fluxo de design orientado por skills que roda localmente com `pnpm tools-dev`, pode implantar a camada web na Vercel, e permanece BYOK em todas as camadas.

Digite `crie um pitch deck estilo revista para nossa rodada seed`. O formulÃ¡rio de perguntas interativo aparece antes que o modelo improvise um Ãºnico pixel. O agente escolhe uma de cinco direÃ§Ãµes visuais curadas. Um plano `TodoWrite` ao vivo Ã© transmitido para a UI. O daemon constrÃ³i uma pasta de projeto real em disco com um template seed, biblioteca de layouts e checklist de auto-verificaÃ§Ã£o. O agente os lÃª â€” pre-flight aplicado â€” executa uma crÃ­tica de cinco dimensÃµes contra a sua prÃ³pria saÃ­da, e emite um Ãºnico `<artifact>` que renderiza em um iframe sandboxed segundos depois.

Isso nÃ£o Ã© "IA tentando desenhar algo". Ã‰ uma IA que foi treinada, pela stack de prompts, a se comportar como uma designer sÃªnior com um sistema de arquivos funcional, uma biblioteca determinÃ­stica de paletas e uma cultura de checklist â€” exatamente o nÃ­vel que o Claude Design estabeleceu, mas aberto e seu.

OD se apoia em quatro ombros open-source:

- [**`alchaincyf/huashu-design`**](https://github.com/alchaincyf/huashu-design) â€” a bÃºssola da filosofia de design. Workflow Junior-Designer, o protocolo de 5 passos para ativos de marca, o checklist anti-AI-slop, a auto-crÃ­tica de 5 dimensÃµes, e a ideia "5 escolas Ã— 20 filosofias de design" por trÃ¡s do nosso seletor de direÃ§Ãµes â€” tudo destilado em [`apps/web/src/prompts/discovery.ts`](apps/web/src/prompts/discovery.ts).
- [**`op7418/guizang-ppt-skill`**](https://github.com/op7418/guizang-ppt-skill) â€” o modo deck. Empacotado verbatim em [`skills/guizang-ppt/`](skills/guizang-ppt/) com a LICENSE original preservada; layouts estilo revista, hero WebGL, checklists P0/P1/P2.
- [**`OpenCoworkAI/open-codesign`**](https://github.com/OpenCoworkAI/open-codesign) â€” a estrela-guia de UX e nosso par mais prÃ³ximo. A primeira alternativa open-source ao Claude Design. Pegamos emprestado seu loop de streaming-artifact, seu padrÃ£o de preview em iframe sandboxed (React 18 + Babel vendorizado), seu painel de agente ao vivo (todos + chamadas de ferramenta + geraÃ§Ã£o interrompÃ­vel), e sua lista de exportaÃ§Ã£o em cinco formatos (HTML / PDF / PPTX / ZIP / Markdown). Divergimos deliberadamente no formato â€” eles sÃ£o um app desktop Electron empacotando [`pi-ai`][piai]; nÃ³s somos um web app + daemon local que delega para sua CLI existente.
- [**`multica-ai/multica`**](https://github.com/multica-ai/multica) â€” a arquitetura daemon-and-runtime. DetecÃ§Ã£o de agentes via PATH-scan, o daemon local como o Ãºnico processo privilegiado, a visÃ£o de mundo agente-como-companheiro-de-equipe.

## VisÃ£o geral

| | O que vocÃª ganha |
|---|---|
| **CLIs de agente de codificaÃ§Ã£o (11)** | Claude Code Â· Codex CLI Â· Cursor Agent Â· Gemini CLI Â· OpenCode Â· Qwen Code Â· GitHub Copilot CLI Â· Hermes (ACP) Â· Kimi CLI (ACP) Â· Pi (RPC) Â· Kiro CLI (ACP) â€” detectados automaticamente no `PATH`, troque com um clique |
| **Fallback BYOK** | Proxy compatÃ­vel com OpenAI em `/api/proxy/stream` â€” cole `baseUrl` + `apiKey` + `model` e qualquer fornecedor (Anthropic-via-OpenAI, DeepSeek, Groq, MiMo, OpenRouter, seu vLLM auto-hospedado, ou qualquer outro provedor compatÃ­vel com OpenAI) torna-se o motor. IPs internos/SSRF bloqueados na borda do daemon. |
| **Design systems integrados** | **129** â€” 2 starters escritos Ã  mÃ£o + 70 sistemas de produtos (Linear, Stripe, Vercel, Airbnb, Tesla, Notion, Anthropic, Apple, Cursor, Supabase, Figma, Xiaohongshu, â€¦) de [`awesome-design-md`][acd2], mais 57 design skills de [`awesome-design-skills`][ads] adicionadas diretamente em `design-systems/` |
| **Skills integradas** | **31** â€” 27 no modo `prototype` (web-prototype, saas-landing, dashboard, mobile-app, gamified-app, social-carousel, magazine-poster, dating-web, sprite-animation, motion-frames, critique, tweaks, wireframe-sketch, pm-spec, eng-runbook, finance-report, hr-onboarding, invoice, kanban-board, team-okrs, â€¦) + 4 no modo `deck` (`guizang-ppt` Â· `simple-deck` Â· `replit-deck` Â· `weekly-update`). Agrupadas no seletor por `scenario`: design / marketing / operation / engineering / product / finance / hr / sale / personal. |
| **DireÃ§Ãµes visuais** | 5 escolas curadas (Editorial Monocle Â· Modern Minimal Â· Warm Soft Â· Tech Utility Â· Brutalist Experimental) â€” cada uma traz uma paleta OKLch determinÃ­stica + font stack ([`apps/web/src/prompts/directions.ts`](apps/web/src/prompts/directions.ts)) |
| **Frames de dispositivo** | iPhone 15 Pro Â· Pixel Â· iPad Pro Â· MacBook Â· Browser Chrome â€” pixel-accurate, compartilhados entre skills em [`assets/frames/`](assets/frames/) |
| **Runtime do agente** | O daemon local faz spawn da CLI na pasta do seu projeto â€” o agente recebe `Read`, `Write`, `Bash`, `WebFetch` reais contra um ambiente real em disco, com fallbacks para `ENAMETOOLONG` no Windows (stdin / arquivo de prompt) em todo adapter |
| **ImportaÃ§Ãµes** | Solte um ZIP de exportaÃ§Ã£o do [Claude Design][cd] no diÃ¡logo de boas-vindas â€” `POST /api/import/claude-design` o decompÃµe em um projeto real para que seu agente continue editando de onde a Anthropic parou |
| **PersistÃªncia** | SQLite em `.od/app.sqlite`: projetos Â· conversas Â· mensagens Â· abas Â· templates salvos. Reabra amanhÃ£, o card de todo e os arquivos abertos estÃ£o exatamente onde vocÃª deixou. |
| **Lifecycle** | Um Ãºnico ponto de entrada: `pnpm tools-dev` (start / stop / run / status / logs / inspect / check) â€” inicializa daemon + web (+ desktop) sob stamps de sidecar tipados |
| **Desktop** | Shell Electron opcional com renderer sandboxed + IPC de sidecar (STATUS / EVAL / SCREENSHOT / CONSOLE / CLICK / SHUTDOWN) â€” alimenta `tools-dev inspect desktop screenshot` para E2E |
| **ImplantÃ¡vel em** | Local (`pnpm tools-dev`) Â· camada web na Vercel Â· Electron empacotado (placeholder, em andamento) |
| **LicenÃ§a** | Apache-2.0 |

[acd2]: https://github.com/VoltAgent/awesome-design-md
[ads]: https://github.com/bergside/awesome-design-skills

## Demo

<table>
<tr>
<td width="50%">
<img src="docs/screenshots/01-entry-view.png" alt="01 Â· Tela de entrada" /><br/>
<sub><b>Tela de entrada</b> â€” escolha uma skill, escolha um design system, digite o brief. A mesma superfÃ­cie para protÃ³tipos, decks, apps mobile, dashboards e pÃ¡ginas editoriais.</sub>
</td>
<td width="50%">
<img src="docs/screenshots/02-question-form.png" alt="02 Â· FormulÃ¡rio de descoberta do turno 1" /><br/>
<sub><b>FormulÃ¡rio de descoberta do turno 1</b> â€” antes que o modelo escreva um pixel, o OD trava o brief: superfÃ­cie, audiÃªncia, tom, contexto de marca, escala. 30 segundos de radios derrotam 30 minutos de redirecionamentos.</sub>
</td>
</tr>
<tr>
<td width="50%">
<img src="docs/screenshots/03-direction-picker.png" alt="03 Â· Seletor de direÃ§Ãµes" /><br/>
<sub><b>Seletor de direÃ§Ãµes</b> â€” quando o usuÃ¡rio nÃ£o tem marca, o agente emite um segundo formulÃ¡rio com 5 direÃ§Ãµes curadas (Monocle / Modern Minimal / Tech Utility / Brutalist / Soft Warm). Um clique no radio â†’ uma paleta + font stack determinÃ­sticos, sem freestyle do modelo.</sub>
</td>
<td width="50%">
<img src="docs/screenshots/04-todo-progress.png" alt="04 Â· Progresso de todos ao vivo" /><br/>
<sub><b>Progresso de todos ao vivo</b> â€” o plano do agente Ã© transmitido como um card ao vivo. AtualizaÃ§Ãµes de <code>in_progress</code> â†’ <code>completed</code> chegam em tempo real. O usuÃ¡rio pode redirecionar barato, em pleno voo.</sub>
</td>
</tr>
<tr>
<td width="50%">
<img src="docs/screenshots/05-preview-iframe.png" alt="05 Â· Preview sandboxed" /><br/>
<sub><b>Preview sandboxed</b> â€” todo <code>&lt;artifact&gt;</code> renderiza em um iframe srcdoc limpo. EditÃ¡vel no local via o workspace de arquivos; baixÃ¡vel como HTML, PDF, ZIP.</sub>
</td>
<td width="50%">
<img src="docs/screenshots/06-design-systems-library.png" alt="06 Â· Biblioteca de 72 sistemas" /><br/>
<sub><b>Biblioteca de 72 sistemas</b> â€” todo sistema de produto mostra sua assinatura de 4 cores. Clique para o <code>DESIGN.md</code> completo, grid de swatches e showcase ao vivo.</sub>
</td>
</tr>
<tr>
<td width="50%">
<img src="docs/screenshots/07-magazine-deck.png" alt="07 Â· Deck estilo revista" /><br/>
<sub><b>Modo deck (guizang-ppt)</b> â€” o <a href="https://github.com/op7418/guizang-ppt-skill"><code>guizang-ppt-skill</code></a> empacotado entra inalterado. Layouts de revista, fundos hero WebGL, saÃ­da HTML em arquivo Ãºnico, exportaÃ§Ã£o PDF.</sub>
</td>
<td width="50%">
<img src="docs/screenshots/08-mobile-app.png" alt="08 Â· ProtÃ³tipo mobile" /><br/>
<sub><b>ProtÃ³tipo mobile</b> â€” chrome do iPhone 15 Pro pixel-accurate (Dynamic Island, SVGs da status bar, indicador de home). ProtÃ³tipos multi-tela usam os ativos compartilhados de <code>/frames/</code> para que o agente nunca redesenhe um celular.</sub>
</td>
</tr>
</table>

## Skills

**31 skills vÃªm na caixa.** Cada uma Ã© uma pasta em [`skills/`](skills/) seguindo a convenÃ§Ã£o [`SKILL.md`][skill] do Claude Code com um frontmatter `od:` estendido que o daemon parseia verbatim â€” `mode`, `platform`, `scenario`, `preview.type`, `design_system.requires`, `default_for`, `featured`, `fidelity`, `speaker_notes`, `animations`, `example_prompt` ([`apps/daemon/src/skills.ts`](apps/daemon/src/skills.ts)).

Dois **modos** de topo carregam o catÃ¡logo: **`prototype`** (27 skills â€” qualquer coisa que renderize como um artefato de pÃ¡gina Ãºnica, de uma landing de revista a uma tela de celular ou um documento de spec de PM) e **`deck`** (4 skills â€” apresentaÃ§Ãµes com swipe horizontal e chrome de framework de deck). O campo **`scenario`** Ã© por onde o seletor as agrupa: `design` Â· `marketing` Â· `operation` Â· `engineering` Â· `product` Â· `finance` Â· `hr` Â· `sale` Â· `personal`.

### Exemplos do showcase

As skills visualmente mais distintivas que vocÃª provavelmente vai rodar primeiro. Cada uma traz um `example.html` real que vocÃª pode abrir direto do repo para ver exatamente o que o agente vai produzir â€” sem auth, sem setup.

<table>
<tr>
<td width="50%" valign="top">
<a href="skills/dating-web/"><img src="docs/screenshots/skills/dating-web.png" alt="dating-web" /></a><br/>
<sub><b><a href="skills/dating-web/"><code>dating-web</code></a></b> Â· <i>prototype</i><br/>Dashboard de namoro / matchmaking â€” nav lateral Ã  esquerda, ticker bar, KPIs, grÃ¡fico de matches mÃºtuos de 30 dias, tipografia editorial.</sub>
</td>
<td width="50%" valign="top">
<a href="skills/digital-eguide/"><img src="docs/screenshots/skills/digital-eguide.png" alt="digital-eguide" /></a><br/>
<sub><b><a href="skills/digital-eguide/"><code>digital-eguide</code></a></b> Â· <i>template</i><br/>E-guia digital de duas spreads â€” capa (tÃ­tulo, autor, prÃ©via do TOC) + spread de aula com pull-quote e lista de passos. Tom criador / lifestyle.</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="skills/email-marketing/"><img src="docs/screenshots/skills/email-marketing.png" alt="email-marketing" /></a><br/>
<sub><b><a href="skills/email-marketing/"><code>email-marketing</code></a></b> Â· <i>prototype</i><br/>E-mail HTML de lanÃ§amento de produto da marca â€” masthead, imagem hero, lockup do tÃ­tulo, CTA, grid de specs. Coluna Ãºnica centralizada, com fallback de tabela seguro.</sub>
</td>
<td width="50%" valign="top">
<a href="skills/gamified-app/"><img src="docs/screenshots/skills/gamified-app.png" alt="gamified-app" /></a><br/>
<sub><b><a href="skills/gamified-app/"><code>gamified-app</code></a></b> Â· <i>prototype</i><br/>ProtÃ³tipo de mobile-app gamificado em trÃªs frames sobre um stage escuro de showcase â€” capa, missÃµes do dia com fitas de XP + barra de nÃ­vel, detalhe da missÃ£o.</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="skills/mobile-onboarding/"><img src="docs/screenshots/skills/mobile-onboarding.png" alt="mobile-onboarding" /></a><br/>
<sub><b><a href="skills/mobile-onboarding/"><code>mobile-onboarding</code></a></b> Â· <i>prototype</i><br/>Fluxo de onboarding mobile em trÃªs frames â€” splash, value-prop, sign-in. Status bar, dots de swipe, CTA primÃ¡rio.</sub>
</td>
<td width="50%" valign="top">
<a href="skills/motion-frames/"><img src="docs/screenshots/skills/motion-frames.png" alt="motion-frames" /></a><br/>
<sub><b><a href="skills/motion-frames/"><code>motion-frames</code></a></b> Â· <i>prototype</i><br/>Hero de motion design em frame Ãºnico com animaÃ§Ãµes CSS em loop â€” anel de tipo rotacionando, globo animado, timer pulsando. Pronto para hand-off para HyperFrames.</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="skills/social-carousel/"><img src="docs/screenshots/skills/social-carousel.png" alt="social-carousel" /></a><br/>
<sub><b><a href="skills/social-carousel/"><code>social-carousel</code></a></b> Â· <i>prototype</i><br/>Carrossel de social media 1080Ã—1080 em trÃªs cards â€” painÃ©is cinematogrÃ¡ficos com tÃ­tulos display que se conectam ao longo da sÃ©rie, logo da marca, indicaÃ§Ã£o de loop.</sub>
</td>
<td width="50%" valign="top">
<a href="skills/sprite-animation/"><img src="docs/screenshots/skills/sprite-animation.png" alt="sprite-animation" /></a><br/>
<sub><b><a href="skills/sprite-animation/"><code>sprite-animation</code></a></b> Â· <i>prototype</i><br/>Slide explicador animado pixel / 8-bit â€” stage cream full-bleed, mascote pixel animado, tipo display kinÃ©tico japonÃªs, keyframes CSS em loop.</sub>
</td>
</tr>
</table>

### SuperfÃ­cies de design & marketing (modo prototype)

| Skill | Plataforma | CenÃ¡rio | O que produz |
|---|---|---|---|
| [`web-prototype`](skills/web-prototype/) | desktop | design | HTML de pÃ¡gina Ãºnica â€” landings, marketing, hero pages (default para prototype) |
| [`saas-landing`](skills/saas-landing/) | desktop | marketing | Layout de marketing com hero / features / pricing / CTA |
| [`dashboard`](skills/dashboard/) | desktop | operation | Admin / analytics com sidebar + layout de dados denso |
| [`pricing-page`](skills/pricing-page/) | desktop | sale | Tabelas de pricing + comparaÃ§Ã£o standalone |
| [`docs-page`](skills/docs-page/) | desktop | engineering | Layout de documentaÃ§Ã£o em 3 colunas |
| [`blog-post`](skills/blog-post/) | desktop | marketing | Long-form editorial |
| [`mobile-app`](skills/mobile-app/) | mobile | design | Tela(s) de app emolduradas em iPhone 15 Pro / Pixel |
| [`mobile-onboarding`](skills/mobile-onboarding/) | mobile | design | Fluxo de onboarding mobile multi-tela (splash Â· value-prop Â· sign-in) |
| [`gamified-app`](skills/gamified-app/) | mobile | personal | ProtÃ³tipo de mobile-app gamificado em trÃªs frames |
| [`email-marketing`](skills/email-marketing/) | desktop | marketing | E-mail HTML de lanÃ§amento de produto (com fallback de tabela seguro) |
| [`social-carousel`](skills/social-carousel/) | desktop | marketing | Carrossel social de 3 cards 1080Ã—1080 |
| [`magazine-poster`](skills/magazine-poster/) | desktop | marketing | Poster de pÃ¡gina Ãºnica estilo revista |
| [`motion-frames`](skills/motion-frames/) | desktop | marketing | Hero de motion design com animaÃ§Ãµes CSS em loop |
| [`sprite-animation`](skills/sprite-animation/) | desktop | marketing | Slide explicador animado pixel / 8-bit |
| [`dating-web`](skills/dating-web/) | desktop | personal | Mockup de dashboard de namoro |
| [`digital-eguide`](skills/digital-eguide/) | desktop | marketing | E-guia digital em duas spreads (capa + aula) |
| [`wireframe-sketch`](skills/wireframe-sketch/) | desktop | design | Sketch de ideaÃ§Ã£o desenhado Ã  mÃ£o â€” para o passo "mostre algo visÃ­vel cedo" |
| [`critique`](skills/critique/) | desktop | design | Folha de auto-crÃ­tica de cinco dimensÃµes (Filosofia Â· Hierarquia Â· Detalhe Â· FunÃ§Ã£o Â· InovaÃ§Ã£o) |
| [`tweaks`](skills/tweaks/) | desktop | design | Painel de tweaks emitidos pela IA â€” o modelo levanta os parÃ¢metros que valem a pena ajustar |

### SuperfÃ­cies de deck (modo deck)

| Skill | Default para | O que produz |
|---|---|---|
| [`guizang-ppt`](skills/guizang-ppt/) | **default** para deck | Web PPT estilo revista â€” empacotado verbatim de [op7418/guizang-ppt-skill][guizang], LICENSE original preservada |
| [`simple-deck`](skills/simple-deck/) | â€” | Deck minimalista de swipe horizontal |
| [`replit-deck`](skills/replit-deck/) | â€” | Deck de walkthrough de produto (estilo Replit) |
| [`weekly-update`](skills/weekly-update/) | â€” | CadÃªncia semanal de equipe como deck de swipe (progresso Â· blockers Â· prÃ³ximos) |

### SuperfÃ­cies de office & operaÃ§Ãµes (modo prototype, cenÃ¡rios flavor de documento)

| Skill | CenÃ¡rio | O que produz |
|---|---|---|
| [`pm-spec`](skills/pm-spec/) | product | Doc de especificaÃ§Ã£o de PM com TOC + log de decisÃµes |
| [`team-okrs`](skills/team-okrs/) | product | Folha de pontuaÃ§Ã£o de OKRs |
| [`meeting-notes`](skills/meeting-notes/) | operation | Log de decisÃµes de reuniÃ£o |
| [`kanban-board`](skills/kanban-board/) | operation | Snapshot de board |
| [`eng-runbook`](skills/eng-runbook/) | engineering | Runbook de incidentes |
| [`finance-report`](skills/finance-report/) | finance | SumÃ¡rio executivo financeiro |
| [`invoice`](skills/invoice/) | finance | Fatura de pÃ¡gina Ãºnica |
| [`hr-onboarding`](skills/hr-onboarding/) | hr | Plano de onboarding de cargo |

Adicionar uma skill exige uma pasta. Leia [`docs/skills-protocol.md`](docs/skills-protocol.md) para o frontmatter estendido, faÃ§a fork de uma skill existente, reinicie o daemon, ela aparece no seletor. O endpoint do catÃ¡logo Ã© `GET /api/skills`; a montagem de seed por skill (template + referÃªncias de side-files) vive em `GET /api/skills/:id/example`.

## Seis ideias estruturais

### 1 Â· NÃ£o enviamos um agente. O seu jÃ¡ basta.

O daemon escaneia seu `PATH` em busca de [`claude`](https://docs.anthropic.com/en/docs/claude-code), [`codex`](https://github.com/openai/codex), [`cursor-agent`](https://www.cursor.com/cli), [`gemini`](https://github.com/google-gemini/gemini-cli), [`opencode`](https://opencode.ai/), [`qwen`](https://github.com/QwenLM/qwen-code), [`copilot`](https://github.com/features/copilot/cli), `hermes`, `kimi`, [`pi`](https://github.com/mariozechner/pi-ai), e [`kiro-cli`](https://kiro.dev) na inicializaÃ§Ã£o. Aqueles que ele encontra tornam-se motores de design candidatos â€” conduzidos por stdio com um adapter por CLI, intercambiÃ¡veis a partir do seletor de modelo. Inspirado por [`multica`](https://github.com/multica-ai/multica) e [`cc-switch`](https://github.com/farion1231/cc-switch). Sem CLI instalada? `POST /api/proxy/stream` Ã© o mesmo pipeline sem o spawn â€” cole qualquer `baseUrl` + `apiKey` compatÃ­vel com OpenAI e o daemon encaminha os chunks SSE de volta, com destinos loopback / link-local / RFC1918 rejeitados na borda.

### 2 Â· Skills sÃ£o arquivos, nÃ£o plugins.

Seguindo a [convenÃ§Ã£o `SKILL.md`](https://docs.anthropic.com/en/docs/claude-code/skills) do Claude Code, cada skill Ã© `SKILL.md` + `assets/` + `references/`. Solte uma pasta em [`skills/`](skills/), reinicie o daemon, ela aparece no seletor. O `magazine-web-ppt` empacotado Ã© o [`op7418/guizang-ppt-skill`](https://github.com/op7418/guizang-ppt-skill) commitado verbatim â€” licenÃ§a original preservada, atribuiÃ§Ã£o preservada.

### 3 Â· Design Systems sÃ£o Markdown portÃ¡til, nÃ£o JSON de tema.

O schema de 9 seÃ§Ãµes `DESIGN.md` de [`VoltAgent/awesome-design-md`][acd2] â€” cor, tipografia, espaÃ§amento, layout, componentes, motion, voz, marca, anti-padrÃµes. Todo artefato lÃª do sistema ativo. Troque o sistema â†’ o prÃ³ximo render usa os novos tokens. O dropdown vem com **Linear, Stripe, Vercel, Airbnb, Tesla, Notion, Apple, Anthropic, Cursor, Supabase, Figma, Resend, Raycast, Lovable, Cohere, Mistral, ElevenLabs, X.AI, Spotify, Webflow, Sanity, PostHog, Sentry, MongoDB, ClickHouse, Cal, Replicate, Clay, Composio, Xiaohongshuâ€¦** â€” mais 57 design skills vindas de [`awesome-design-skills`][ads].

### 4 Â· O formulÃ¡rio de perguntas interativo previne 80% dos redirecionamentos.

A stack de prompts do OD codifica uma `RULE 1`: todo brief de design fresco comeÃ§a com um `<question-form id="discovery">` em vez de cÃ³digo. SuperfÃ­cie Â· audiÃªncia Â· tom Â· contexto de marca Â· escala Â· restriÃ§Ãµes. Um brief longo ainda deixa decisÃµes de design em aberto â€” tom visual, postura de cor, escala â€” exatamente as coisas que o formulÃ¡rio trava em 30 segundos. O custo de uma direÃ§Ã£o errada Ã© uma rodada de chat, nÃ£o um deck terminado.

Este Ã© o **modo Junior-Designer** destilado de [`huashu-design`](https://github.com/alchaincyf/huashu-design): faÃ§a as perguntas em batch upfront, mostre algo visÃ­vel cedo (mesmo um wireframe com blocos cinzas), permita que o usuÃ¡rio redirecione barato. Combinado com o protocolo de ativos de marca (localizar Â· baixar Â· `grep` hex Â· escrever `brand-spec.md` Â· vocalizar), Ã© a maior razÃ£o Ãºnica pela qual a saÃ­da deixa de parecer freestyle de IA e passa a parecer uma designer que prestou atenÃ§Ã£o antes de pintar.

### 5 Â· O daemon faz o agente parecer estar no seu laptop, porque estÃ¡.

O daemon faz spawn da CLI com `cwd` definido para a pasta de artefatos do projeto sob `.od/projects/<id>/`. O agente recebe `Read`, `Write`, `Bash`, `WebFetch` â€” ferramentas reais contra um sistema de arquivos real. Ele pode `Read` no `assets/template.html` da skill, `grep` no seu CSS por valores hex, escrever um `brand-spec.md`, soltar imagens geradas, e produzir arquivos `.pptx` / `.zip` / `.pdf` que aparecem no workspace de arquivos como chips de download quando a turn termina. SessÃµes, conversas, mensagens, abas persistem em um DB SQLite local â€” abra o projeto amanhÃ£ e o card de todo do agente estÃ¡ exatamente onde vocÃª deixou.

### 6 Â· A stack de prompts Ã© o produto.

O que vocÃª compÃµe na hora do envio nÃ£o Ã© "system + user". Ã‰:

```
DISCOVERY directives  (formulÃ¡rio do turn-1, branch de marca do turn-2, TodoWrite, crÃ­tica de 5 dimensÃµes)
  + identity charter   (OFFICIAL_DESIGNER_PROMPT, anti-AI-slop, junior-pass)
  + DESIGN.md ativo    (72 sistemas disponÃ­veis)
  + SKILL.md ativo     (31 skills disponÃ­veis)
  + metadata do projeto (kind, fidelity, speakerNotes, animations, ids de inspiraÃ§Ã£o)
  + side files da skill (auto-injetados em pre-flight: ler assets/template.html + references/*.md)
  + (deck kind, sem seed de skill) DECK_FRAMEWORK_DIRECTIVE   (nav / counter / scroll / print)
```

Cada camada Ã© componÃ­vel. Cada camada Ã© um arquivo que vocÃª pode editar. Leia [`apps/web/src/prompts/system.ts`](apps/web/src/prompts/system.ts) e [`apps/web/src/prompts/discovery.ts`](apps/web/src/prompts/discovery.ts) para ver o contrato real.

## Arquitetura

```
â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€ browser (Next.js 16) â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
â”‚  chat Â· workspace de arquivos Â· preview iframe Â· settings Â· imports â”‚
â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
               â”‚ /api/* (reescrito em dev)          â”‚
               â–¼                                    â–¼
   â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”   /api/proxy/stream (SSE)
   â”‚  Daemon local (Express + SQLite) â”‚   â”€â†’ qualquer endpoint
   â”‚                                  â”‚       compatÃ­vel com OpenAI (BYOK)
   â”‚  /api/agents          /api/skillsâ”‚       com bloqueio SSRF
   â”‚  /api/design-systems  /api/projects/â€¦
   â”‚  /api/chat (SSE)      /api/proxy/stream (SSE)
   â”‚  /api/templates       /api/import/claude-design
   â”‚  /api/artifacts/save  /api/artifacts/lint
   â”‚  /api/upload          /api/projects/:id/filesâ€¦
   â”‚  /artifacts (static)  /frames (static)
   â”‚
   â”‚  opcional: IPC de sidecar em /tmp/open-design/ipc/<ns>/<app>.sock
   â”‚  (STATUS Â· EVAL Â· SCREENSHOT Â· CONSOLE Â· CLICK Â· SHUTDOWN)
   â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
             â”‚ spawn(cli, [...], { cwd: .od/projects/<id> })
             â–¼
   â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
   â”‚  claude Â· codex Â· gemini Â· opencode Â· cursor-agent Â· qwen        â”‚
   â”‚  copilot Â· hermes (ACP) Â· kimi (ACP) Â· pi (RPC) Â· kiro (ACP)      â”‚
   â”‚  lÃª SKILL.md + DESIGN.md, escreve artefatos no disco             â”‚
   â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
```

| Camada | Stack |
|---|---|
| Frontend | Next.js 16 App Router + React 18 + TypeScript, deployable na Vercel |
| Daemon | Node 24 Â· Express Â· streaming SSE Â· `better-sqlite3`; tabelas: `projects` Â· `conversations` Â· `messages` Â· `tabs` Â· `templates` |
| Transporte do agente | `child_process.spawn`; parsers de eventos tipados para `claude-stream-json` (Claude Code), `copilot-stream-json` (Copilot), parsers `json-event-stream` por CLI (Codex / Gemini / OpenCode / Cursor Agent), `acp-json-rpc` (Hermes / Kimi / Kiro via Agent Client Protocol), `pi-rpc` (Pi via JSON-RPC stdio), `plain` (Qwen Code) |
| Proxy BYOK | `POST /api/proxy/stream` â†’ `/v1/chat/completions` compatÃ­vel com OpenAI, pass-through SSE; rejeita hosts loopback / link-local / RFC1918 na borda do daemon |
| Storage | Arquivos planos em `.od/projects/<id>/` + SQLite em `.od/app.sqlite` (gitignored, auto-criado). Sobreponha a raiz com `OD_DATA_DIR` para isolamento de testes |
| Preview | Iframe sandboxed via `srcdoc` + parser `<artifact>` por skill ([`apps/web/src/artifacts/parser.ts`](apps/web/src/artifacts/parser.ts)) |
| Export | HTML (assets inline) Â· PDF (impressÃ£o do browser, deck-aware) Â· PPTX (orientado pelo agente via skill) Â· ZIP (archiver) Â· Markdown |
| Lifecycle | `pnpm tools-dev start \| stop \| run \| status \| logs \| inspect \| check`; portas via `--daemon-port` / `--web-port`, namespaces via `--namespace` |
| Desktop (opcional) | Shell Electron â€” descobre a URL web via IPC de sidecar, sem adivinhar portas; o mesmo canal `STATUS`/`EVAL`/`SCREENSHOT`/`CONSOLE`/`CLICK`/`SHUTDOWN` alimenta `tools-dev inspect desktop â€¦` para E2E |

## Quickstart

```bash
git clone https://github.com/nexu-io/open-design.git
cd open-design
corepack enable
corepack pnpm --version   # deve imprimir 10.33.2
pnpm install
pnpm tools-dev run web
# abra a URL web impressa pelo tools-dev
```

Requisitos de ambiente: Node `~24` e pnpm `10.33.x`. `nvm`/`fnm` sÃ£o ajudantes opcionais; se vocÃª usar um, rode `nvm install 24 && nvm use 24` ou `fnm install 24 && fnm use 24` antes de `pnpm install`.

Para inicializaÃ§Ã£o desktop/background, restarts em portas fixas e checagens do dispatcher de geraÃ§Ã£o de mÃ­dia (`OD_BIN`, `OD_DAEMON_URL`, `apps/daemon/dist/cli.js`), veja [`QUICKSTART.md`](QUICKSTART.md).

A primeira carga:

1. Detecta quais CLIs de agente vocÃª tem no `PATH` e escolhe uma automaticamente.
2. Carrega 31 skills + 72 design systems.
3. Abre o diÃ¡logo de boas-vindas para vocÃª colar uma chave Anthropic (necessÃ¡ria apenas para o caminho de fallback BYOK).
4. **Auto-cria `./.od/`** â€” a pasta de runtime local para o DB SQLite de projetos, artefatos por projeto e renders salvos. NÃ£o hÃ¡ passo `od init`; o daemon faz `mkdir` em tudo que precisa no boot.

Digite um prompt, aperte **Send**, observe o formulÃ¡rio de perguntas chegar, preencha-o, observe o card de todo fluir, observe o artefato renderizar. Clique em **Save to disk** ou baixe como um ZIP do projeto.

### Estado de primeira execuÃ§Ã£o (`./.od/`)

O daemon possui uma pasta oculta na raiz do repo. Tudo nela Ã© gitignored e local da mÃ¡quina â€” nunca faÃ§a commit.

```
.od/
â”œâ”€â”€ app.sqlite                 â† projetos Â· conversas Â· mensagens Â· abas abertas
â”œâ”€â”€ artifacts/                 â† renders pontuais "Save to disk" (com timestamp)
â””â”€â”€ projects/<id>/             â† diretÃ³rio de trabalho por projeto, tambÃ©m o cwd do agente
```

| Querâ€¦ | FaÃ§a isso |
|---|---|
| Inspecionar o que estÃ¡ lÃ¡ | `ls -la .od && sqlite3 .od/app.sqlite '.tables'` |
| Resetar para um estado limpo | `pnpm tools-dev stop`, `rm -rf .od`, rode `pnpm tools-dev run web` novamente |
| MovÃª-lo para outro lugar | ainda nÃ£o suportado â€” o caminho Ã© hard-coded relativo ao repo |

Mapa completo de arquivos, scripts e troubleshooting â†’ [`QUICKSTART.md`](QUICKSTART.md).

## Como usar (interface web)

O Open Design Ã© **local-first**: nÃ£o existe SaaS hospedado. VocÃª roda na sua mÃ¡quina e acessa pelo navegador. TrÃªs cenÃ¡rios cobrem 99% dos usos.

### 1 Â· Modo "duplo-clique" (recomendado para usuÃ¡rio final)

Depois de `pnpm install` uma vez, use os scripts auxiliares na raiz do repo:

```bash
./start.sh    # sobe daemon + web (portas fixas) e abre o navegador
./stop.sh     # para tudo
```

Portas padrÃ£o: daemon `17456`, web `17573`. Sobreponha com env vars: `OD_DAEMON_PORT=18000 OD_WEB_PORT=18001 ./start.sh`.

URL: **http://localhost:17573** (abre automaticamente se vocÃª tem `xdg-open` ou `open`).

### 2 Â· Comando manual (controle fino)

```bash
cd open-design
pnpm install                                              # uma vez
pnpm tools-dev run web --daemon-port 17456 --web-port 17573
```

Abra **http://localhost:17573**. Para parar: `pnpm tools-dev stop`. Para inspecionar:

```bash
pnpm tools-dev status --json
pnpm tools-dev logs --json
pnpm tools-dev check
```

### 3 Â· App desktop (Electron, sem terminal aberto)

```bash
pnpm tools-dev                       # sobe daemon + web + desktop juntos
```

Uma janela nativa abre apontando para a web local. Fechando a janela, tudo morre junto. Em ambiente GUI, valide com:

```bash
pnpm tools-dev inspect desktop status
pnpm tools-dev inspect desktop screenshot --path /tmp/od.png
```

Pacote `.app` (macOS beta): `pnpm tools-pack build` â†’ `pnpm tools-pack start`.

### Self-host em servidor remoto (avanÃ§ado)

Tecnicamente possÃ­vel, nÃ£o suportado oficialmente: rode `pnpm tools-dev run web` numa VM/VPS e acesse via port-forward SSH ou reverse proxy com TLS + auth prÃ³prios. **Avisos:**

- O daemon assume que vocÃª Ã© dono da mÃ¡quina â€” ele faz `spawn` de CLIs de agente e escreve em `.od/projects/`.
- Sem auth nativa na UI. Adicione uma camada (nginx basic-auth, Cloudflare Access, Tailscale) antes de expor.
- A camada web (Next.js) pode ir para Vercel; o daemon precisa de filesystem real + CLIs de agente instaladas.

### Fluxo tÃ­pico de uso

1. Suba o serviÃ§o (cenÃ¡rio 1, 2 ou 3 acima).
2. Abra a URL web no navegador.
3. Cole sua chave de modelo (Anthropic, OpenAI, ou qualquer endpoint BYOK compatÃ­vel com OpenAI) no diÃ¡logo de boas-vindas. **Sem chave?** Se vocÃª jÃ¡ tem `claude`, `codex`, `gemini`, `cursor-agent`, etc. no `PATH`, o daemon detecta e usa direto.
4. Crie um projeto, escolha uma skill (ex.: `web-prototype`, `guizang-ppt`, `dashboard`) e um design system (ex.: `linear-app`, `stripe`, `warm-editorial`).
5. Digite o brief. Responda o formulÃ¡rio de descoberta do turn 1 (30s de radios).
6. Veja o todo plan streamando ao vivo e o artefato renderizar no iframe.
7. Baixe como HTML / PDF / ZIP, ou salve como template reutilizÃ¡vel.

### NÃ£o existe (intencionalmente)

- VersÃ£o SaaS hospedada por terceiros.
- Conta / login / multi-tenancy.
- CLI puro headless sem daemon â€” o bin `od` Ã© parte do daemon, nÃ£o roda standalone.

Tudo Ã© local-first por design: vocÃª Ã© dono do `.od/`, dos artefatos, das chaves de modelo e do agente que conduz o loop.

## Estrutura do repositÃ³rio

```
open-design/
â”œâ”€â”€ README.md                      â† este arquivo (em inglÃªs)
â”œâ”€â”€ README.de.md                   â† Deutsch
â”œâ”€â”€ README.zh-CN.md                â† ç®€ä½“ä¸­æ–‡
â”œâ”€â”€ README.pt-BR.md                â† PortuguÃªs (Brasil)
â”œâ”€â”€ QUICKSTART.md                  â† guia de run / build / deploy
â”œâ”€â”€ package.json                   â† workspace pnpm, Ãºnico bin: od
â”‚
â”œâ”€â”€ apps/
â”‚   â”œâ”€â”€ daemon/                    â† Node + Express, o Ãºnico servidor
â”‚   â”‚   â”œâ”€â”€ src/                   â† fonte TypeScript do daemon
â”‚   â”‚   â”‚   â”œâ”€â”€ cli.ts             â† fonte do bin `od`, compilado para dist/cli.js
â”‚   â”‚   â”‚   â”œâ”€â”€ server.ts          â† rotas /api/* (projetos, chat, arquivos, exports)
â”‚   â”‚   â”‚   â”œâ”€â”€ agents.ts          â† scanner de PATH + builders de argv por CLI
â”‚   â”‚   â”‚   â”œâ”€â”€ claude-stream.ts   â† parser de JSON em streaming para stdout do Claude Code
â”‚   â”‚   â”‚   â”œâ”€â”€ skills.ts          â† loader do frontmatter SKILL.md
â”‚   â”‚   â”‚   â””â”€â”€ db.ts              â† schema SQLite (projects/messages/templates/tabs)
â”‚   â”‚   â”œâ”€â”€ sidecar/               â† wrapper de sidecar do daemon para tools-dev
â”‚   â”‚   â””â”€â”€ tests/                 â† testes do pacote daemon
â”‚   â”‚
â”‚   â””â”€â”€ web/                       â† cliente Next.js 16 App Router + React
â”‚       â”œâ”€â”€ app/                   â† entrypoints do App Router
â”‚       â”œâ”€â”€ next.config.ts         â† rewrites de dev + export estÃ¡tico prod para out/
â”‚       â””â”€â”€ src/                   â† mÃ³dulos cliente React + TypeScript
â”‚           â”œâ”€â”€ App.tsx            â† roteamento, bootstrap, settings
â”‚           â”œâ”€â”€ components/        â† chat, composer, picker, preview, sketch, â€¦
â”‚           â”œâ”€â”€ prompts/
â”‚           â”‚   â”œâ”€â”€ system.ts      â† composeSystemPrompt(base, skill, DS, metadata)
â”‚           â”‚   â”œâ”€â”€ discovery.ts   â† formulÃ¡rio do turn-1 + branch do turn-2 + crÃ­tica 5-dim
â”‚           â”‚   â””â”€â”€ directions.ts  â† 5 direÃ§Ãµes visuais Ã— paleta OKLch + font stack
â”‚           â”œâ”€â”€ artifacts/         â† parser de <artifact> em streaming + manifests
â”‚           â”œâ”€â”€ runtime/           â† srcdoc do iframe, markdown, helpers de export
â”‚           â”œâ”€â”€ providers/         â† transports de SSE do daemon + API BYOK
â”‚           â””â”€â”€ state/             â† config + projetos (localStorage + daemon-backed)
â”‚
â”œâ”€â”€ e2e/                           â† Playwright UI + harness de integraÃ§Ã£o externa/Vitest
â”‚
â”œâ”€â”€ packages/
â”‚   â”œâ”€â”€ contracts/                 â† contratos compartilhados de app web/daemon
â”‚   â”œâ”€â”€ sidecar-proto/             â† contrato de protocolo de sidecar do Open Design
â”‚   â”œâ”€â”€ sidecar/                   â† primitivos genÃ©ricos de runtime de sidecar
â”‚   â””â”€â”€ platform/                  â† primitivos genÃ©ricos de processo/plataforma
â”‚
â”œâ”€â”€ skills/                        â† 31 bundles de skill SKILL.md (27 prototype + 4 deck)
â”‚   â”œâ”€â”€ web-prototype/             â† default para modo prototype
â”‚   â”œâ”€â”€ saas-landing/  dashboard/  pricing-page/  docs-page/  blog-post/
â”‚   â”œâ”€â”€ mobile-app/  mobile-onboarding/  gamified-app/
â”‚   â”œâ”€â”€ email-marketing/  social-carousel/  magazine-poster/
â”‚   â”œâ”€â”€ motion-frames/  sprite-animation/  digital-eguide/  dating-web/
â”‚   â”œâ”€â”€ critique/  tweaks/  wireframe-sketch/
â”‚   â”œâ”€â”€ pm-spec/  team-okrs/  meeting-notes/  kanban-board/
â”‚   â”œâ”€â”€ eng-runbook/  finance-report/  invoice/  hr-onboarding/
â”‚   â”œâ”€â”€ simple-deck/  replit-deck/  weekly-update/   â† modo deck
â”‚   â””â”€â”€ guizang-ppt/               â† magazine-web-ppt empacotado (default para deck)
â”‚       â”œâ”€â”€ SKILL.md
â”‚       â”œâ”€â”€ assets/template.html   â† seed
â”‚       â””â”€â”€ references/{themes,layouts,components,checklist}.md
â”‚
â”œâ”€â”€ design-systems/                â† 72 sistemas DESIGN.md
â”‚   â”œâ”€â”€ default/                   â† Neutral Modern (starter)
â”‚   â”œâ”€â”€ warm-editorial/            â† Warm Editorial (starter)
â”‚   â”œâ”€â”€ linear-app/  vercel/  stripe/  airbnb/  notion/  cursor/  apple/  â€¦
â”‚   â””â”€â”€ README.md                  â† visÃ£o geral do catÃ¡logo
â”‚
â”œâ”€â”€ assets/
â”‚   â””â”€â”€ frames/                    â† frames de dispositivo compartilhados (uso cross-skill)
â”‚       â”œâ”€â”€ iphone-15-pro.html
â”‚       â”œâ”€â”€ android-pixel.html
â”‚       â”œâ”€â”€ ipad-pro.html
â”‚       â”œâ”€â”€ macbook.html
â”‚       â””â”€â”€ browser-chrome.html
â”‚
â”œâ”€â”€ templates/
â”‚   â””â”€â”€ deck-framework.html        â† baseline de deck (nav / counter / print)
â”‚
â”œâ”€â”€ scripts/
â”‚   â””â”€â”€ sync-design-systems.ts     â† reimporta o tarball upstream awesome-design-md
â”‚
â”œâ”€â”€ docs/
â”‚   â”œâ”€â”€ spec.md                    â† spec do produto, cenÃ¡rios, diferenciaÃ§Ã£o
â”‚   â”œâ”€â”€ architecture.md            â† topologias, fluxo de dados, componentes
â”‚   â”œâ”€â”€ skills-protocol.md         â† frontmatter od: estendido do SKILL.md
â”‚   â”œâ”€â”€ agent-adapters.md          â† detecÃ§Ã£o + dispatch por CLI
â”‚   â”œâ”€â”€ modes.md                   â† prototype / deck / template / design-system
â”‚   â”œâ”€â”€ references.md              â† procedÃªncia long-form
â”‚   â”œâ”€â”€ roadmap.md                 â† entrega em fases
â”‚   â”œâ”€â”€ schemas/                   â† schemas JSON
â”‚   â””â”€â”€ examples/                  â† exemplos canÃ´nicos de artefatos
â”‚
â””â”€â”€ .od/                           â† dados de runtime, gitignored, auto-criado
    â”œâ”€â”€ app.sqlite                 â† projetos / conversas / mensagens / abas
    â”œâ”€â”€ projects/<id>/             â† pasta de trabalho por projeto (cwd do agente)
    â””â”€â”€ artifacts/                 â† renders pontuais salvos
```

## Design Systems

<p align="center">
  <img src="docs/assets/design-systems-library.png" alt="A biblioteca de 72 design systems â€” spread de style guide" width="100%" />
</p>

72 sistemas na caixa, cada um como um Ãºnico [`DESIGN.md`](design-systems/README.md):

<details>
<summary><b>CatÃ¡logo completo</b> (clique para expandir)</summary>

**AI & LLM** â€” `claude` Â· `cohere` Â· `mistral-ai` Â· `minimax` Â· `together-ai` Â· `replicate` Â· `runwayml` Â· `elevenlabs` Â· `ollama` Â· `x-ai`

**Developer Tools** â€” `cursor` Â· `vercel` Â· `linear-app` Â· `framer` Â· `expo` Â· `clickhouse` Â· `mongodb` Â· `supabase` Â· `hashicorp` Â· `posthog` Â· `sentry` Â· `warp` Â· `webflow` Â· `sanity` Â· `mintlify` Â· `lovable` Â· `composio` Â· `opencode-ai` Â· `voltagent`

**Productivity** â€” `notion` Â· `figma` Â· `miro` Â· `airtable` Â· `superhuman` Â· `intercom` Â· `zapier` Â· `cal` Â· `clay` Â· `raycast`

**Fintech** â€” `stripe` Â· `coinbase` Â· `binance` Â· `kraken` Â· `mastercard` Â· `revolut` Â· `wise`

**E-Commerce** â€” `shopify` Â· `airbnb` Â· `uber` Â· `nike` Â· `starbucks` Â· `pinterest`

**Media** â€” `spotify` Â· `playstation` Â· `wired` Â· `theverge` Â· `meta`

**Automotive** â€” `tesla` Â· `bmw` Â· `ferrari` Â· `lamborghini` Â· `bugatti` Â· `renault`

**Other** â€” `apple` Â· `ibm` Â· `nvidia` Â· `vodafone` Â· `sentry` Â· `resend` Â· `spacex`

**Starters** â€” `default` (Neutral Modern) Â· `warm-editorial`

</details>

A biblioteca de sistemas de produto Ã© importada via [`scripts/sync-design-systems.ts`](scripts/sync-design-systems.ts) de [`VoltAgent/awesome-design-md`][acd2]. Rode novamente para atualizar. As 57 design skills vÃªm de [`bergside/awesome-design-skills`][ads] e sÃ£o adicionadas diretamente em `design-systems/`.

## DireÃ§Ãµes visuais

Quando o usuÃ¡rio nÃ£o tem brand spec, o agente emite um segundo formulÃ¡rio com cinco direÃ§Ãµes curadas â€” a adaptaÃ§Ã£o OD do [fallback "5 escolas Ã— 20 filosofias de design" de `huashu-design`](https://github.com/alchaincyf/huashu-design#%E8%AE%BE%E8%AE%A1%E6%96%B9%E5%90%91%E9%A1%BE%E9%97%AE-fallback). Cada direÃ§Ã£o Ã© uma spec determinÃ­stica â€” paleta em OKLch, font stack, sinais de postura de layout, referÃªncias â€” que o agente vincula verbatim no `:root` do template seed. Um clique no radio â†’ um sistema visual completamente especificado. Sem improvisaÃ§Ã£o, sem AI-slop.

| DireÃ§Ã£o | Mood | Refs |
|---|---|---|
| Editorial â€” Monocle / FT | Revista impressa, tinta + cream + ferrugem quente | Monocle Â· FT Weekend Â· NYT Magazine |
| Modern minimal â€” Linear / Vercel | Frio, estruturado, accent mÃ­nimo | Linear Â· Vercel Â· Stripe |
| Tech utility | Densidade de informaÃ§Ã£o, monospace, terminal | Bloomberg Â· ferramentas Bauhaus |
| Brutalist | Cru, tipo oversized, sem sombras, accents Ã¡speros | Bloomberg Businessweek Â· Achtung |
| Soft warm | Generoso, baixo contraste, neutros pÃªssego | Notion marketing Â· Apple Health |

Spec completa â†’ [`apps/web/src/prompts/directions.ts`](apps/web/src/prompts/directions.ts).

## AlÃ©m do chat â€” o que mais vem incluÃ­do

O loop de chat / artefato pega o destaque, mas vÃ¡rias capacidades menos visÃ­veis jÃ¡ estÃ£o conectadas e valem ser conhecidas antes de comparar OD com qualquer outra coisa:

- **ImportaÃ§Ã£o de ZIP do Claude Design.** Solte uma exportaÃ§Ã£o de claude.ai no diÃ¡logo de boas-vindas. `POST /api/import/claude-design` extrai em um real `.od/projects/<id>/`, abre o arquivo de entrada como aba, e prepara um prompt continue-de-onde-a-Anthropic-parou para seu agente local. Sem re-prompting, sem "peÃ§a ao modelo para recriar o que acabamos de ter". ([`apps/daemon/src/server.ts`](apps/daemon/src/server.ts) â€” `/api/import/claude-design`)
- **Proxy BYOK compatÃ­vel com OpenAI.** `POST /api/proxy/stream` aceita `{ baseUrl, apiKey, model, messages }`, normaliza o caminho (`â€¦/v1/chat/completions`), encaminha chunks SSE de volta ao browser, e rejeita destinos loopback / link-local / RFC1918 para evitar SSRF. Qualquer coisa que fale o schema chat OpenAI funciona â€” shim Anthropic-via-OpenAI, DeepSeek, Groq, MiMo, OpenRouter, seu vLLM auto-hospedado. MiMo recebe `tool_choice: 'none'` automaticamente porque seu schema de tools se comporta mal em geraÃ§Ã£o free-form.
- **Templates salvos pelo usuÃ¡rio.** Uma vez que vocÃª gosta de um render, `POST /api/templates` faz snapshot do HTML + metadata na tabela `templates` do SQLite. O prÃ³ximo projeto o escolhe a partir de uma linha "your templates" no seletor â€” mesma superfÃ­cie que as 31 enviadas, mas suas.
- **PersistÃªncia de abas.** Todo projeto lembra seus arquivos abertos e a aba ativa na tabela `tabs`. Reabra o projeto amanhÃ£ e o workspace fica exatamente do jeito que vocÃª deixou.
- **API de lint de artefatos.** `POST /api/artifacts/lint` roda checagens estruturais em um artefato gerado (framing `<artifact>` quebrado, side files obrigatÃ³rios faltando, tokens de paleta velhos) e retorna findings que o agente pode ler de volta no prÃ³ximo turn. A auto-crÃ­tica de cinco dimensÃµes usa isso para fundamentar sua pontuaÃ§Ã£o em evidÃªncia real, nÃ£o vibes.
- **Protocolo de sidecar + automaÃ§Ã£o desktop.** Processos daemon, web e desktop carregam stamps tipados de cinco campos (`app Â· mode Â· namespace Â· ipc Â· source`) e expÃµem um canal IPC JSON-RPC em `/tmp/open-design/ipc/<namespace>/<app>.sock`. `tools-dev inspect desktop status \| eval \| screenshot` dirige esse canal, entÃ£o E2E headless funciona contra um shell Electron real sem harnesses sob medida ([`packages/sidecar-proto/`](packages/sidecar-proto/), [`apps/desktop/src/main/`](apps/desktop/src/main/)).
- **Spawning Windows-friendly.** Todo adapter que de outra forma estouraria o limite ~32 KB de argv de `CreateProcess` em prompts compostos longos (Codex, Gemini, OpenCode, Cursor Agent, Qwen, Pi) alimenta o prompt via stdin. Claude Code e Copilot mantÃªm `-p`; o daemon faz fallback para um arquivo de prompt temporÃ¡rio quando atÃ© isso transborda.
- **Dados de runtime por namespace.** `OD_DATA_DIR` e `--namespace` te dÃ£o Ã¡rvores `.od/` totalmente isoladas, entÃ£o Playwright, canais beta e seus projetos reais nunca compartilham um arquivo SQLite.

## MaquinÃ¡rio anti-AI-slop

Todo o maquinÃ¡rio abaixo Ã© o playbook de [`huashu-design`](https://github.com/alchaincyf/huashu-design), portado para a stack de prompts do OD e tornado aplicÃ¡vel por skill via o pre-flight de side files. Leia [`apps/web/src/prompts/discovery.ts`](apps/web/src/prompts/discovery.ts) para o fraseado vivo:

- **FormulÃ¡rio de perguntas primeiro.** O turn 1 Ã© apenas `<question-form>` â€” sem thinking, sem ferramentas, sem narraÃ§Ã£o. O usuÃ¡rio escolhe defaults na velocidade do radio.
- **ExtraÃ§Ã£o de brand-spec.** Quando o usuÃ¡rio anexa um screenshot ou URL, o agente roda um protocolo de cinco passos (localizar Â· baixar Â· grep hex Â· codificar `brand-spec.md` Â· vocalizar) antes de escrever CSS. **Nunca adivinha cores de marca da memÃ³ria.**
- **CrÃ­tica 5-dim.** Antes de emitir `<artifact>`, o agente pontua silenciosamente sua saÃ­da de 1â€“5 em filosofia / hierarquia / execuÃ§Ã£o / especificidade / contenÃ§Ã£o. Qualquer coisa abaixo de 3/5 Ã© uma regressÃ£o â€” corrige e re-pontua. Dois passes Ã© normal.
- **Checklist P0/P1/P2.** Toda skill envia um `references/checklist.md` com gates P0 rÃ­gidos. O agente deve passar P0 antes de emitir.
- **Blacklist de slop.** Gradientes roxos agressivos, Ã­cones emoji genÃ©ricos, card arredondado com accent de borda esquerda, humanos SVG desenhados Ã  mÃ£o, Inter como face *display*, mÃ©tricas inventadas â€” explicitamente proibidos no prompt.
- **Placeholders honestos > stats falsos.** Quando o agente nÃ£o tem um nÃºmero real, ele escreve `â€”` ou um bloco cinza rotulado, nÃ£o "10Ã— mais rÃ¡pido".

## ComparaÃ§Ã£o

| Eixo | [Claude Design][cd] (Anthropic) | [Open CoDesign][ocod] | **Open Design** |
|---|---|---|---|
| LicenÃ§a | Fechada | MIT | **Apache-2.0** |
| Form factor | Web (claude.ai) | Desktop (Electron) | **App web + daemon local** |
| ImplantÃ¡vel na Vercel | âŒ | âŒ | **âœ…** |
| Runtime do agente | Empacotado (Opus 4.7) | Empacotado ([`pi-ai`][piai]) | **Delegado para a CLI existente do usuÃ¡rio** |
| Skills | ProprietÃ¡rias | 12 mÃ³dulos TS customizados + `SKILL.md` | **31 bundles [`SKILL.md`][skill] baseados em arquivo, soltÃ¡veis** |
| Design system | ProprietÃ¡rio | `DESIGN.md` (roadmap v0.2) | **`DESIGN.md` Ã— 129 sistemas enviados** |
| Flexibilidade de provider | Apenas Anthropic | 7+ via [`pi-ai`][piai] | **10 adapters de CLI + proxy BYOK compatÃ­vel com OpenAI** |
| FormulÃ¡rio de perguntas inicial | âŒ | âŒ | **âœ… Regra rÃ­gida, turn 1** |
| Seletor de direÃ§Ãµes | âŒ | âŒ | **âœ… 5 direÃ§Ãµes determinÃ­sticas** |
| Progresso de todos ao vivo + stream de tools | âŒ | âœ… | **âœ…** (padrÃ£o UX de open-codesign) |
| Preview iframe sandboxed | âŒ | âœ… | **âœ…** (padrÃ£o de open-codesign) |
| ImportaÃ§Ã£o de ZIP do Claude Design | n/a | âŒ | **âœ… `POST /api/import/claude-design` â€” continue editando de onde a Anthropic parou** |
| EdiÃ§Ãµes cirÃºrgicas em modo comentÃ¡rio | âŒ | âœ… | ðŸš§ roadmap (lift de open-codesign) |
| Painel de tweaks emitidos pela IA | âŒ | âœ… | ðŸŸ¡ parcial â€” a [skill `tweaks`](skills/tweaks/) Ã© enviada, UX de painel dedicado lateral ao chat ainda no roadmap |
| Workspace nÃ­vel-filesystem | âŒ | parcial (sandbox Electron) | **âœ… cwd real, ferramentas reais, SQLite persistido (projects Â· conversations Â· messages Â· tabs Â· templates)** |
| Auto-crÃ­tica 5-dim | âŒ | âŒ | **âœ… Gate pre-emit** |
| Lint de artefatos | âŒ | âŒ | **âœ… `POST /api/artifacts/lint` â€” findings retornados ao agente** |
| IPC de sidecar + desktop headless | âŒ | âŒ | **âœ… Processos com stamp + `tools-dev inspect desktop status \| eval \| screenshot`** |
| Formatos de export | Limitado | HTML / PDF / PPTX / ZIP / Markdown | **HTML / PDF / PPTX (orientado pelo agente) / ZIP / Markdown** |
| Reuso de skill PPT | N/A | Built-in | **[`guizang-ppt-skill`][guizang] entra (default para modo deck)** |
| CobranÃ§a mÃ­nima | Pro / Max / Team | BYOK | **BYOK â€” cole qualquer `baseUrl` compatÃ­vel com OpenAI** |

[cd]: https://x.com/claudeai/status/2045156267690213649
[ocod]: https://github.com/OpenCoworkAI/open-codesign
[piai]: https://github.com/mariozechner/pi-ai
[acd]: https://github.com/VoltAgent/awesome-claude-design
[guizang]: https://github.com/op7418/guizang-ppt-skill
[skill]: https://docs.anthropic.com/en/docs/claude-code/skills

## Agentes de codificaÃ§Ã£o suportados

Detectados automaticamente do `PATH` no boot do daemon. Sem config necessÃ¡ria. O dispatch de streaming vive em [`apps/daemon/src/agents.ts`](apps/daemon/src/agents.ts) (`AGENT_DEFS`); parsers por CLI vivem ao lado dele. Modelos sÃ£o populados ou por probing `<bin> --list-models` / `<bin> models` / handshake ACP, ou de uma lista de fallback curada quando a CLI nÃ£o expÃµe uma lista.

| Agente | Bin | Formato de stream | Forma do argv (caminho de prompt composto) |
|---|---|---|---|
| [Claude Code](https://docs.anthropic.com/en/docs/claude-code) | `claude` | `claude-stream-json` (eventos tipados) | `claude -p <prompt> --output-format stream-json --verbose [--include-partial-messages] [--add-dir â€¦] --permission-mode bypassPermissions` |
| [Codex CLI](https://github.com/openai/codex) | `codex` | `json-event-stream` + parser `codex` | `codex exec --json --skip-git-repo-check --full-auto [-C cwd] [--model â€¦] [-c model_reasoning_effort=â€¦] -` (prompt no stdin) |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli) | `gemini` | `json-event-stream` + parser `gemini` | `gemini --output-format stream-json --skip-trust --yolo [--model â€¦] -` (prompt no stdin) |
| [OpenCode](https://opencode.ai/) | `opencode` | `json-event-stream` + parser `opencode` | `opencode run --format json --dangerously-skip-permissions [--model â€¦] -` (prompt no stdin) |
| [Cursor Agent](https://www.cursor.com/cli) | `cursor-agent` | `json-event-stream` + parser `cursor-agent` | `cursor-agent --print --output-format stream-json --stream-partial-output --force --trust [--workspace cwd] [--model â€¦] -` (prompt no stdin) |
| [Qwen Code](https://github.com/QwenLM/qwen-code) | `qwen` | `plain` (chunks brutos do stdout) | `qwen --yolo [--model â€¦] -` (prompt no stdin) |
| [GitHub Copilot CLI](https://github.com/features/copilot/cli) | `copilot` | `copilot-stream-json` (eventos tipados) | `copilot -p <prompt> --allow-all-tools --output-format json [--model â€¦] [--add-dir â€¦]` |
| [Hermes](https://github.com/eqlabs/hermes) | `hermes` | `acp-json-rpc` (Agent Client Protocol) | `hermes acp --accept-hooks` |
| Kimi CLI | `kimi` | `acp-json-rpc` | `kimi acp` |
| [Kiro CLI](https://kiro.dev) | `kiro-cli` | `acp-json-rpc` | `kiro-cli acp` |
| [Pi](https://github.com/mariozechner/pi-ai) | `pi` | `pi-rpc` (JSON-RPC stdio) | `pi --mode rpc --no-session [--model â€¦] [--thinking â€¦]` (prompt enviado como comando RPC `prompt`) |
| **BYOK compatÃ­vel com OpenAI** | n/a | Pass-through SSE | `POST /api/proxy/stream` â†’ `<baseUrl>/v1/chat/completions`; SSRF-guarded contra loopback / link-local / RFC1918 |

Adicionar uma nova CLI Ã© uma entrada em [`apps/daemon/src/agents.ts`](apps/daemon/src/agents.ts). O formato de streaming Ã© um de `claude-stream-json`, `copilot-stream-json`, `json-event-stream` (com um `eventParser` por CLI), `acp-json-rpc`, `pi-rpc`, ou `plain`.

## ReferÃªncias & linhagem

Todo projeto externo do qual este repo toma emprestado. Cada link vai para a fonte para que vocÃª possa verificar a procedÃªncia.

| Projeto | Papel aqui |
|---|---|
| [`Claude Design`][cd] | O produto de cÃ³digo fechado para o qual este repo Ã© a alternativa open-source. |
| [**`alchaincyf/huashu-design`**](https://github.com/alchaincyf/huashu-design) | O nÃºcleo da filosofia de design. Workflow Junior-Designer, o protocolo de 5 passos para ativos de marca, checklist anti-AI-slop, auto-crÃ­tica de 5 dimensÃµes e a biblioteca "5 escolas Ã— 20 filosofias de design" por trÃ¡s do nosso seletor de direÃ§Ãµes â€” tudo destilado em [`apps/web/src/prompts/discovery.ts`](apps/web/src/prompts/discovery.ts) e [`apps/web/src/prompts/directions.ts`](apps/web/src/prompts/directions.ts). |
| [**`op7418/guizang-ppt-skill`**][guizang] | Skill magazine-web-PPT empacotada verbatim em [`skills/guizang-ppt/`](skills/guizang-ppt/) com a LICENSE original preservada. Default para modo deck. Cultura de checklist P0/P1/P2 emprestada para toda outra skill. |
| [**`multica-ai/multica`**](https://github.com/multica-ai/multica) | A arquitetura daemon + adapter. DetecÃ§Ã£o de agentes via PATH-scan, daemon local como o Ãºnico processo privilegiado, visÃ£o de mundo agente-como-companheiro-de-equipe. Adotamos o modelo; nÃ£o vendorizamos o cÃ³digo. |
| [**`OpenCoworkAI/open-codesign`**][ocod] | A primeira alternativa open-source ao Claude Design e nosso par mais prÃ³ximo. PadrÃµes de UX adotados: loop de streaming-artifact, preview iframe sandboxed (React 18 + Babel vendorizados), painel de agente ao vivo (todos + chamadas de tool + interrompÃ­vel), lista de export em cinco formatos (HTML/PDF/PPTX/ZIP/Markdown), hub de storage local-first, taste-injection via `SKILL.md`. PadrÃµes de UX no nosso roadmap: ediÃ§Ãµes cirÃºrgicas em modo comentÃ¡rio, painel de tweaks emitidos pela IA. **Deliberadamente nÃ£o vendorizamos [`pi-ai`][piai]** â€” open-codesign o empacota como o runtime do agente; nÃ³s delegamos para qualquer CLI que o usuÃ¡rio jÃ¡ tenha. |
| [`VoltAgent/awesome-claude-design`][acd] / [`awesome-design-md`][acd2] | Fonte do schema `DESIGN.md` de 9 seÃ§Ãµes e dos 70 sistemas de produto importados via [`scripts/sync-design-systems.ts`](scripts/sync-design-systems.ts). |
| [`bergside/awesome-design-skills`][ads] | Fonte das 57 design skills adicionadas diretamente como arquivos `DESIGN.md` normalizados em `design-systems/`. |
| [`farion1231/cc-switch`](https://github.com/farion1231/cc-switch) | InspiraÃ§Ã£o para distribuiÃ§Ã£o de skills baseada em symlinks atravÃ©s de vÃ¡rias CLIs de agente. |
| [Skills do Claude Code][skill] | A convenÃ§Ã£o `SKILL.md` adotada verbatim â€” qualquer skill do Claude Code entra em `skills/` e Ã© pega pelo daemon. |

Texto de procedÃªncia long-form â€” o que tomamos de cada um, o que deliberadamente nÃ£o tomamos â€” vive em [`docs/references.md`](docs/references.md).

## Roadmap

- [x] Daemon + detecÃ§Ã£o de agente (10 adapters de CLI) + registro de skills + catÃ¡logo de design system
- [x] App web + chat + formulÃ¡rio de perguntas + seletor de 5 direÃ§Ãµes + progresso de todos + preview sandboxed
- [x] 31 skills + 72 design systems + 5 direÃ§Ãµes visuais + 5 frames de dispositivo
- [x] Projetos backed por SQLite Â· conversas Â· mensagens Â· abas Â· templates
- [x] Proxy BYOK compatÃ­vel com OpenAI (`/api/proxy/stream`) com guard SSRF
- [x] ImportaÃ§Ã£o de ZIP do Claude Design (`/api/import/claude-design`)
- [x] Protocolo de sidecar + desktop Electron com automaÃ§Ã£o IPC (STATUS / EVAL / SCREENSHOT / CONSOLE / CLICK / SHUTDOWN)
- [x] API de lint de artefatos + gate pre-emit de auto-crÃ­tica 5-dim
- [ ] EdiÃ§Ãµes cirÃºrgicas em modo comentÃ¡rio (clique no elemento â†’ instruÃ§Ã£o â†’ patch) â€” padrÃ£o de [`open-codesign`][ocod]
- [ ] UX do painel de tweaks emitidos pela IA â€” building block ([skill `tweaks`](skills/tweaks/)) Ã© enviado; painel integrado ao chat ainda pendente
- [ ] Receita de deployment Vercel + tunnel (Topologia B)
- [ ] `npx od init` em um comando para esqueletar um projeto com `DESIGN.md`
- [ ] Marketplace de skills (`od skills install <github-repo>`) e superfÃ­cie CLI `od skill add | list | remove | test` (rascunhada em [`docs/skills-protocol.md`](docs/skills-protocol.md), implementaÃ§Ã£o pendente)
- [ ] Build Electron empacotado a partir de `apps/packaged/`

Entrega em fases â†’ [`docs/roadmap.md`](docs/roadmap.md).

## Status

Esta Ã© uma implementaÃ§Ã£o inicial â€” o loop fechado (detectar â†’ escolher skill + design system â†’ chat â†’ parsear `<artifact>` â†’ preview â†’ salvar) roda end-to-end. A stack de prompts e a biblioteca de skills Ã© onde a maior parte do valor vive, e elas sÃ£o estÃ¡veis. A UI a nÃ­vel de componente Ã© enviada diariamente.

## DÃª uma estrela

<p align="center">
  <a href="https://github.com/nexu-io/open-design"><img src="docs/assets/star-us.png" alt="Star Open Design no GitHub â€” github.com/nexu-io/open-design" width="100%" /></a>
</p>

Se isto te economizou trinta minutos â€” dÃª uma â˜…. Estrelas nÃ£o pagam aluguel, mas dizem para o prÃ³ximo designer, agente e contribuidor que este experimento merece sua atenÃ§Ã£o. Um clique, trÃªs segundos, sinal real: [github.com/nexu-io/open-design](https://github.com/nexu-io/open-design).

## Contribuindo

Issues, PRs, novas skills e novos design systems sÃ£o todos bem-vindos. As contribuiÃ§Ãµes de maior alavancagem geralmente sÃ£o uma pasta, um arquivo Markdown ou um adapter do tamanho de um PR:

- **Adicione uma skill** â€” solte uma pasta em [`skills/`](skills/) seguindo a convenÃ§Ã£o [`SKILL.md`][skill].
- **Adicione um design system** â€” solte um `DESIGN.md` em [`design-systems/<brand>/`](design-systems/) usando o schema de 9 seÃ§Ãµes.
- **Conecte uma nova CLI de agente de codificaÃ§Ã£o** â€” uma entrada em [`apps/daemon/src/agents.ts`](apps/daemon/src/agents.ts).

Walkthrough completo, barra para merge, estilo de cÃ³digo e o que nÃ£o aceitamos â†’ [`CONTRIBUTING.md`](CONTRIBUTING.md) ([Deutsch](CONTRIBUTING.de.md), [ç®€ä½“ä¸­æ–‡](CONTRIBUTING.zh-CN.md)).

## Contribuidores

Obrigado a todos que ajudaram a mover Open Design adiante â€” atravÃ©s de cÃ³digo, docs, feedback, novas skills, novos design systems, ou atÃ© uma issue afiada. Toda contribuiÃ§Ã£o real conta, e o mural abaixo Ã© a forma mais fÃ¡cil de dizer isso em alto e bom som.

<a href="https://github.com/nexu-io/open-design/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=nexu-io/open-design&cache_bust=2026-04-30" alt="Contribuidores Open Design" />
</a>

Se vocÃª enviou seu primeiro PR â€” bem-vindo. A label [`good-first-issue`](https://github.com/nexu-io/open-design/labels/good-first-issue) Ã© o ponto de entrada.

## Atividade do repositÃ³rio

<picture>
  <img alt="Open Design â€” mÃ©tricas do repositÃ³rio" src="docs/assets/github-metrics.svg" />
</picture>

O SVG acima Ã© regenerado diariamente por [`.github/workflows/metrics.yml`](.github/workflows/metrics.yml) usando [`lowlighter/metrics`](https://github.com/lowlighter/metrics). Acione um refresh manual da aba **Actions** se quiser mais cedo; para plugins mais ricos (trÃ¡fego, follow-up time), adicione um secret de repositÃ³rio `METRICS_TOKEN` com um PAT fine-grained.

## HistÃ³rico de Stars

<a href="https://star-history.com/#nexu-io/open-design&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=nexu-io/open-design&type=Date&theme=dark&cache_bust=2026-04-30" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=nexu-io/open-design&type=Date&cache_bust=2026-04-30" />
    <img alt="HistÃ³rico de stars do Open Design" src="https://api.star-history.com/svg?repos=nexu-io/open-design&type=Date&cache_bust=2026-04-30" />
  </picture>
</a>

Se a curva sobe, esse Ã© o sinal que procuramos. DÃª â˜… neste repo para empurrÃ¡-la.

## LicenÃ§a

Apache-2.0. O `skills/guizang-ppt/` empacotado retÃ©m sua [LICENSE](skills/guizang-ppt/LICENSE) original (MIT) e atribuiÃ§Ã£o de autoria a [op7418](https://github.com/op7418).

---

Projeto adaptado da comunidade INEMA TDS · Marca **Arckhé**

Feito pelo **[ARCKHÉ.AI](https://linnoff88-dev.github.io/arckhe-ai)**.