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

## 📐 Aula 5: Alinhamento de Itens no Grid
Aprofundamento no CSS Grid com foco no controle de alinhamento dos itens dentro das células. Enquanto nas aulas anteriores vimos como distribuir elementos em linhas e colunas, aqui exploramos como cada item se posiciona dentro do seu próprio espaço na grade.

### Conceitos aplicados na aula:

- justify-items-stretch: Faz com que cada item se estique horizontalmente para preencher toda a largura da célula do grid. É o comportamento padrão do grid, mas pode ser sobrescrito por outros valores.
- justify-items-start / justify-items-end / justify-items-center: Controla o alinhamento horizontal dos itens dentro das células. O start os empurra para a esquerda, o end para a direita, e o center os centraliza.
- items-baseline (Flex): No contexto do Flexbox, o items-baseline alinha todos os itens pela linha de base do texto, independentemente do tamanho de cada caixa — útil quando os elementos têm alturas diferentes mas precisam de alinhamento tipográfico consistente.

### Outros conceitos de alinhamento:

- place-items-center: Atalho que centraliza os itens tanto no eixo horizontal quanto no vertical de uma vez só (equivale a usar justify-items-center e items-center juntos).
- self-start / self-end / self-center: Enquanto as propriedades acima controlam todos os filhos a partir do contêiner, as variações com "self" permitem que um item individual sobrescreva o alinhamento definido pelo pai, posicionando apenas a si mesmo de forma diferente.

## 📏 Aula 6: Larguras e Alturas
O Tailwind oferece um sistema completo e flexível para controlar as dimensões dos elementos, combinando valores absolutos (fixos) e relativos (proporcionais ao contêiner pai). Dominar esse sistema é essencial para construir layouts que funcionem bem em diferentes tamanhos de tela.

### Conceitos aplicados na aula:

Tamanho Absoluto (w-6, w-12, w-24, w-48): Define larguras fixas baseadas na escala de espaçamento do Tailwind, onde cada unidade equivale a 4px (ex: w-6 = 24px, w-24 = 96px). Não se adapta ao contêiner pai.
Tamanho Relativo (w-1/4, w-1/3, w-1/2, w-2/3): Define a largura como uma fração do contêiner pai. Ótimo para criar divisões proporcionais dentro de um layout, como duas colunas de igual tamanho lado a lado.
w-full: Faz o elemento ocupar 100% da largura disponível no contêiner pai. É diferente de não definir largura nenhuma (comportamento padrão de elementos block).
- w-auto: Deixa o navegador calcular a largura automaticamente com base no conteúdo do elemento, semelhante ao comportamento natural de elementos inline.
- min-w-X (Largura Mínima): Garante que um elemento nunca ficará menor do que o valor definido, mesmo que o espaço disponível seja insuficiente. Útil para evitar que conteúdos sejam esmagados.
- max-w-X (Largura Máxima): Limita o crescimento de um elemento. Mesmo que o espaço disponível seja maior, o elemento não ultrapassará esse valor. Muito usado para manter textos legíveis em telas largas.
- size-X: Atalho que define largura e altura com um único valor ao mesmo tempo (equivale a usar w-X h-X juntos).
- h-X (Altura): Funciona da mesma forma que w-X, mas no eixo vertical. Pode também usar valores relativos como h-full e h-screen (100% da altura da viewport).

## 🎨 Aula 7: Bordas, Sombras e Opacidade
Além de tamanhos e posicionamento, o Tailwind oferece utilitários visuais para enriquecer a aparência dos elementos. Bordas, arredondamentos, sombras e opacidade são recursos fundamentais para dar profundidade e refinamento à interface.

### Conceitos aplicados na aula:

- border-2: Define a espessura da borda do elemento. O número representa a largura em pixels (border = 1px, border-2 = 2px, border-4 = 4px, etc.).
- border-green-800: Define a cor da borda usando a mesma paleta de cores do Tailwind. Deve ser usada junto com uma classe border-X para que a borda apareça.
- rounded-xl: Arredonda os cantos do elemento. A escala vai do sutil (rounded-sm) ao totalmente circular (rounded-full), passando por valores intermediários como rounded, rounded-md, rounded-lg e rounded-xl.
- shadow-lg: Adiciona uma sombra ao elemento. O tamanho varia de shadow-sm a shadow-2xl. A sombra usa por padrão uma cor escura semitransparente.
- shadow-blue-400: Personaliza a cor da sombra. Combinado com shadow-lg, permite criar efeitos visuais como "glows" coloridos, muito usados em interfaces modernas.
- opacity-100: Controla a transparência do elemento inteiro, de opacity-0 (invisível) a opacity-100 (totalmente visível). Valores intermediários como opacity-50 deixam o elemento semitransparente.

