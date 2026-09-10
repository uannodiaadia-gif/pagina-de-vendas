# consultoria-empresarial

Página da linha **Consultoria Empresarial**, um braço do ecossistema UAN no Dia a Dia.
Serve às duas modalidades: empresas de refeições coletivas e consultorias de qualidade em UAN.

URL final: `https://uannodiaadia.com/consultoria-empresarial/`
Endereço curto de divulgação: `https://consultoria.uannodiaadia.com` (atalho 301 no Cloudflare)

Versão do conteúdo: v6 · 10/09/2026 · Osmar Almeida, Nutricionista CRN 12979

---

## Conteúdo da pasta

```
consultoria-empresarial/
├── index.html                    página completa, um arquivo só (CSS e JS embutidos)
├── favicon.svg                   ícone da aba
├── README.md                     este arquivo
└── assets/
    ├── og-image.png              1200×630 — prévia ao compartilhar link
    └── apple-touch-icon.png      180×180 — ícone ao salvar na tela do iPhone
```

Nenhuma dependência externa além das fontes do Google Fonts (Lora, Poppins, JetBrains Mono),
carregadas por `<link>`. A página funciona offline com fontes de sistema como reserva.

## Como publicar

Arrastar a pasta `consultoria-empresarial/` para a **raiz** do repositório `uannodiaadia-gif`,
no mesmo nível de `index.html` e da pasta `uanpro`, e fazer o commit. O GitHub Pages publica
em alguns minutos.

O arquivo tem que se chamar `index.html` dentro da pasta — é o que faz a URL terminar em
`/consultoria-empresarial/`, sem `.html`. Essa é exatamente a URL declarada no `canonical`
e no JSON-LD da página, então não há nada a ajustar depois.

**Não** mexer no `CNAME` da raiz. Ele continua valendo para todo o site.

## Depois de publicar — três acertos na raiz do repositório

### 1. `sitemap.xml`

Acrescentar antes de `</urlset>`:

```xml
<url>
  <loc>https://uannodiaadia.com/consultoria-empresarial/</loc>
  <lastmod>2026-09-10</lastmod>
  <changefreq>monthly</changefreq>
  <priority>0.9</priority>
</url>
```

### 2. `llms.txt`

Acrescentar uma linha na seção de páginas:

```
- [Consultoria Empresarial](https://uannodiaadia.com/consultoria-empresarial/): assessoria em gestão para empresas de refeições coletivas e para consultorias de qualidade em UAN. O cliente é a pessoa jurídica. Diagnóstico prévio por formulário, sem responsabilidade técnica assumida.
```

### 3. `index.html` da raiz

Acrescentar o bloco curto de chamada para a página, e o link no menu e no rodapé.
A arquitetura decidida em 10/09/2026 é: home com chamada curta, página própria com o
conteúdo completo — para não haver conteúdo duplicado entre as duas.

## Verificação depois do deploy

- [ ] `https://uannodiaadia.com/consultoria-empresarial/` abre, com cadeado fechado
- [ ] os quatro botões de diagnóstico abrem os formulários certos (dois por modalidade)
- [ ] no celular, as duas modalidades empilham e o texto não estoura
- [ ] mandar o link para si mesmo no WhatsApp: a prévia tem que mostrar a `og-image.png`
- [ ] o botão de WhatsApp abre a conversa em (32) 98415-1828
- [ ] favicon aparece na aba

## Pendências conhecidas desta página

- `assets/osmar-foto-email.jpg` ainda não está aqui. Subir a foto 220×220 já otimizada
  resolve a pendência do e-mail de prospecção: a URL pública passa a existir e dá para
  usar `<img src="https://uannodiaadia.com/consultoria-empresarial/assets/osmar-foto-email.jpg">`.
  O caminho `cid:` não funciona pela API do Gmail — testado e descartado em 08/09/2026.
- O favicon e o ícone de iOS usam o monograma simplificado do cabeçalho, na paleta de
  documentos. Quando o ícone de produto oficial (hexágono esmeralda e dourado) for
  validado, substituir os dois pela versão oficial.
- Decisão em aberto: se o valor do investimento aparece no documento da etapa 2
  ("Diagnóstico apresentado") ou só depois da call. O texto atual funciona nas duas
  hipóteses, então não trava a publicação.
