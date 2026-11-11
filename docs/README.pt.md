<p align="center">
  <a href="../README.md">English</a> ·
  <a href="README.fr.md">Français</a> ·
  <a href="README.de.md">Deutsch</a> ·
  <a href="README.es.md">Español</a> ·
  <a href="README.it.md">Italiano</a> ·
  <strong>Português</strong>
</p>

<p align="center">
  <img src="images/hero.svg" alt="Thierry Skill: direção de arte web à medida" width="100%">
</p>

# Thierry Skill

**Um diretor de arte para o Claude.** Com este skill, o Claude desenha sites como um bom estúdio: encontra uma ideia no ofício do cliente, deduz dela um sistema visual completo, constrói o site, olha para o resultado no ecrã e dá-lhe uma nota antes de o dar por terminado.

[![Licença: MIT](https://img.shields.io/badge/licença-MIT-14161a.svg)](../LICENSE)
![Compatível com Claude Code](https://img.shields.io/badge/Claude_Code-skill-e5412d.svg)
![Língua do skill: francês](https://img.shields.io/badge/língua_do_skill-francês-5c6370.svg)

```bash
npx skills@latest add Jacckisback/thierry-skills
```

## O problema

Os agentes de IA escrevem código de interface correto. Falta-lhes um ponto de vista. Peça «um site bonito e moderno» e recebe a média de todos os sites: a mesma fonte, o mesmo gradiente roxo, os mesmos três cartões com ícones. Nada está errado e nada fica na memória.

Os skills de design existentes polem sobretudo a superfície: curvas, durações, microinterações. Esse trabalho conta, mas vem no fim. Um site com animações perfeitas e sem ideia continua a ser um modelo pronto.

## O que este skill muda

Obriga o Claude a responder a três perguntas, por ordem, antes de acrescentar qualquer efeito:

1. **Qual é a ideia?** Uma frase que diga algo preciso sobre este cliente, e que o site de um concorrente não poderia dizer.
2. **Qual é o sistema?** Tipografia, cor, espaço, forma, imagem, voz e movimento, todos deduzidos dessa ideia.
3. **Funciona no ecrã?** Capturas em três larguras, medidas e avaliadas.

Dois briefings de uma só frase, dois resultados sem relação:

<table>
  <tr>
    <td width="50%"><img src="images/demo-luthier.png" alt="Página inicial de um construtor de guitarras, composta como o livro de encomendas da oficina"></td>
    <td width="50%"><img src="images/demo-pour-contre.png" alt="Primeiro ecrã do site de uma advogada de direito do trabalho: A FAVOR dos trabalhadores, CONTRA o seu empregador"></td>
  </tr>
  <tr>
    <td><em>«Um site para um construtor de guitarras flamencas em Madrid, três guitarras por mês, por encomenda.»</em><br>Ideia: o livro de encomendas da oficina. Três linhas por mês, e uma pode ter o seu nome.</td>
    <td><em>«Um site para uma advogada de direito do trabalho em Lyon que só defende trabalhadores.»</em><br>Ideia: uma peça processual. «A favor: os trabalhadores. Contra: o seu empregador.»</td>
  </tr>
</table>

As duas páginas foram geradas pelo skill durante os testes, a partir de briefings fictícios. Avaliadas com a sua própria grelha, obtiveram 81 e 82 em 100. Ficam abaixo do seu limiar de 85, sobretudo porque um briefing de uma frase não traz fotografias reais, preços nem provas, e o skill assinala esses espaços como «a fornecer» em vez de os inventar.

## A direção de arte, explicada

Um site é belo quando três coisas são verdadeiras ao mesmo tempo:

- **Uma ideia.** Diz algo específico sobre o seu assunto.
- **Um sistema.** Cada escolha visual decorre dessa ideia, e as escolhas respondem umas às outras.
- **Uma execução.** Cada detalhe invisível está certo: alinhamentos, estados, ritmo, velocidade, acessibilidade.

A maioria dos sites falha o primeiro ponto e compensa com efeitos. Um efeito nunca é uma ideia.

O skill procura a ideia naquilo de que o ofício é feito: objetos, documentos, gestos, lugares, materiais, palavras e medidas. Um garrafeiro tem rótulos e notas de prova. Uma arquiteta tem plantas e cortes. Um advogado tem peças processuais. Essas formas já pertencem ao cliente, por isso um site construído a partir delas não se confunde com o de mais ninguém.

O teste central é o do **logótipo trocado**: substitua o logótipo pelo de um concorrente direto. Se o site continuar a funcionar, não há ideia, e o trabalho recomeça.

<p align="center">
  <img src="images/process.svg" alt="Os sete passos do skill" width="100%">
</p>

*Os sete passos: compreender, encontrar a ideia, afinar a personalidade, construir o sistema, compor, executar, olhar e avaliar.*

### A personalidade em números

«Caloroso», «sério» ou «ousado» não dizem nada a uma folha de estilos. O skill posiciona sete cursores de 0 a 10 (temperatura, densidade, energia, ornamento, época, registo, contraste) e converte cada um em parâmetros concretos: raios, pesos, espaçamento entre letras, durações, margens, saturação. Dois negócios do mesmo setor recebem afinações diferentes, e é daí que vem o trabalho à medida.

<p align="center">
  <img src="images/sliders.svg" alt="Sete cursores de personalidade para duas direções do mesmo ofício" width="100%">
</p>

## Em números

| | |
| --- | --- |
| **7** | passos, do briefing à revisão |
| **9** | leis que o skill nunca quebra sem que lho peçam |
| **7** | cursores de personalidade, cada um convertido em valores exatos |
| **21** | setores, com as expectativas do visitante, os clichés a evitar e duas direções opostas |
| **10** | arquiteturas de primeiro ecrã à escolha |
| **11** | ficheiros de referência, cerca de 30 000 palavras, carregados só quando são precisos |
| **6** | línguas com regras tipográficas: francês, espanhol, alemão, inglês, italiano, português |
| **35** | verificações estáticas ao código (`audit.mjs`) |
| **22** | verificações à página renderizada (`regard.mjs`) |
| **100** | pontos na grelha de revisão, em 9 eixos ponderados |

## Verifica o seu próprio trabalho

Um design julgado apenas pela leitura do código não foi julgado. O último passo é obrigatório: capturar, olhar, avaliar, corrigir.

O `regard.mjs` abre a página num navegador real em três larguras. Guarda o primeiro ecrã, a página inteira, secções legíveis, uma versão em tons de cinzento e uma versão desfocada, e depois mede o que escapa ao olho.

<table>
  <tr>
    <td width="33%"><img src="images/regard-ecran.png" alt="Captura do primeiro ecrã"></td>
    <td width="33%"><img src="images/regard-gris.png" alt="Captura em tons de cinzento"></td>
    <td width="33%"><img src="images/regard-flou.png" alt="Captura desfocada"></td>
  </tr>
  <tr>
    <td><strong>Primeiro ecrã.</strong> O teste dos cinco segundos: o que retém um desconhecido?</td>
    <td><strong>Tons de cinzento.</strong> A hierarquia aguenta-se sem a cor?</td>
    <td><strong>Desfocada.</strong> O teste de semicerrar os olhos: uma massa dominante, depois uma segunda, depois o resto.</td>
  </tr>
</table>

Medido em cada passagem: o contraste do texto face aos limiares WCAG, o transbordo horizontal, os alvos táteis abaixo de 24 e 44 px, o comprimento das linhas, as famílias e os tamanhos de letra realmente apresentados, as fontes que não carregaram, as imagens sem dimensões ou sem texto alternativo, a estrutura dos títulos, os campos sem rótulo, os saltos de layout e o que continua a mexer quando o visitante pediu menos movimento.

O `audit.mjs` lê o código-fonte e assinala vícios de modelo e falhas de execução: `transition: all`, entradas a partir de `scale(0)`, anéis de foco removidos, gradientes roxos, texto de preenchimento, botões com rótulos vagos, pontuação francesa incorreta.

Depois a página recebe uma nota. Abaixo de 85, as três fraquezas mais graves são corrigidas e a página é capturada de novo.

<p align="center">
  <img src="images/score.svg" alt="A grelha de revisão de 100 pontos" width="100%">
</p>

*A grelha: ideia e personalidade 20, tipografia 15, composição 15, cor e forma 10, conteúdo e voz 10, acabamentos 10, acessibilidade e desempenho 10, imagem 5, movimento 5.*

## O que pode pedir

| Diz | O skill entrega |
| --- | --- |
| «Cria um site para…» | uma ficha de direção de arte, o código e uma revisão sobre capturas |
| «Refaz este site» | um diagnóstico, o que se mantém, uma nova direção, um antes e depois |
| «O que achas?» | uma nota em 100 e correções ordenadas, sem alterar nada |
| «Dá-lhe um polimento» | acabamentos que não tocam no conceito |
| «Parece genérico», «parece feito por IA» | a lista dos vícios encontrados e o que substitui cada um |
| «Dá-me opções» | três direções que diferem no conceito, não na cor |
| «Prompt para o Lovable» | um prompt pronto a colar no Lovable ou noutro gerador |

## Instalar

```bash
npx skills@latest add Jacckisback/thierry-skills
```

Ou à mão: copie `skills/thierry-skill` para a pasta `.claude/skills/` do seu projeto, ou para `~/.claude/skills/` para o ter em todo o lado. Nas aplicações do Claude, comprima a pasta `skills/thierry-skill` num `.zip` e carregue-o nas definições de skills.

Os dois scripts precisam do Node 18 ou posterior. O `regard.mjs` precisa também do Playwright com Chromium:

```bash
npm i -D playwright
```

```bash
npx playwright install chromium
```

## Utilizar

Basta uma frase:

> Usa o thierry-skill: cria a página inicial de uma loja de vinhos naturais em Madrid.

O skill está escrito em francês e responde na língua em que lhe escrever. Constrói sites em qualquer língua.

Os scripts também podem ser lançados à mão:

```bash
node skills/thierry-skill/scripts/regard.mjs http://localhost:3000 --out revisao
```

```bash
node skills/thierry-skill/scripts/audit.mjs ./src
```

## Conteúdo

```
skills/thierry-skill/
├── SKILL.md                         processo, leis, formatos de entrega
├── references/
│   ├── 01-direction-artistique.md   conceito, assinatura, tabela de conversão dos cursores
│   ├── 02-univers-par-secteur.md    21 setores: expectativas, clichés, duas direções cada
│   ├── 03-typographie.md            escolha, combinação, escala, afinação, carregamento
│   ├── 04-couleur.md                paletas em OKLCH, contraste, modo escuro
│   ├── 05-composition.md            espaço, grelha, primeiro ecrã, imagem, telemóvel
│   ├── 06-mouvement.md              quando animar, curvas, durações, coreografia
│   ├── 07-finitions.md              estados, formulários, acessibilidade, desempenho, SEO
│   ├── 08-anti-generique.md         os vícios «feito por IA» e os seus substitutos
│   ├── 09-ecriture.md               títulos, botões, tipografia em seis línguas
│   ├── 10-revue.md                  a grelha de 100 pontos e o formato da revisão
│   └── 11-brief-lovable.md          modelo de prompt com um exemplo preenchido
├── assets/tokens.css                variáveis CSS neutras para adaptar
└── scripts/
    ├── regard.mjs                   capturas e medições
    └── audit.mjs                    auditoria estática do código
```

## O objetivo

Sites que só possam pertencer ao seu dono. Um visitante deve conseguir descrever o site de memória no dia seguinte, e o cliente deve reconhecer nele o seu próprio ofício. O skill trata a beleza como o resultado da precisão: uma ideia verdadeira, um sistema rigoroso e uma prova no ecrã.

## Limites

- Não substitui o conteúdo do cliente. Sem fotografias, preços e provas reais, assinala os espaços e a nota fica limitada.
- As direções por setor são pontos de partida. Usadas tal como estão, dariam o mesmo site a todos os negócios de um setor.
- Os scripts dão indícios a confirmar a olho. Não testam a navegação por teclado, os estados dos formulários nem os leitores de ecrã.
- Os resultados dependem do modelo que executa o skill e, até agora, só foram testados com dois briefings.

## Origem

Este skill nasceu do estudo atento dos [skills de Emil Kowalski](https://github.com/emilkowalski/skills), que tratam a animação e o detalhe de interface com grande precisão. Alarga o campo à direção de arte completa e acrescenta a verificação do resultado no ecrã. Todo o texto e código são originais.

## Licença

[MIT](../LICENSE)
