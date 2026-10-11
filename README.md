# GLOBAL SCALE — site pronto para a Vercel

Pacote com apenas 3 arquivos:

```
index.html    o site inteiro (HTML, CSS, JS e as fotos já embutidos)
vercel.json   configuração da Vercel (URLs limpas e cabeçalhos de segurança)
README.md     este guia
```

Não tem build, não tem dependências e não precisa de pasta de imagens.

## Como publicar na Vercel

**Pelo site (mais simples)**
1. Acesse vercel.com e entre na sua conta.
2. Clique em **Add New → Project** e escolha **"Deploy"** a partir de um upload, ou arraste esta pasta para vercel.com/new.
3. Em *Framework Preset* deixe **Other** e não preencha *Build Command* nem *Output Directory*.
4. Clique em **Deploy**. Em alguns segundos o site estará no ar.

**Pelo terminal**
```bash
npm i -g vercel
cd global-scale
vercel --prod
```

**Domínio próprio:** no projeto da Vercel, vá em *Settings → Domains* e adicione o seu domínio.

## Como editar

Abra o `index.html` em qualquer editor e procure por **`CONFIGURAÇÃO DO SITE`** (fica dentro do primeiro `<script>`). Ali estão:

- `brand` — nome e frase da marca;
- `contact.whatsapp` — número do WhatsApp (só números, com 55 + DDD), o texto exibido e a mensagem inicial;
- `company` — razão social, CNPJ e endereço (campos vazios não aparecem no site);
- `offer.ctaUrl` — link do checkout da Kiwify (já configurado);
- `offer` — o que está incluído e como o conteúdo é disponibilizado (valor e pagamento aparecem como "Exibido no checkout");
- `tracking` — IDs do Google Analytics (GA4) e do Pixel da Meta, se quiser ativar;
- `modules`, `steps`, `faq`, `audience` — os textos de cada seção.

Os textos da política de privacidade e dos termos de uso ficam no final do `<body>`, nos blocos `<dialog>`. São modelos: revise com um profissional antes de divulgar.

## Fotos

As 8 fotos estão embutidas no `index.html` em formato WebP (blocos `<img src="data:image/webp;base64,...">`). Para trocar uma, use um conversor de imagem para base64 e substitua o texto do `src`, ou me peça para gerar um novo pacote.

## Observações

- Compartilhar o link no WhatsApp ou Instagram mostra título e descrição, mas sem imagem de capa. Para ter capa, suba um arquivo `og.jpg` (1200×630) na raiz e inclua no `<head>`: `<meta property="og:image" content="https://SEU-DOMINIO/og.jpg">`.
- As fotos são ilustrativas de estilo de vida e o site informa isso. Mantenha o aviso e não acrescente legendas que sugiram ganhos.
- Os botões de acesso abrem o checkout `https://pay.kiwify.com.br/EBMKn6K` em nova aba.
