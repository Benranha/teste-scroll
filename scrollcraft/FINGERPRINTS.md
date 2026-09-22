# Fingerprints

Every site you build with **scroll-craft** gets one row here, appended after it
ships. The registry exists so your next build can prove it is a different page
rather than a re-skin of one you already made.

This file is **yours**. It starts empty on purpose: the gate is about not
repeating *yourself*, so it has nothing to say until you have built something.

The rules and the gate live in the skill's
`references/uniqueness.md`. Short version:

**A new build must differ from EVERY row below on at least 4 of the 6
dimensions.** Four against each row individually, not four on average across the
table. If a planned build fails, change the plan. Never edit a row to make room
for it.

The six dimensions are: **grammar**, **nav treatment**, **hero device**,
**act-sequence shape**, **close pattern**, **signature move**.

Dimension 6 is free, because a signature move is unique by definition. So the
gate really asks for three more out of the remaining five, and a build that
changes only grammar and world will fail it.

---

## The registry

| Build | Grammar | Nav treatment | Hero device | Act-sequence shape | Close pattern | Signature move | World | Port |
|---|---|---|---|---|---|---|---|---|
| `tres-livros` | Mundo contínuo (worldflight) | Percurso das três paradas, fixo à esquerda, clicável; ausente na abertura e no fim | Nome centrado sobre a sala em tela cheia, chapa radial só atrás do texto | 8 pernas alternando anda/para: 1.55 · 1.4 · 1.77 · 1.4 · 1.32 · 1.4 · 1.49 · 0.6 = 10.9vh | O quadro se abre de volta ao retrato inteiro (a mesa toda) e para; chamada e um botão na coluna ao lado | As marcas de corte: quando o filme congela num livro, quatro cantos em azul travam nos cantos reais do livro no vídeo e uma linha de chamada liga a ficha a ele | Documental cru do celular, HDR convertido para SDR, mesa branca como chão da página | 4507 |

*(primeira linha deste repositório. A próxima build tem de diferir desta em
pelo menos 4 das 6 dimensões.)*

---

## What is taken

Add a bullet here whenever a build claims something a later build should avoid
reusing: a grammar, a nav treatment, a close pattern, a signature move, an
act-count-and-length band. The shared columns are what the next build inherits
as a constraint, so writing them down is the whole point.

Tomado por **tres-livros**:

- **Gramática**: mundo contínuo (worldflight) com um único plano real cortado
  em pernas.
- **Chrome**: lista de paradas clicável na margem esquerda, que some na
  abertura e no fim.
- **Herói**: nome centrado sobre vídeo em tela cheia com chapa radial local.
- **Fecho**: o quadro se abre de volta ao retrato inteiro e para.
- **Assinatura**: marcas de corte travadas nos cantos reais de um objeto do
  vídeo, mais linha de chamada até a ficha.
- **Faixa de tamanho**: 8 pernas, 10.9vh, alternando movimento e congelamento.
- **Mundo**: documental cru de celular sobre mesa branca, chão claro.

### O que este build aprendeu (e a próxima build paga se esquecer)

- **Uma chapa de contraste não pode ser um bloco `[data-sc-copy]`.** O harness
  esconde todo `[data-sc-copy]` para fotografar o fundo, então uma chapa que é
  bloco de texto nunca entra na medição: o contraste continua reprovando e
  nenhum ajuste na chapa muda o número. Ela tem de ser um `div` comum, com a
  opacidade dirigida pela página.
- **O elemento medido é o que carrega `data-sc-copy`, e ele deve envolver só o
  texto.** Com o atributo num container de tela inteira, o harness amostra o
  quadro inteiro e reprova por causa de um canto escuro a 600px do texto.
- **Não dependa do evento `scroll` para enquadramento próprio.** Um `scrollTo`
  programático (o harness e os botões de navegação) nem sempre o emite, e o
  enquadramento fica atrasado em relação ao filme: na folha de contato aparecem
  quadros com a janela no lugar errado. Um laço `requestAnimationFrame` com
  comparação de chave resolve.
- **Congelar de verdade custa um clipe.** Uma perna de pausa feita só com
  pôster recebe o push-in do engine (`scale(1.03 → 1.17)`), que é justamente o
  que não pode acontecer numa parada. Meio segundo do quadro repetido,
  codificado como clipe, congela de verdade e pesa poucos KB.
- **`avconvert` resolve HDR do iPhone melhor que este ffmpeg.** O arquivo é
  HLG/bt2020 10 bits; sem `zscale` o ffmpeg local não tonemapeia, e o
  `avconvert --preset Preset1920x1080` do próprio macOS entrega SDR bt709
  correto para depois graduar.

---

## Appending a row

After shipping, add one line to the table and one bullet to **What is taken** if
the build claimed something new. Fill every column. Say what the build shares
with existing rows.

Rows are append-only. A build that has been superseded stays in the table,
because the space it occupies is still occupied.

---

## Worked example

The skill's author kept a registry of twelve builds across eight page grammars.
If you want to see what a filled-in table looks like, and which shapes tend to
collide, read `EXAMPLES.md` in the scroll-craft repository. Treat it as
illustration only: those rows are somebody else's builds and they do **not**
constrain yours.
