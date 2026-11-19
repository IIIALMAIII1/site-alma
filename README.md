# ALMA Arquitetura e Gestão de Obra

Site estático (um `index.html` + vídeos). Não precisa instalar nada nem fazer build.

Todos os arquivos ficam no mesmo nível, sem subpastas:

```
index.html        ← o site inteiro (HTML, CSS e JavaScript)
alma-16x9.mp4     ← vídeo horizontal (computador)
alma-9x16.mp4     ← vídeo vertical (celular)
poster-16x9.jpg
poster-9x16.jpg
README.md
```

## Publicar no GitHub Pages

### Opção A: pelo navegador (sem terminal)

1. Entre em github.com e clique em **New repository**.
2. Nome: `alma-site` (ou outro). Deixe **Public** e clique em **Create repository**.
3. Na página do repositório, clique em **uploading an existing file**.
4. Selecione os 6 arquivos juntos e arraste para a janela.
5. Clique em **Commit changes**.
6. Vá em **Settings → Pages**. Em **Source**, escolha **Deploy from a branch**, branch **main**, pasta **/ (root)**, e clique em **Save**.
7. Em 1 a 2 minutos o site fica no ar em `https://SEU-USUARIO.github.io/alma-site/`.

### Opção B: pelo terminal (Git)

```bash
cd alma-site
git init
git add .
git commit -m "Site ALMA"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/alma-site.git
git push -u origin main
```

Depois faça o passo 6 da opção A.

## Domínio próprio (opcional)

Em **Settings → Pages → Custom domain**, digite o domínio (por exemplo `almaobras.com.br`) e, no painel onde o domínio foi comprado, crie os registros DNS que o GitHub mostrar. Marque **Enforce HTTPS** quando ficar disponível.

## Antes de divulgar

- **Fotos:** as fotos são ilustrativas, carregadas do Unsplash. Troque pelas fotos dos seus voos e obras: procure `images.unsplash.com` no `index.html` e substitua cada endereço pelo caminho da sua foto (por exemplo `fotos/obra-01.jpg`, com a foto enviada para uma pasta `fotos`).
- **Medidas da seção de acompanhamento:** os números (área, largura, diâmetro) são ilustrativos. Ficam no `index.html` no bloco `var RD=[ ... ]` e nos textos dentro de `<svg class="meas">`.
- **WhatsApp:** o número está em `wa.me/5511961729497`. Se mudar, troque em todos os lugares onde aparece.
- **Cores:** ficam no início do `<style>`, no bloco `:root { --bg: ...; --accent: ...; }`.

## Editar depois

Edite o `index.html` direto no GitHub (ícone de lápis) e clique em **Commit changes**. O site atualiza sozinho em cerca de 1 minuto.
