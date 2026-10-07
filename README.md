# Face VSL — Vercel final

Versão ajustada para hospedagem estática na Vercel.

## Player
- MP4 em `/assets/vsl.mp4` com H.264/AAC e `faststart`.
- ~12 MB, abaixo do limite de 25 MB.
- Autoplay mudo via atributo HTML + tentativas redundantes em JS.
- Primeiro toque em qualquer lugar do vídeo: reinicia em 0:00 e ativa o som.
- Sem controles nativos de pausar/avançar.
- Barra de progresso visual acelerada; ela não altera o tempo real do vídeo.
- Capa `/assets/capa.jpg` enquanto o primeiro frame não estiver disponível.

## Vercel
Envie o conteúdo desta pasta preservando `assets/` ao lado de `index.html`.
