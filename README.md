# Face VSL Template

Template reutilizável de página VSL com aparência de feed social, feito em HTML/CSS/JS puro e otimizado para mobile.

## O que já funciona

- Layout responsivo/mobile-first.
- Perfil, seguidores, selo, copy e números sociais configuráveis.
- Player de vídeo nativo HTML5.
- CTA liberado depois de **tempo realmente assistido**.
- Curtida com incremento/decremento visual.
- Botão de comentar que leva ao campo.
- Comentários locais editáveis e curtidas nos comentários.
- Novo comentário inserido instantaneamente no feed.
- Compartilhamento via Web Share API; fallback para copiar link.
- Bloco de oferta/checkout configurável.
- Sem bibliotecas externas e sem dependências.

## Como personalizar

Abra `index.html` e procure por:

```js
const CONFIG = {
```

É ali que você altera:

- `pageName`
- `avatarUrl`
- `followersText`
- `postText`
- `videoUrl`
- `posterUrl`
- `ctaDelaySeconds`
- `offerTitle`
- `offerText`
- `ctaText`
- `ctaUrl`
- `comments`

### Vídeo local

Crie uma pasta `assets`, coloque a VSL dentro dela e use:

```js
videoUrl: "./assets/vsl.mp4"
```

Para performance, prefira um MP4 H.264 bem comprimido ou uma CDN de vídeo.

## Vercel

O projeto pode ser enviado diretamente para a Vercel como site estático. O `vercel.json` incluído adiciona cache de assets e cabeçalhos básicos.

## Observação

O template usa uma interface social genérica inspirada em padrões de feed. Personalize marca, textos, imagens e disclosures para sua campanha antes de publicar.
