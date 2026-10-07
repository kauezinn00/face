# Face VSL Template

Template em **HTML/CSS/JS puro** para páginas no estilo **feed social + VSL**, pronto para subir na Vercel.

## Arquivos

- `index.html` — página completa.
- `vercel.json` — configuração simples para Vercel.
- `assets/` — fotos de perfil usadas nos comentários.
- `README.md` — instruções rápidas.

## O que já foi adicionado nesta versão

- visual mais fiel ao estilo social/Face;
- curtida azul no botão principal;
- reações nos comentários (curtida/coração);
- respostas encadeadas dentro de alguns comentários;
- botão **Ver mais comentários**;
- suporte a foto de perfil na página e nos comentários;
- fotos de perfil já conectadas no bloco de comentários.

## Como editar rápido

Abra o `index.html` e procure pelo objeto:

```js
const CONFIG = {
```

Troque principalmente:

- `brandText` — texto do topo.
- `pageName` — nome da página/persona.
- `avatarUrl` — foto principal da página.
- `followersText` — texto de seguidores.
- `postText` — hook/copy acima da VSL.
- `videoUrl` — URL ou caminho do vídeo.
- `posterUrl` — capa opcional do vídeo.
- `initialLikes`, `initialComments`, `initialShares` — números sociais.
- `ctaDelaySeconds` — segundos **realmente assistidos** antes de liberar a oferta.
- `offerKicker`, `offerTitle`, `offerText`, `ctaText`, `ctaUrl`, `microcopy` — bloco da oferta.
- `comments` — comentários iniciais.
- `commentsPerPage` — quantos comentários aparecem por vez.

## Estrutura de comentário

Cada comentário aceita este formato:

```js
{
  name: "Mariana Costa",
  avatarUrl: "./assets/comment-01.webp",
  text: "Comentário aqui",
  time: "12 min",
  likes: 18,
  reactions: ["like", "love"],
  replies: [
    {
      name: "Larissa Gomes",
      avatarUrl: "./assets/comment-02.webp",
      text: "Resposta aqui",
      time: "8 min",
      likes: 3,
      reactions: ["like"]
    }
  ]
}
```

## CTA controlado pela retenção

O CTA aparece depois do tempo definido em `ctaDelaySeconds`, contando apenas o tempo de vídeo **assistido de verdade**. Saltar o vídeo não libera o CTA instantaneamente.

## Publicação na Vercel

1. Coloque os arquivos em uma pasta.
2. Se usar imagens/vídeos locais adicionais, mantenha dentro de `assets/`.
3. Faça upload para a Vercel.


### Refinamentos visuais extras

- tipografia e espaçamento refinados para ficar mais próximos de um feed social real;
- comentários com threads visuais e linha lateral;
- números e reações mais naturais;
- textos de comentários fortalecidos para gerar curiosidade e retenção sem depender de uma oferta específica;
- comentários adicionais para aumentar a profundidade visual da seção.
