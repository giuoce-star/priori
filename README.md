[LEIA-ME.md](https://github.com/user-attachments/files/28398000/LEIA-ME.md)
# Site Priori Engenharia — Guia de publicação

Site institucional completo da Priori Engenharia, construído em HTML/CSS/JS puro. Sem dependências, sem CMS, sem custos de hospedagem.

## 📁 Estrutura do projeto

```
priori/
├── index.html                          → Home
├── sobre.html                          → Página Sobre
├── construcao-civil.html               → Hub de Construção Civil
├── engenharia-ambiental.html           → Hub de Engenharia Ambiental
├── subestacao-eletrica.html            → Serviço
├── avcb.html                           → Serviço
├── casas.html                          → Serviço
├── industrias.html                     → Serviço
├── esgoto.html                         → Serviço
├── drenagem.html                       → Serviço
├── galpoes.html                        → Serviço
├── descontaminacao.html                → Serviço
├── paisagismo.html                     → Serviço
├── recuperacao-areas-degradadas.html   → Serviço
├── eta.html                            → Serviço
├── ete.html                            → Serviço
├── atestados.html                      → Atestados e certificações
├── depoimentos.html                    → Depoimentos
├── blog.html                           → Blog (placeholder)
├── contato.html                        → Contato com formulário
├── obrigado.html                       → Página pós-envio do formulário
├── styles.css                          → Estilos (compartilhado)
├── main.js                             → Scripts (compartilhado)
└── assets/
    ├── logo-original.png               → Logo original (fundo preto)
    └── logo-original-transparent.png   → Logo aplicada no site
```

**Total: 19 páginas HTML, 1 CSS, 1 JS, 2 imagens. Tudo abaixo de 600 KB.**

---

## 🚀 Como colocar o site no ar — passo a passo

### Opção 1 — Netlify (recomendado)

**Por que Netlify?** Hospedagem gratuita pra sempre, HTTPS automático, deploy em 30 segundos, fácil apontar o domínio próprio.

1. **Crie uma conta grátis** em [netlify.com](https://www.netlify.com)
2. Faça login no painel
3. Procure o botão **"Add new site" → "Deploy manually"**
4. **Arraste a pasta `priori`** inteira pra dentro da área indicada
5. Aguarde o upload — em 20 segundos seu site está no ar em uma URL tipo `random-name-12345.netlify.app`
6. Teste navegando pelas páginas

**Pronto, seu site já tá online de graça.**

### Apontar o domínio prioriengenharia.com pro Netlify

1. No painel do site no Netlify, vá em **Domain settings** → **Add a domain**
2. Digite `prioriengenharia.com` e confirme
3. O Netlify vai te mostrar **2 nameservers** parecidos com:
   - `dns1.p01.nsone.net`
   - `dns2.p01.nsone.net`
   - `dns3.p01.nsone.net`
   - `dns4.p01.nsone.net`
4. **Anote esses 4 endereços**
5. Vá no painel onde o domínio está registrado (Registro.br, GoDaddy, Hostinger, etc.)
6. Procure **"Servidores DNS"** ou **"Nameservers"** e cole os 4 endereços que o Netlify te deu
7. Salve

⏰ A propagação leva entre 1 hora e 24 horas (geralmente menos de 4h).

Depois disso, `prioriengenharia.com` aponta pro novo site e o HTTPS é ativado automaticamente.

### Opção 2 — Vercel

Mesmo processo, só que em [vercel.com](https://vercel.com). Funciona igual.

### Opção 3 — Cloudflare Pages

Idem, em [pages.cloudflare.com](https://pages.cloudflare.com). Também grátis.

---

## 📧 Ativar o formulário de contato

O formulário usa **FormSubmit** (gratuito, sem cadastro).

1. Abra o arquivo `contato.html`
2. Procure pela linha (em torno da linha 80):

   ```html
   <form action="https://formsubmit.co/contato@prioriengenharia.com" method="POST" ...>
   ```

3. Substitua `contato@prioriengenharia.com` pelo **e-mail real** que vai receber os leads (ex: `frederico@prioriengenharia.com`)

4. Faça o **primeiro envio de teste** pelo site após publicar — o FormSubmit vai mandar um e-mail de confirmação pro destinatário. **É preciso clicar no link de confirmação** uma única vez pra ativar.

5. A partir daí, todo envio de formulário cai direto na caixa de entrada do e-mail configurado.

---

## ✏️ Como editar conteúdo do site

Tudo é HTML normal. Basta abrir o arquivo da página que você quer alterar com qualquer editor (VS Code, Sublime Text, ou até bloco de notas) e mudar o texto.

**Onde encontrar coisas comuns:**

- **Textos de qualquer página**: dentro do arquivo `.html` correspondente
- **Cores e tipografia do site inteiro**: arquivo `styles.css`, no topo, dentro de `:root`
- **WhatsApp e telefone**: usar busca/substituir pelo número antigo nas páginas (Ctrl+F)
- **Logo**: substituir os arquivos em `assets/` mantendo os nomes
- **Logos de clientes na home**: editar o trecho `<section class="clients">` em `index.html`

**Depois de editar:** salve o arquivo e arraste a pasta de novo no Netlify pra atualizar o site no ar (leva 20 segundos).

---

## 🔧 Coisas pra revisar antes de divulgar o site

- [x] ~~Trocar e-mail do formulário em `contato.html`~~ → **Feito:** `contato@prioriengenharia.com`
- [x] ~~Confirmar CNPJ no `footer`~~ → **Confirmado:** 10.957.982/0001-68
- [x] ~~Confirmar telefone~~ → **Confirmado:** apenas WhatsApp (71) 99903-7045
- [ ] Substituir as imagens dos cards e do hero pelas fotos reais de obras quando o dono enviar
- [ ] Atualizar bios do Frederico Santos e Giulia Oceano em `sobre.html` com info real
- [ ] Revisar a lista de clientes em `index.html` na seção de logos
- [ ] Quando o dono confirmar os atestados reais, substituir os textos em `atestados.html`
- [ ] Quando coletar depoimentos reais de clientes, substituir os placeholders em `depoimentos.html`

---

## 🎨 Sistema visual usado

Caso o cliente queira manter o padrão visual em outras peças:

- **Fontes**: Fraunces (títulos) + Manrope (corpo) — ambas Google Fonts gratuitas
- **Paleta**:
  - Fundo creme: `#EFEAE0`
  - Fundo creme alt: `#F6F2EA`
  - Fundo escuro: `#14140F`
  - Texto principal: `#14140F`
  - Texto secundário: `#5C5C50`
  - Acento (verde-musgo): `#2D3F1F`
  - Acento dourado (sobre fundo escuro): `#C9B98F`

---

## ❓ Problemas comuns

**"Não aparece estilo no site"** → o arquivo `styles.css` não está na mesma pasta dos HTMLs. Coloque-o ao lado do `index.html`.

**"Logo não aparece"** → a pasta `assets/` precisa estar dentro da pasta principal (no mesmo nível dos HTMLs).

**"Formulário envia mas não chega e-mail"** → você ainda não fez o primeiro envio pra ativar o FormSubmit. Faça um envio teste e clique no link de confirmação que chega no e-mail destinatário.

**"Quero adicionar uma página nova"** → copie um arquivo existente (ex: `casas.html`), renomeie, edite o conteúdo. Lembre de adicionar o link no menu (header) e no footer das outras páginas.

---

Qualquer dúvida na manutenção, é só voltar aqui.
