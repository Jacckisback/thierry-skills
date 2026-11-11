<p align="center">
  <a href="../README.md">English</a> ·
  <a href="README.fr.md">Français</a> ·
  <a href="README.de.md">Deutsch</a> ·
  <a href="README.es.md">Español</a> ·
  <strong>Italiano</strong> ·
  <a href="README.pt.md">Português</a>
</p>

<p align="center">
  <img src="images/hero.svg" alt="Thierry Skill: direzione artistica web su misura" width="100%">
</p>

# Thierry Skill

**Un direttore artistico per Claude.** Con questo skill Claude progetta siti web come fa un buono studio: trova un'idea nel mestiere del cliente, ne ricava un sistema visivo completo, costruisce il sito, guarda il risultato a schermo e gli dà un voto prima di considerarlo finito.

[![Licenza: MIT](https://img.shields.io/badge/licenza-MIT-14161a.svg)](../LICENSE)
![Compatibile con Claude Code](https://img.shields.io/badge/Claude_Code-skill-e5412d.svg)
![Lingua dello skill: francese](https://img.shields.io/badge/lingua_dello_skill-francese-5c6370.svg)

```bash
npx skills@latest add Jacckisback/thierry-skills
```

## Il problema

Gli agenti IA scrivono codice d'interfaccia corretto. Manca loro un punto di vista. Chiedete «un bel sito moderno» e otterrete la media di tutti i siti: lo stesso carattere, lo stesso gradiente viola, le stesse tre schede con icone. Niente è sbagliato e niente resta in mente.

Gli skill di design esistenti rifiniscono soprattutto la superficie: curve, durate, microinterazioni. È un lavoro che conta, ma viene per ultimo. Un sito con animazioni perfette e senza idea resta un modello preconfezionato.

## Che cosa cambia questo skill

Obbliga Claude a rispondere a tre domande, in ordine, prima di aggiungere qualsiasi effetto:

1. **Qual è l'idea?** Una frase che dica qualcosa di preciso su questo cliente, e che il sito di un concorrente non potrebbe dire.
2. **Qual è il sistema?** Tipografia, colore, spazio, forma, immagine, voce e movimento, tutti ricavati da quell'idea.
3. **Funziona a schermo?** Schermate a tre larghezze, misurate e valutate.

Due brief di una sola frase, due risultati senza alcun legame:

<table>
  <tr>
    <td width="50%"><img src="images/demo-luthier.png" alt="Pagina iniziale di un liutaio, composta come il registro degli ordini della bottega"></td>
    <td width="50%"><img src="images/demo-pour-contre.png" alt="Prima schermata del sito di un'avvocata giuslavorista: PER i lavoratori, CONTRO il loro datore di lavoro"></td>
  </tr>
  <tr>
    <td><em>«Un sito per un liutaio di chitarre flamenche a Madrid, tre chitarre al mese, su ordinazione.»</em><br>Idea: il registro degli ordini della bottega. Tre righe al mese, e una può portare il vostro nome.</td>
    <td><em>«Un sito per un'avvocata giuslavorista di Lione che difende solo i lavoratori.»</em><br>Idea: un atto giudiziario. «Per: i lavoratori. Contro: il loro datore di lavoro.»</td>
  </tr>
</table>

Entrambe le pagine sono state generate dallo skill durante le prove, a partire da brief fittizi. Valutate con la sua stessa griglia, hanno ottenuto 81 e 82 su 100. Sono sotto la sua soglia di 85, soprattutto perché un brief di una frase non contiene foto vere, prezzi né prove, e lo skill segna quegli spazi come «da fornire» invece di inventarli.

## La direzione artistica, spiegata

Un sito è bello quando tre cose sono vere insieme:

- **Un'idea.** Dice qualcosa di specifico sul suo soggetto.
- **Un sistema.** Ogni scelta visiva discende da quell'idea, e le scelte si rispondono tra loro.
- **Un'esecuzione.** Ogni dettaglio invisibile è giusto: allineamenti, stati, ritmo, velocità, accessibilità.

La maggior parte dei siti manca il primo punto e compensa con gli effetti. Un effetto non è mai un'idea.

Lo skill cerca l'idea in ciò di cui è fatto il mestiere: oggetti, documenti, gesti, luoghi, materiali, parole e misure. Un enotecario ha etichette e schede di degustazione. Un'architetta ha piante e sezioni. Un avvocato ha atti. Queste forme appartengono già al cliente, quindi un sito costruito a partire da esse non può essere scambiato per quello di un altro.

La prova centrale è quella del **logo scambiato**: sostituite il logo con quello di un concorrente diretto. Se il sito funziona ancora, non c'è un'idea, e il lavoro ricomincia.

<p align="center">
  <img src="images/process.svg" alt="I sette passi dello skill" width="100%">
</p>

*I sette passi: capire, trovare l'idea, regolare la personalità, costruire il sistema, comporre, eseguire, guardare e valutare.*

### La personalità in numeri

«Caldo», «serio» o «audace» non dicono nulla a un foglio di stile. Lo skill posiziona sette cursori da 0 a 10 (temperatura, densità, energia, ornamento, epoca, registro, contrasto) e converte ciascuno in parametri concreti: raggi, pesi, spaziatura tra le lettere, durate, margini, saturazione. Due attività dello stesso settore ricevono regolazioni diverse: è da qui che nasce il su misura.

<p align="center">
  <img src="images/sliders.svg" alt="Sette cursori di personalità per due direzioni dello stesso mestiere" width="100%">
</p>

## In cifre

| | |
| --- | --- |
| **7** | passi, dal brief alla revisione |
| **9** | leggi che lo skill non infrange mai se non gli viene chiesto |
| **7** | cursori di personalità, ciascuno convertito in valori esatti |
| **21** | settori, con le attese del visitatore, i cliché da evitare e due direzioni opposte |
| **10** | architetture di prima schermata tra cui scegliere |
| **11** | file di riferimento, circa 30.000 parole, caricati solo quando servono |
| **6** | lingue con regole tipografiche: francese, spagnolo, tedesco, inglese, italiano, portoghese |
| **35** | controlli statici sul codice (`audit.mjs`) |
| **22** | controlli sulla pagina renderizzata (`regard.mjs`) |
| **100** | punti nella griglia di revisione, su 9 assi ponderati |

## Controlla il proprio lavoro

Un progetto giudicato solo leggendo il codice non è stato giudicato. L'ultimo passo è obbligatorio: catturare, guardare, valutare, correggere.

`regard.mjs` apre la pagina in un vero browser a tre larghezze. Salva la prima schermata, la pagina intera, sezioni leggibili, una versione in scala di grigi e una versione sfocata, poi misura ciò che all'occhio sfugge.

<table>
  <tr>
    <td width="33%"><img src="images/regard-ecran.png" alt="Schermata della prima vista"></td>
    <td width="33%"><img src="images/regard-gris.png" alt="Schermata in scala di grigi"></td>
    <td width="33%"><img src="images/regard-flou.png" alt="Schermata sfocata"></td>
  </tr>
  <tr>
    <td><strong>Prima schermata.</strong> La prova dei cinque secondi: che cosa ricorda uno sconosciuto?</td>
    <td><strong>Scala di grigi.</strong> La gerarchia regge senza il colore?</td>
    <td><strong>Sfocata.</strong> La prova degli occhi socchiusi: una massa dominante, poi una seconda, poi il resto.</td>
  </tr>
</table>

A ogni passaggio vengono misurati: il contrasto del testo rispetto alle soglie WCAG, lo sbordamento orizzontale, le aree tattili sotto i 24 e i 44 px, la lunghezza delle righe, le famiglie e le dimensioni dei caratteri realmente visualizzate, i caratteri non caricati, le immagini senza dimensioni o senza testo alternativo, la struttura dei titoli, i campi senza etichetta, gli spostamenti di layout e ciò che continua a muoversi quando il visitatore ha chiesto meno movimento.

`audit.mjs` legge il codice sorgente e segnala i vizi da modello e gli errori di esecuzione: `transition: all`, ingressi da `scale(0)`, anelli di focus rimossi, gradienti viola, testo segnaposto, etichette di pulsanti vaghe, punteggiatura francese errata.

Poi la pagina riceve un voto. Sotto 85, le tre debolezze più gravi vengono corrette e la pagina viene catturata di nuovo.

<p align="center">
  <img src="images/score.svg" alt="La griglia di revisione da 100 punti" width="100%">
</p>

*La griglia: idea e personalità 20, tipografia 15, composizione 15, colore e forma 10, contenuto e voce 10, finiture 10, accessibilità e prestazioni 10, immagine 5, movimento 5.*

## Che cosa potete chiedere

| Voi dite | Lo skill consegna |
| --- | --- |
| «Crea un sito per…» | una scheda di direzione artistica, il codice, poi una revisione sulle schermate |
| «Rifai questo sito» | una diagnosi, che cosa tenere, una nuova direzione, un prima e dopo |
| «Che ne pensi?» | un voto su 100 e correzioni ordinate, senza modificare nulla |
| «Rifiniscilo» | finiture che non toccano il concetto |
| «Sembra generico», «sembra fatto dall'IA» | l'elenco dei vizi trovati e ciò che sostituisce ciascuno |
| «Dammi delle opzioni» | tre direzioni che differiscono nel concetto, non nel colore |
| «Prompt per Lovable» | un prompt pronto da incollare in Lovable o in un altro generatore |

## Installazione

```bash
npx skills@latest add Jacckisback/thierry-skills
```

Oppure a mano: copiate `skills/thierry-skill` nella cartella `.claude/skills/` del vostro progetto, o in `~/.claude/skills/` per averlo ovunque. Nelle app di Claude, comprimete la cartella `skills/thierry-skill` in uno `.zip` e caricatelo nelle impostazioni degli skill.

I due script richiedono Node 18 o successivo. `regard.mjs` richiede anche Playwright con Chromium:

```bash
npm i -D playwright
```

```bash
npx playwright install chromium
```

## Uso

Basta una frase:

> Usa thierry-skill: crea la pagina iniziale di un'enoteca di vini naturali a Madrid.

Lo skill è scritto in francese e risponde nella lingua in cui scrivete. Costruisce siti in qualsiasi lingua.

Gli script si possono lanciare anche a mano:

```bash
node skills/thierry-skill/scripts/regard.mjs http://localhost:3000 --out revisione
```

```bash
node skills/thierry-skill/scripts/audit.mjs ./src
```

## Contenuto

```
skills/thierry-skill/
├── SKILL.md                         processo, leggi, formati di consegna
├── references/
│   ├── 01-direction-artistique.md   concetto, firma, tabella di conversione dei cursori
│   ├── 02-univers-par-secteur.md    21 settori: attese, cliché, due direzioni ciascuno
│   ├── 03-typographie.md            scelta, abbinamenti, scala, regolazioni fini, caricamento
│   ├── 04-couleur.md                palette in OKLCH, contrasto, modalità scura
│   ├── 05-composition.md            spazio, griglia, prima schermata, immagine, mobile
│   ├── 06-mouvement.md              quando animare, curve, durate, coreografia
│   ├── 07-finitions.md              stati, moduli, accessibilità, prestazioni, SEO
│   ├── 08-anti-generique.md         i vizi «fatto dall'IA» e i loro sostituti
│   ├── 09-ecriture.md               titoli, pulsanti, tipografia in sei lingue
│   ├── 10-revue.md                  la griglia da 100 punti e il formato della revisione
│   └── 11-brief-lovable.md          modello di prompt con un esempio compilato
├── assets/tokens.css                variabili CSS neutre da adattare
└── scripts/
    ├── regard.mjs                   schermate e misure
    └── audit.mjs                    verifica statica del codice
```

## L'obiettivo

Siti che possano appartenere solo al loro proprietario. Un visitatore dovrebbe saper descrivere il sito a memoria il giorno dopo, e il cliente dovrebbe riconoscervi il proprio mestiere. Lo skill considera la bellezza il risultato della precisione: un'idea vera, un sistema rigoroso e una prova a schermo.

## Limiti

- Non sostituisce i contenuti del cliente. Senza foto, prezzi e prove reali segna gli spazi, e il voto resta limitato.
- Le direzioni per settore sono punti di partenza. Usate così come sono, darebbero lo stesso sito a tutte le attività di un settore.
- Gli script forniscono indizi da verificare a occhio. Non provano la navigazione da tastiera, gli stati dei moduli né i lettori di schermo.
- I risultati dipendono dal modello che esegue lo skill e finora sono stati provati solo su due brief.

## Origine

Questo skill è nato dallo studio attento degli [skill di Emil Kowalski](https://github.com/emilkowalski/skills), che trattano l'animazione e il dettaglio d'interfaccia con grande precisione. Allarga il campo alla direzione artistica completa e aggiunge la verifica del risultato a schermo. Tutto il testo e il codice sono originali.

## Licenza

[MIT](../LICENSE)
