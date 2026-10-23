# HTML e CSS — roteiro de apresentação

18 slides • duração sugerida: 17 a 20 minutos, com demonstração.

## Sugestão para dividir o grupo

- Pessoa 1: slides 1–5 — contexto, estrutura e tags.
- Pessoa 2: slides 6–9 — formulários, CSS e seletores.
- Pessoa 3: slides 10–14 — box model, layout e acessibilidade.
- Pessoa 4: slides 15–18 — demonstração, revisão e referências.

Adaptem os blocos à quantidade de integrantes.

## Slide 01

Abertura (40 s). Apresente o grupo e diga: HTML organiza o conteúdo; CSS define a apresentação. Vamos construir uma página de cursos para conectar cada conceito a algo visível. Acrescente nomes e turma à capa se desejar.

## Slide 02

Visão geral (45 s). O navegador cria uma representação da estrutura HTML, aplica as regras CSS e calcula o layout antes de desenhar. HTML e CSS não substituem a lógica de negócio ou o banco de dados. JavaScript é uma terceira camada comum, mas não será necessário no exemplo.

## Slide 03

Aplicação (45 s). Dê exemplos próximos: site da escola, sistema de matrícula e loja online. Mesmo com React, Angular ou outros frameworks, a interface continua baseada em elementos HTML e regras CSS. Semântica e responsividade afetam acesso, manutenção e usabilidade.

## Slide 04

Estrutura (1 min). Explique abertura, conteúdo e fechamento de uma tag usando h1. Atributos são informações na tag de abertura: lang é um exemplo. meta é um elemento vazio, sem tag de fechamento. title aparece na aba; h1 aparece no documento. UTF-8 permite os caracteres usados em português. A viewport é importante para o layout em dispositivos móveis.

## Slide 05

Tags (1 min). header representa conteúdo introdutório; nav identifica a navegação; main é o conteúdo principal; section agrupa um tema; article é um conteúdo independente; footer é um rodapé. Mostre que section normalmente recebe um título. Exemplo de link: <a href="#inscricao">Inscrição</a>. Exemplo de imagem informativa: <img src="turma.jpg" alt="Turma apresentando projetos">. Imagens decorativas recebem alt vazio. div e span continuam úteis quando não existe semântica específica.

## Slide 06

Formulários (1 min 15 s). Explique que id conecta o campo ao label e deve ser único; name é a chave no envio. method=post envia dados no corpo da requisição, mas não cifra os dados: HTTPS é que protege o transporte. /cadastro é uma rota ilustrativa que exige backend; ela não existe no arquivo demonstrativo. required faz a validação no navegador, mas pode ser contornada, por isso o servidor precisa validar novamente. textarea coleta texto longo; checkbox e radio são outros tipos úteis. Placeholder não substitui label.

## Slide 07

CSS (1 min). .card é o seletor. O bloco entre chaves contém declarações no formato propriedade: valor. background define o fundo; color define a cor do texto; padding cria espaço interno; border-radius arredonda os cantos. CSS pode ser externo, interno em style ou inline. Para manutenção, normalmente preferimos um arquivo externo. O exemplo demonstrativo usa style no mesmo HTML para ser aberto sem outros arquivos.

## Slide 08

Seletores (1 min). Um elemento pode ter várias classes separadas por espaços. Um mesmo nome de classe pode ser reutilizado em vários elementos. id é único e também serve de destino para links internos. Para regras reutilizáveis, classes são uma boa escolha. O seletor de atributo e a pseudoclasse mostrados são seletores válidos mesmo sem chaves completas nesta tabela. :focus-visible permite destacar o elemento focado quando isso é apropriado, como na navegação por teclado.

## Slide 09

Cascata (1 min). Todas as regras do exemplo são de mesma origem, mesma importância e sem camadas. Nesse contexto, o ID tem especificidade maior que a classe; a classe tem mais que o tipo. A ordem no arquivo resolve um empate de especificidade. A cascata completa considera origem, importância e camadas antes da especificidade. Não diga que ID sempre vence qualquer CSS. Evite resolver conflitos adicionando IDs ou !important sem compreender a causa.

## Slide 10

Box model (1 min). Do centro para fora: conteúdo, padding, border e margin. Padding é espaço dentro da borda; margin é espaço fora dela. Com border-box, width já inclui padding e borda, mas nunca a margem. Exemplo: width de 300px com padding de 20px em cada lado e borda de 1px mantém largura total de 300px com border-box; com content-box teria 342px, sem contar margem.