### Outros conceitos visuais:

- ring-X: Cria um contorno (outline) ao redor do elemento sem ocupar espaço no layout, diferentemente da border. Muito usado para indicar foco em campos de formulário.
- divide-X: Adiciona bordas automaticamente entre os elementos filhos de um contêiner, sem precisar adicionar borda em cada filho individualmente.

## 🖱️ Aula 8: Hover, Focus e Transições
O Tailwind facilita a criação de estados interativos como hover e focus diretamente no HTML, usando prefixos antes das classes de estilo. Combinados com as classes de transição, esses recursos permitem criar animações suaves e feedback visual para o usuário sem escrever nenhum CSS customizado.

### Conceitos aplicados na aula:

- hover:bg-teal-600: O prefixo hover: faz com que a classe só seja aplicada quando o mouse estiver sobre o elemento. Qualquer classe do Tailwind pode ser prefixada com hover:.
- focus:bg-teal-600: O prefixo focus: aplica o estilo quando o elemento está em foco (geralmente ao clicar ou navegar pelo teclado). Muito importante para acessibilidade.
- hover:scale-105: Aumenta o elemento em 5% ao passar o mouse, criando um efeito de "crescimento". Faz parte das classes de transformação (scale, rotate, translate).
- hover:bg-transparent: Remove a cor de fundo no hover, útil para criar botões que "esvaziam" e mostram só a borda ao passar o mouse.
- hover:border-4 / hover:border-teal-500: Adiciona borda no hover. Combinado com hover:bg-transparent e hover:text-black, cria o efeito clássico de botão "outline" ao passar o mouse.
- transition: Habilita a interpolação suave entre os estados padrão e o hover/focus. Sem ele, as mudanças de estilo ocorrem de forma abrupta e instantânea.
- duration-150 / duration-450: Controla a duração da transição em milissegundos. O 150 é rápido e responsivo, enquanto valores maiores criam animações mais lentas e dramáticas.

### Outros modificadores de estado:

- active: Aplica o estilo no momento exato do clique, enquanto o botão do mouse está pressionado. Ótimo para criar feedback tátil visual.
- disabled: Estiliza o elemento quando ele está desabilitado (atributo HTML disabled), como um botão que ainda não pode ser clicado.
- group-hover: Permite que um elemento filho mude de estilo quando o mouse passa sobre um elemento pai marcado com a classe group.

## 📱 Aula 9: Design Responsivo
O Tailwind adota por padrão a filosofia mobile-first: os estilos sem prefixo se aplicam a todas as telas, e os prefixos de breakpoint definem adaptações para telas maiores. Isso garante que o layout base seja sempre pensado para dispositivos móveis, crescendo progressivamente para telas maiores.

### Conceitos aplicados na aula:

- sm: (≥ 640px): Breakpoint para telas pequenas, como smartphones em modo paisagem e tablets pequenos.
- md: (≥ 768px): Breakpoint para tablets e telas médias.
- lg: (≥ 1024px): Breakpoint para laptops e desktops menores.
- lg:flex-row: Um exemplo prático de uso de breakpoint. A classe flex-col se aplica por padrão (mobile), e ao atingir o breakpoint lg a direção muda para flex-row, reorganizando o layout horizontalmente em telas maiores.
- sm:bg-pink-200 / md:bg-pink-300 / lg:bg-pink-400: Demonstração visual de breakpoints — a cor de fundo fica progressivamente mais escura conforme a tela aumenta, ilustrando como cada prefixo atua em sua faixa de tamanho correspondente.

### Outros breakpoints disponíveis:

- xl: (≥ 1280px): Para desktops maiores.
- 2xl: (≥ 1536px): Para monitores grandes e ultrawide.

*** Regra de ouro do mobile-first: Comece sempre estilizando para a tela menor (sem prefixo) e vá adicionando prefixos de breakpoint para adaptar o layout às telas maiores. Nunca ao contrário. ***