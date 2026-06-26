# UAN no Dia a Dia — Site (GitHub Pages)

Página única (`index.html`), autossuficiente: imagens já embutidas, sem pastas ou dependências externas. É só subir e publicar.

## Publicar no GitHub Pages
1. Crie um repositório (ex.: `uannodiaadia-site`).
2. Envie os arquivos **`index.html`** e **`politica-de-privacidade.html`** para a raiz do repositório (os dois precisam ficar juntos, na mesma pasta).
3. Vá em **Settings → Pages**.
4. Em *Source*, escolha **Deploy from a branch**, branch **main** e pasta **/ (root)**. Salve.
5. Em 1–2 minutos o site fica no ar em `https://SEU-USUARIO.github.io/uannodiaadia-site/`.
6. (Opcional) Domínio próprio: aba **Pages → Custom domain**.

## Trocar os links da Hotmart
Abra o `index.html` e procure pelo bloco **`>>> LINKS DOS PRODUTOS`** (perto do fim, dentro de `<script>`).

Hoje todos os botões apontam para o link geral `https://hotm.io/r2ZzaYD`. Para cada produto, na Hotmart clique em **"Promover produto"**, copie o link `hotm.io` específico e cole no campo `link` correspondente:

| Produto | id na lista |
|---|---|
| Kit Profissional Completo | `6587672` |
| Guia Essencial | `7640894` |
| Formação | `7784054` |
| Mentoria Anual | `6630746` |

E o link do **UAN Cardápio Pro** (lista de espera / oferta de lançamento) na variável `LINK_CARDAPIO_PRO`.

## Lançamento automático
A contagem regressiva aponta para **10/07/2026**. Quando a data chegar, o contador vira "Disponível agora" e o botão do Cardápio Pro muda automaticamente de *"Entrar na lista de espera"* para *"Comprar agora"*. Não precisa editar nada.

## Editar preços / textos
Os 4 produtos são montados a partir da lista `PRODUTOS` no `<script>` — dá para ajustar nome, descrição, bullets e preço por ali, num lugar só.

---
Osmar Almeida · Nutricionista CRN 12979 · @uannodiaadia