## Slide 11

Flexbox (1 min). O padrão é flex-direction: row, então o eixo principal é horizontal neste exemplo. Se mudar para column, os eixos mudam. O justify-content: space-between coloca espaço entre os itens; align-items: center centraliza no eixo transversal. gap pode definir espaçamento entre itens; flex-wrap: wrap permite quebra em novas linhas quando necessário. O exemplo demonstrativo utiliza essas duas propriedades adicionais.

## Slide 12

Grid (1 min). grid-template-columns define as colunas; repeat evita repetir a mesma declaração; 1fr representa uma fração do espaço livre. gap define os intervalos entre as células. Flex e Grid podem coexistir: o projeto usa Flex na navegação e Grid nos cards. O HTML do exemplo envolve os três articles em uma div class=cursos. Para conteúdo potencialmente longo, o exemplo completo usa minmax(0, 1fr) para permitir que as trilhas encolham.

## Slide 13

Responsividade (1 min). Quando a viewport tem até 700px, a regra muda os cards de três para uma coluna. O breakpoint deve responder ao conteúdo, não só ao nome de um aparelho. A meta viewport do slide 4 evita a viewport virtual típica de páginas antigas no celular. Use max-width, porcentagens, rem e clamp quando fizer sentido; para imagens, max-width:100% e height:auto são um ponto de partida. Media query não detecta o tipo do dispositivo: testa uma condição da viewport. O exemplo foi verificado em 1280px, 700px e 390px.

## Slide 14

Acessibilidade (1 min). Mostre a navegação com Tab no exemplo funcionando. Clicar no label deve focar o campo correto. Não remova outline sem fornecer um substituto acessível. Para texto comum, a WCAG nível AA normalmente exige contraste de pelo menos 4,5:1; texto grande tem limiar de 3:1. Esses valores não substituem uma avaliação completa de acessibilidade. A cor sozinha não deve transmitir estado, e placeholder não deve ser o único rótulo.

## Slide 15

Projeto (45 s). As duas imagens são capturas do exemplo real. Abra exemplo.html em um navegador. O arquivo está completo e não precisa de instalação, servidor, internet ou JavaScript. Explique que os slides anteriores usam trechos reduzidos para ensinar e que o arquivo contém os ajustes completos de layout, foco e espaçamento. Não há backend ou cadastro efetivo.

## Slide 16

Demonstração (2 min). Abra exemplo.html. 1: no modo responsivo das ferramentas do navegador, compare 1280px e 390px; observe a quebra dos cards e a ausência de rolagem horizontal. 2: use Tab para navegar e mostre o foco. Clique em um label. 3: no formulário, clique em Testar formulário sem preencher; o navegador deve apontar um obrigatório. Preencha Ana Exemplo e um texto sem arroba; o campo de e-mail deve rejeitar. Finalize com ana@example.com. Os dados fictícios aparecem na URL via GET e a página recarrega; não existe servidor salvando dados. Validação de interface não substitui validação no backend.

## Slide 17

Fechamento (1 min). Peça respostas ao desafio antes de encerrar. Resposta: class é reutilizável e um elemento pode ter várias classes; id identifica um elemento de forma única no documento. Margin fica fora da borda e padding fica dentro. Pergunta extra: qual regra faz os cards mudarem para uma coluna? Resposta: a media query que altera grid-template-columns para 1fr. Conhecimento central: HTML e CSS trabalham juntos, com estrutura e estilo separados conceitualmente.

## Slide 18

Referências (20 s). Estes são links de referência para aprofundamento, não uma lista de sites usados pelo projeto. Consulte a documentação de cada propriedade quando houver dúvida. Convide a turma a modificar o HTML e CSS do exemplo e observar o resultado no navegador.

## Como usar no Canva

Na página inicial do Canva, use a opção de importar/enviar arquivo e selecione Slides-HTML-e-CSS.pptx. Abra como apresentação e confira fontes, quebras de linha e imagens após a conversão. Os slides têm textos e formas editáveis. O PDF serve como referência visual; as capturas do exemplo são imagens.

## Exemplo prático

Abra exemplo.html em um navegador. Não precisa instalar nada. Use dados fictícios no formulário. Para estudar o código, abra o mesmo arquivo em um editor de texto.
