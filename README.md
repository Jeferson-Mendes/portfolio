# Portfólio — Jeferson Mendes

Site estático (um único `index.html`, sem build) pronto para o GitHub Pages.

## Publicar no GitHub Pages

1. Crie um repositório chamado **`jeferson-mendes.github.io`** (o nome precisa ser exatamente `<seu-usuario>.github.io`).
2. Suba os arquivos `index.html` e `CNAME` para a branch `main`.
3. No repositório: **Settings → Pages → Build and deployment → Source: Deploy from a branch → `main` / `(root)`**.
4. Em ~1 minuto o site estará em `https://jeferson-mendes.github.io`.

## Domínio personalizado

1. Edite o arquivo `CNAME` e troque `seudominio.com.br` pelo domínio que você comprou (só o domínio, sem `https://`).
2. No painel do registrador (Registro.br, Hostinger, Cloudflare etc.), crie os registros DNS:

   **Domínio raiz (`seudominio.com.br`)** — 4 registros `A`:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
   (opcional, IPv6 — registros `AAAA`: `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`)

   **`www`** — 1 registro `CNAME` apontando para `jeferson-mendes.github.io`

3. Em **Settings → Pages → Custom domain**, informe o domínio e salve. Quando o certificado ficar pronto, marque **Enforce HTTPS**.
4. Recomendado: verifique o domínio em **Settings (do seu perfil) → Pages → Add a domain**, para evitar que outra pessoa o reivindique.

A propagação de DNS pode levar de alguns minutos a algumas horas.

> Se usar Cloudflare como DNS, deixe os registros como "DNS only" (nuvem cinza) até o HTTPS do GitHub ser emitido.

## Personalizar

- Textos, experiências e stack ficam todos no `index.html`, em seções marcadas (`#sobre`, `#contextos`, `#competencias`, `#foco`, `#experiencia`, `#stack`, `#contato`).
- As cores estão em variáveis no topo do `<style>` (`--accent` muda o verde em todo o site).
- Tema claro/escuro segue o sistema e pode ser alternado no botão ◐.
