# Coisa de Auditor — kit de publicação

Esta pasta é o site pronto para publicar:

- `index.html` — o site completo (capa + abas Ferramentas, Notícias, Planilhas)
- `downloads/` — as duas planilhas reais (walkthrough e workpaper SOX/COSO)

## Passo a passo

1. **Instale o Claude Code** (na sua máquina pessoal)
   - Windows (PowerShell): `irm https://claude.ai/install.ps1 | iex`
   - macOS/Linux: `curl -fsSL https://claude.ai/install.sh | bash`
   - Verifique: `claude --version`

2. **Crie sua conta no GitHub** (github.com, gratuita), se ainda não tiver.
   Contas e senhas são sempre você quem cria e digita — nunca o Claude Code.

3. **Abra o terminal DENTRO desta pasta** e rode: `claude`
   Faça login com sua conta Claude quando pedir.

4. **Cole este prompt como primeira mensagem:**

> Este é o projeto do site estático coisadeauditor.com.br (index.html + pasta downloads/).
> Quero publicá-lo. Vamos passo a passo, explicando antes de executar:
> 1) inicialize o git e crie um repositório no GitHub (me guie na autenticação);
> 2) publique como site estático — me recomende o caminho mais simples (GitHub Pages ou Netlify) e execute;
> 3) confirme que os dois links de download da aba Planilhas funcionam no site publicado;
> 4) ao final, me diga exatamente quais registros DNS eu configuro no registro.br
>    para apontar coisadeauditor.com.br para o site, e como ativar o HTTPS.

5. **DNS**: com os registros que o Code te passar, entre no painel do **registro.br**
   e configure você mesmo (é conta sua). A propagação pode levar de minutos a algumas horas.

6. **Teste**: abra https://coisadeauditor.com.br, navegue pelas abas e baixe as duas planilhas.

## O que fica para depois (já combinado)

- Ligar o formulário da newsletter a um serviço real (hoje é protótipo e avisa isso).
- Matriz de risco e Parecer técnico estão como "Em breve" na aba Planilhas.
- A calculadora de risco & materialidade segue "em estudo" na aba Ferramentas.
