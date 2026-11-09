# vsl1

Landing page VSL Aloud — `index.html` com Meta Pixel + player de vídeo (VTurb) e interceptor UTM→SCK.
Hospedado em domínio próprio: https://vsl1.inglessemtrava.com

## Estado atual em produção

Em 2026-09-21, a página em produção estava com um tema **claro** (light mode), enquanto o `index.html`
deste repositório ainda reflete o tema **escuro** (dark mode) do último commit. Diferenças identificadas
via diff entre o HTML local e o HTML servido em produção:

- **Paleta de cores** (`:root`): fundo `#0a0a0a` → `#ffffff`, borda `#1e1e1e` → `#e0e0e0`,
  texto `#f5f5f5` → `#000000`.
- **Urgency bar**: fundo `#000` → `#ffffff`; texto com `letter-spacing` reduzido (`0.12em` → `0.03em`),
  cor `#fff` → `#000000` com `-webkit-text-stroke: 0.5px #000000`; destaque da data
  (`.highlight`) mudou de dourado (`var(--gold-end)`) para vermelho puro (`#ff0000`).
- **Footer**: fundo `#000` → `#ffffff`.
- **Conteúdo**: o emoji `⚠️` no início do texto da urgency bar foi removido em produção.

O restante do HTML (estrutura, scripts, embed do player VTurb, interceptor UTM→SCK) é idêntico entre
repo e produção. Um snapshot do HTML de produção nesse estado está versionado em
[`inglessemtrava-vsl1`](https://github.com/jvf2298019/inglessemtrava-vsl1).

**Pendência:** sincronizar este repositório com o tema claro atualmente em produção, ou reverter a
produção para o tema escuro do repo — decisão de negócio, não técnica.
