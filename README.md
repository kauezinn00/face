# Face VSL — Player vertical de teste

Base: versão aprovada sem faixa Facebook e sem texto no rodapé. Fotos dos comentários continuam embutidas no HTML.

## Arquivos
- `index.html` — página completa.
- `assets/vsl.mp4` — vídeo original com metadata de streaming movida para o começo (faststart).
- `assets/capa.jpg` — miniatura do vídeo.
- `vercel.json` — configuração Vercel.

## Player
- 9:16 (vertical), sem controles nativos para pausa/avanço.
- Tenta autoplay com áudio. Navegadores normalmente **bloqueiam autoplay com som** sem interação.
- Se bloqueado, tenta autoplay mudo com botão **Ativar som**. Ao tocar, volta o vídeo para o início e liga o som.
- O progresso é visual, acelerado de forma não linear. **Não mede a porcentagem real assistida.** Não tem clique nem recurso de avançar.
- O CTA continua configurado via `CONFIG.ctaDelaySeconds` contando progresso real do vídeo, independentemente da barra visual.

## Próximas ofertas
No `index.html`, procure por `const CONFIG = {` para trocar nome, textos, VSL, checkout e comentários.
Se alterar `videoUrl` e `posterUrl`, altere apenas os caminhos em CONFIG. As referências visuais no HTML são substituídas no `init()`.

## Uso
Extraia a pasta e abra `index.html` em navegador moderno. Para teste mais fiel do autoplay, sirva a pasta por um servidor local ou faça deploy na Vercel.
