# **Tailwind CSS**

Framework utilitário de CSS, ou seja, vem com uma série de classes prontas pra usar direto no HTML, sem precisar escrever estilos separados em outro arquivo. Cada um dos atributos vai ter sua própria classe no tailwind, agilizando o desenvolvimento e mantendo a consistência visual.

### VANTAGENS E CARACTERÍSTICAS DO TAILWIND
- A manipulação é mais rápida
- Evita fazer mudanças que quebrem o layout 
- Padronização de classes
- Facilidade para utilizar hovers, dark mode e design responsivo

Toda vez que mexer com Tailwind devemos rodar esse código no terminal: 
"npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch"

JAMAIS EDITAR MANUALMENTE output.css. Como esse arquivo é gerado automaticamente pelo Tailwind (através do comando acima no terminal), qualquer alteração que você fizer nele será completamente apagada e reescrita na próxima vez que você der um Ctrl + S no seu HTML. Assim, podemos simplesmente ignorar os problemas e dar continuidade no arquivo HTML.

## 📝 Aula 2: Tipografia e Cores
O Tailwind possui um sistema muito intuitivo para estilizar textos e cores. Em vez de criar arquivos CSS separados para definir o tamanho, a cor e a fonte de um título, você aplica utilitários diretamente no HTML, o que deixa a padronização visual do projeto muito mais fácil.

### Conceitos aplicados na aula:
Tamanhos de Texto (text-sm, text-lg, text-3xl): O Tailwind usa uma escala de tamanhos que vai do menor (xs, sm) passando pelo base (base, lg, xl) até os tamanhos gigantes para títulos (2xl, 3xl, até 9xl).

Cores de Texto e Fundo (text-red-700, bg-cyan-200): A paleta de cores padrão funciona com uma escala de intensidade de 50 (quase branco) a 950 (quase preto). O bg- muda a cor do fundo da caixa, e o text- muda a cor da letra.

Família de Fontes (font-sans, font-serif, font-mono):

- sans: Fontes sem serifa (linhas retas, como Arial). É o padrão da web.

- serif: Fontes com serifa (com "perninhas", como Times New Roman). Boas para textos longos/jornais.

- mono: Fontes monoespaçadas (como letras de máquina de escrever ou código de programação).

Peso da Fonte (font-thin, font-semibold, font-bold): Define a espessura da letra, variando do mais fino (thin = 100) até o mais grosso (black = 900).

Decorações e Estilos (italic, underline, line-through): Estilos rápidos para deixar o texto em itálico, sublinhado ou riscado (útil para preços com desconto, por exemplo).

Combinação de Classes: O Tailwind permite empilhar quantas classes você quiser no mesmo elemento, aplicando todos os estilos de uma só vez.

### Outros conceitos de Tipografia:
Alinhamento de Texto (text-left, text-center, text-right): Controla o alinhamento do texto dentro do contêiner, como no Word. Há também o text-justify para preencher o espaço inteiro.

Transformação de Texto (uppercase, lowercase, capitalize): Muda o texto para tudo maiúsculo, tudo minúsculo, ou apenas a primeira letra de cada palavra maiúscula, sem precisar reescrever o texto no HTML.

Espaçamento entre Letras (tracking-tight, tracking-wide): Controla o "letter-spacing". O tight aproxima as letras (ótimo para títulos grandes), e o wide afasta (bom para textos pequenos ficarem mais legíveis).

Altura da Linha (leading-none, leading-relaxed): Controla o espaço entre as linhas de um parágrafo ("line-height").

## 📦 Aula 3: Introdução ao Flexbox
O Flexbox (Flexible Box) é um modelo de layout projetado para organizar elementos em uma única dimensão (ou seja, em uma linha horizontal ou em uma coluna vertical). Ele é perfeito para alinhar itens, distribuir espaços e lidar com tamanhos dinâmicos.

### Conceitos aplicados na aula:
- flex: Transforma a div principal em um contêiner flexível, colocando todos os elementos filhos lado a lado por padrão.

- flex-wrap: O comportamento padrão do flex é tentar espremer tudo na mesma linha. O wrap permite que os itens "pulem" para a linha de baixo caso acabe o espaço na tela.

- gap-4: Adiciona um espaçamento uniforme (neste caso, 16px) entre os itens, sem precisar usar margens individuais em cada um.

- w-min: Define que a largura do elemento será o mínimo necessário para caber o seu conteúdo (no caso, os números "01", "02").

- p-4 (Padding): Espaçamento interno. Afasta o texto das bordas da caixa.

- m-4 (Margin): Espaçamento externo. Afasta a caixa dos outros elementos ao redor.

### Outros conceitos de Flex:
- flex-col: Muda a direção do flex. Em vez de ficarem lado a lado (linha), os itens ficam um embaixo do outro (coluna).

- justify-center / justify-between: Alinha os itens no eixo principal (horizontal, se for linha). O center centraliza, e o between joga um item para cada ponta, distribuindo o espaço no meio.

- items-center: Centraliza os itens no eixo secundário (vertical). Muito usado para alinhar um ícone e um texto exatamente no meio da mesma linha.

## 🔲 Aula 4: Introdução ao CSS Grid
Enquanto o Flexbox trabalha em uma dimensão (linha OU coluna), o Grid é um sistema bidimensional, ou seja, ele permite organizar o layout trabalhando com linhas e colunas simultaneamente. É ideal para criar a estrutura principal de uma página (como galerias de fotos, painéis de informações, etc).

### Conceitos aplicados na aula:
- grid: Ativa o modelo de Grid no contêiner.

- grid-cols-3: Define explicitamente que o seu contêiner terá 3 colunas de tamanhos iguais.

- gap-x-3 e gap-y-8: O Grid permite ter espaços diferentes para colunas (eixo X) e para as linhas (eixo Y). O gap-3 (sozinho) aplicaria o mesmo espaço para ambos os lados.

- col-span-2 / col-span-3: Esse é o grande poder do Grid! Permite que um único elemento "estique" e ocupe o espaço de 2 ou 3 colunas, quebrando a padronização e criando layouts mais complexos.

- size-8: Um atalho muito útil do Tailwind que aplica altura e largura ao mesmo tempo (equivale a usar w-8 h-8).

### Outros conceitos de Grid:
- grid-rows-X: Assim como as colunas, você pode definir quantas linhas o seu grid terá (ex: grid-rows-2).

- row-span-X: Da mesma forma que um elemento pode ocupar várias colunas, ele pode se esticar para baixo, ocupando várias linhas (ex: row-span-2).

**Flex vs Grid (Regra de ouro): Use Flexbox quando quiser organizar itens em um fluxo contínuo (uma barra de navegação, botões lado a lado). Use Grid quando precisar de uma estrutura rígida de colunas e linhas (uma galeria de imagens, o esqueleto da página inteira)**