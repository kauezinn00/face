# Face VSL Template

Template em **HTML/CSS/JS puro** para páginas no estilo **feed social + VSL**, pronto para subir na Vercel.

## Arquivos

- `index.html` — página completa.
- `vercel.json` — configuração simples para Vercel.
- `README.md` — instruções rápidas.

## Como editar rápido

Abra o `index.html` e procure pelo objeto:

```js
const CONFIG = {
```

Troque principalmente:

- `brandText` — texto do topo.
- `pageName` — nome da página/persona.
- `avatarUrl` — foto principal do perfil.
- `followersText` — texto de seguidores.
- `postText` — hook/copy acima da VSL.
- `videoUrl` — URL ou caminho do vídeo.
- `posterUrl` — capa opcional do vídeo.
- `initialLikes`, `initialComments`, `initialShares` — números sociais.
- `ctaDelaySeconds` — segundos **realmente assistidos** antes de liberar a oferta.
- `offerKicker`, `offerTitle`, `offerText`, `ctaText`, `ctaUrl`, `microcopy` — bloco da oferta.
- `comments` — comentários iniciais.
- `commentsPerPage` — quantos comentários aparecem por vez.

## Comentários com foto

Cada comentário aceita:

```js
{
  name: "Mariana Costa",
  avatarUrl: "./assets/mariana.jpg",
  initials: "MC",
  text: "Comentário aqui",
  time: "12 min",
  likes: 18
}
```

Se `avatarUrl` estiver vazio, ele usa as iniciais.

## Foto principal da página

Para usar a foto principal do perfil:

```js
avatarUrl: "./assets/perfil.jpg"
```

## CTA controlado pela retenção

O CTA aparece depois do tempo definido em `ctaDelaySeconds`, contando apenas o tempo de vídeo **assistido de verdade**. Saltar o vídeo não libera o CTA instantaneamente.

## Publicação na Vercel

1. Coloque os arquivos em uma pasta.
2. Se usar imagens/vídeos locais, crie uma pasta `assets/`.
3. Faça upload para a Vercel.

## Observação

A estrutura foi deixada mais realista visualmente, com:

- topo social mais fiel;
- botões com estados ativos;
- reação azul no Curtir;
- contadores de reações/comentários/compartilhamentos;
- lista maior de comentários;
- suporte a foto de perfil na página e nos comentários.
