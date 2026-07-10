# Como editar o site coisadeauditor.com.br

Guia rápido para alterar o site pela sua máquina, no VSCode, sem dor de cabeça.

O site é publicado automaticamente: **todo `git push` atualiza
https://coisadeauditor.com.br em ~1 minuto.**

---

## Parte 1 — Configuração (só na primeira vez)

1. **Instale o VSCode** (se ainda não tiver): https://code.visualstudio.com/
2. **Abra a pasta do projeto no VSCode:**
   - VSCode → menu **File → Open Folder…**
   - Selecione: `C:\Site novo\coisadeauditor-projeto`
3. Pronto. O Git já está instalado e configurado nesta pasta — não precisa
   clonar nem logar de novo.

> Abra o terminal dentro do VSCode em **Terminal → New Terminal**.
> Ele já abre dentro da pasta certa.

---

## Parte 2 — O ciclo de toda alteração (SEMPRE nesta ordem)

### 1. Puxe a versão mais recente ANTES de mexer
```bash
git pull
```
Isso traz o que foi alterado no GitHub (por você pela web, ou por mim).
**Nunca pule este passo** — é o que evita conflito.

### 2. Faça suas edições
Abra o `index.html` (ou outro arquivo), altere e **salve** (`Ctrl+S`).

### 3. Veja o resultado antes de publicar
Dê **duplo-clique** no `index.html` (no Explorer do Windows) para abrir no
navegador e conferir. Nada disso ainda foi publicado.

### 4. Registre e publique
```bash
git add -A
git commit -m "descreva o que mudou"
git push
```
Em ~1 minuto o site novo está no ar. Confira em https://coisadeauditor.com.br
(use **Ctrl+F5** para furar o cache do navegador).

---

## Alternativa sem digitar comandos (aba Source Control)

No VSCode, clique no ícone de ramificação na barra lateral (ou `Ctrl+Shift+G`):

1. Clique em **⋯ → Pull** (ou no ícone de sincronizar) — equivale ao `git pull`.
2. Faça as edições e salve.
3. Escreva a mensagem na caixa de texto e clique em **✓ Commit**.
4. Clique em **Sync Changes** (ou **Push**) — publica.

Faz exatamente o mesmo que os comandos acima.

---

## Receitas rápidas

### Trocar um texto
Abra `index.html`, use `Ctrl+F` para achar o texto, edite, salve, e faça o
ciclo do commit/push.

### Adicionar a imagem de uma notícia
1. Coloque o arquivo na pasta `imagens/` (ex.: `imagens/anpd.jpg`).
2. No `index.html`, ache o card da notícia e troque o comentário
   `<!-- IMAGEM: ... -->` por:
   ```html
   <img src="imagens/anpd.jpg" alt="descrição curta da imagem">
   ```
3. Commit + push. (Mais detalhes em `imagens/README.md`.)

---

## Se der erro no `git push`

Mensagem tipo *"Updates were rejected"* ou *"rejected (non-fast-forward)"*
significa que há algo novo no GitHub que você ainda não puxou. Resolva com:
```bash
git pull
git push
```
Se aparecer um conflito que você não souber resolver, é só me chamar.

---

## Regra de ouro

**Edite em um lugar de cada vez e sempre `git pull` antes de começar.**
Prefira editar aqui no VSCode; use o GitHub web só para retoques rápidos
quando não estiver na sua máquina.
