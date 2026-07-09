# Imagens

Coloque aqui as imagens das notícias (e outras imagens do site), para hospedá-las
no próprio repositório em vez de depender de links externos.

## Como usar

1. Suba o arquivo de imagem nesta pasta — ex.: `anpd.jpg`, `iia.png`.
2. No `index.html`, dentro do bloco da notícia, use o caminho relativo:

   ```html
   <a class="ncard-media" href="...">
     <img src="imagens/anpd.jpg" alt="descrição curta da imagem">
   </a>
   ```

   E no destaque:

   ```html
   <a class="featured-media" href="...">
     <span class="featured-ribbon">● Em destaque</span>
     <img src="imagens/destaque.jpg" alt="descrição curta">
   </a>
   ```

## Dicas

- Formato: **JPG**, **PNG** ou **WebP**.
- Proporção ideal ~**16:10** (o site recorta sozinho com `object-fit: cover`).
- Largura recomendada: **800–1200px** (não precisa ser gigante — deixa o site leve).
- Sempre preencha o `alt` com uma descrição curta (acessibilidade e SEO).
- Prefira hospedar a imagem aqui a usar link externo, que pode sair do ar.
