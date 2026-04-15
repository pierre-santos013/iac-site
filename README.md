# iac-site

Site de download do [Local AI Assistant](https://github.com/pierre-santos013/iac) — landing page estática servida via Docker.

## Stack

- [Astro](https://astro.build) — geração de HTML estático
- Tailwind CSS — estilização
- Docker + `serve` — servidor de produção (porta 3009)

## Rodar localmente

```bash
npm install
npm run dev
```

## Build e Docker

```bash
npm run build
docker compose up --build -d
```

Acesse em `http://localhost:3009`.

---

## Publicar nova versão do app

O botão de download busca automaticamente o release mais recente via API do GitHub (`pierre-santos013/iac-site/releases/latest`).

Para disponibilizar uma nova versão:

```bash
gh release create v0.X.X "caminho/Local-AI-Assistant-Setup-0.X.X.exe" \
  --repo pierre-santos013/iac-site \
  --title "v0.X.X" \
  --notes "Local AI Assistant v0.X.X"
```

> O repositório de código-fonte da aplicação (`pierre-santos013/iac`) é privado.
> Os releases públicos do instalador `.exe` ficam neste repo (`iac-site`).
