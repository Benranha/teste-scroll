# BRIEF · tres-livros

**Respondido pelo usuário.** O usuário dispensou a entrevista de oito perguntas e
mandou o brief abaixo em uma mensagem. As respostas estão nas palavras dele; onde
uma pergunta da entrevista não foi coberta, está marcado como *não respondido* e
a decisão tomada está escrita ao lado, para ele corrigir.

Única mídia: `teste-scroll/IMG_5453.MOV`. Nada gerado.

---

## O brief, verbatim

> Usa a skill scroll-craft com o vídeo teste-scroll/IMG_5453.MOV (é a única
> mídia, não gera nada novo). O vídeo é um plano contínuo: começa na sala, desce
> até a mesa, passa por três livros (Homens da Palavra, A Jornada de Meninos a
> Homens e Pastores da Família) e depois volta para a sala.
>
> 1. Abertura (sala, sem livro): só um nome bem simples no centro, grande e
>    limpo, e uma linha pequena embaixo pedindo para rolar a página. Mais nada na
>    tela.
> 2. Cada livro é uma parada: enquanto a pessoa rola, o vídeo avança. Quando a
>    câmera chega em cima de um livro, o vídeo segura naquele quadro por um
>    trecho de rolagem, e aparecem as informações do livro ao lado: título,
>    autor, uma frase curta sobre o que ele ensina e para quem é.
> 3. Continuando a rolar: as informações somem, o vídeo volta a andar até o
>    próximo livro e para de novo. O mesmo ritmo nos três livros: anda, para,
>    informa, anda.
> 4. Final: a câmera volta para a sala mostrando a mesa inteira, e a página
>    termina com uma chamada simples (um botão só).
>
> Regras: textos em português, informações reais dos livros (sem inventar
> números nem avaliações). No celular o vídeo ocupa a tela em pé e as
> informações ficam numa faixa embaixo. No computador as informações ficam do
> lado do vídeo, sem cobrir o livro. O vídeo é HDR do iPhone, então converte
> para SDR antes de codificar.

## As oito perguntas, mapeadas

1. **Vibe e referências.** *Não respondido.* Lido do brief: "simples", "grande e
   limpo". Decisão: claro, limpo, a mesa branca do vídeo vira o chão da página.
2. **A jornada, seção por seção.** Respondido: sala com nome → livro 1 → livro 2
   → livro 3 → sala com a mesa inteira e um botão.
3. **Curva de energia.** Respondido por ritmo: "anda, para, informa, anda", igual
   nos três livros.
4. **Sentimento por etapa e o momento único.** *Não respondido.* Ver curva abaixo.
5. **Algo que nenhum site faz.** *Não respondido.* Decisão: a assinatura abaixo.
6. **Distância do premium-minimal.** Lido do brief ("simples", "limpo"):
   premium-minimal em chão claro, não escuro.
7. **Mundo contínuo ou cenas?** Respondido: "o vídeo é um plano contínuo". Um
   mundo só.
8. **O que já existe.** Respondido: o vídeo e nada mais.

**Nome (decisão minha, trocar à vontade):** "Três livros".
**Botão (decisão minha):** "Quero ler os três". O destino do link não foi dado:
está como `#link-da-chamada` no HTML.

---

## A curva de sentimento

Uma linha por perna, sentimento primeiro, causa depois.

```
1  Chegada      a sala em tela cheia, o nome no meio, nada mais
2  Curiosidade  a câmera desce e o quadro se recolhe numa janela à direita
3  Atenção      o vídeo para em Homens da Palavra; as marcas travam nos cantos do livro
4  Deslocamento o vídeo volta a andar, sem texto, só a mesa
5  Confronto    para em A Jornada: o rosto na capa encara de volta
6  Deslocamento anda de novo
7  Peso         para em Pastores da Família: o livro que leva a conversa para casa
8  Chegada      a câmera volta para a sala, o quadro se abre e mostra a mesa inteira
9  Decisão      um botão
```

Duas linhas "deslocamento" vizinhas de paradas não são enchimento: são o
"anda" que o brief pede entre cada "para". O próprio brief pede o mesmo ritmo
três vezes, então a regra "sem sentimentos iguais lado a lado" é atendida pela
alternância anda/para, não pela variação entre as paradas.

## O pico

O brief exige o **mesmo ritmo nos três livros**, e isso vence a regra da skill
de dar mais rolagem a uma parada. As três paradas têm a mesma duração. O pico,
então, é o fim:

> "no final o vídeo volta pra sala, a janela se abre e você vê a mesa inteira
> com os três livros em cima, de onde você acabou de passar"

Mora na perna 7 (volta) e 8 (mesa).

## A frase de contar para alguém

> É o site onde o vídeo para em cima de cada livro, umas marcas de corte azuis
> se prendem nos cantos do livro de verdade, e a ficha dele aparece do lado.

## Silêncios de autor

- **As três paradas são pausas de autor.** O quadro está congelado de
  propósito. Um trecho sem mudança de imagem dentro de uma parada não é rolagem
  morta: a ficha entra, segura e sai nesse trecho.
- **O caminho entre as paradas não tem texto.** Nenhuma janela de texto cobre
  as pernas 3 e 5. É o "anda" do brief.

## Regras do brief que passam por cima da skill

- **"Uma linha pequena embaixo pedindo para rolar a página."** A skill proíbe
  qualquer chamada de rolagem. O usuário pediu explicitamente, então fica: uma
  linha de texto, sem seta nem animação.
- **Mesmo ritmo nas três paradas** no lugar de um pico com mais rolagem (acima).

## Fatos dos livros (só o que está na capa ou é público)

- **Homens da Palavra.** Subtítulo da capa: *Lições da vida de homens que
  andaram com Deus.* Nathan Busenitz (organizador), prefácio de John MacArthur.
- **A Jornada de Meninos a Homens.** JB Carvalho.
- **Pastores da Família.** Subtítulo da capa: *Chamando e preparando homens para
  liderar seus lares.* Voddie Baucham Jr.

Sem números, sem avaliações, sem o selo "best seller" da capa.

---

## Verificação (o que foi medido, e em quê)

Três passadas do harness, servindo em `localhost:4507`, Chrome real:

| Passada | Rolagem morta | Pernas | Contraste |
|---|---|---|---|
| 1440x900 | nenhuma | 8 de 8 pintam quadro real | todas as linhas acima de 4,5:1 no pior quadro |
| 390x844 | nenhuma | 8 de 8 pintam quadro real | idem |
| movimento reduzido | n/a | 8 de 8, só pôsteres | idem |

Sem erros de console nas três. Teclado: no topo nada é focável, nas paradas os
três botões do percurso, no fim o botão da chamada, todos visíveis quando
recebem foco.

**O que não foi verificado:** celular de verdade. O Chrome headless não
reproduz o decodificador de vídeo do iPhone, o modo de baixo consumo nem a
rolagem por toque. Se algum clipe aparecer congelado num iPhone, o caminho é
publicar `references/device-diag.html` ao lado do site na primeira rodada.

## Duas coisas do material, não do código

- **O fim é macio.** O foco automático do celular não fechou no último trecho,
  então os quadros da volta para a sala são mais moles que os das paradas. É o
  arquivo, não a codificação.
- **Aos ~9,4s passam pés no rodapé do quadro**, dentro da perna entre A Jornada
  e Pastores da Família. No computador o corte da janela tira quase tudo; no
  celular dá para ver por uns instantes.
